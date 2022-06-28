class DisableButton extends StatefulWidget {
  const DisableButton({
    Key key,
    this.width,
    this.height,
    this.isUserInscrit,
  }) : super(key: key);

  final double width;
  final double height;
  final bool isUserInscrit;

  @override
  _DisableButtonState createState() => _DisableButtonState();
}

class _DisableButtonState extends State<DisableButton> {
  @override
  Widget build(BuildContext context) {
    return Column(
      mainAxisSize: MainAxisSize.min,
      children: <Widget>[
        ElevatedButton(
          style: ElevatedButton.styleFrom(
              elevation: 10,
              primary: Colors.greenAccent,
              padding: const EdgeInsets.symmetric(horizontal: 50, vertical: 20),
              textStyle: const TextStyle(
                fontSize: 20,
                fontWeight: FontWeight.bold,
                fontFamily: 'Lexend Deca',
              )),
          onPressed: () {},
          child: const Text('Participer'),
        ),
        const SizedBox(height: 20),
        ElevatedButton(
          child: const Text('Se désinscrire'),
          onPressed: null,
          style: ElevatedButton.styleFrom(
              elevation: 10,
              primary: Colors.redAccent,
              padding: const EdgeInsets.symmetric(horizontal: 50, vertical: 20),
              textStyle: const TextStyle(
                fontSize: 20,
                fontWeight: FontWeight.bold,
                fontFamily: 'Lexend Deca',
              )),
        ),
      ],
    );
  }
}
