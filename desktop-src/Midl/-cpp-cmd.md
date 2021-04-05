---
title: /cpp_cmd Schalter
description: Der/cpp- \_ cmd-Schalter gibt den Präprozessor an, den der Mittell-Compiler verwendet, um Eingabedateien vorzuverarbeiten.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718696"
---
# <a name="cpp_cmd-switch"></a>/cpp- \_ cmd-Schalter

Der **/cpp- \_ cmd** -Schalter gibt den Präprozessor an, den der Mittell-Compiler verwendet, um Eingabedateien vorzuverarbeiten.

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*C- \_ \_ präprozessorbinär Datei* 
</dt> <dd>

Gibt den Befehl an, der den Präprozessor aufruft. Dieser Befehl ermöglicht es Entwicklern, den standardpräprozessor zu überschreiben. Standardmäßig ruft die Mittel l den Microsoft C/C++-Compiler aus der Buildumgebung des Buildcomputers auf.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das *\_ \_ binäre C-präprozessorargument* für den Switch kann den vollständigen Pfad angeben. das exe-Suffix und die Anführungszeichen sind optional. In der Regel verwenden Entwickler den-Schalter, um eine bestimmte Version des Microsoft C/C++-präprozessorprozesses oder einer entsprechenden Version in der Buildumgebung auszuwählen. In diesem Fall ist es nicht erforderlich, den Schalter " [**/cpp \_ opt**](-cpp-opt.md) " mit **/cpp \_ cmd** zu verwenden.

Wenn ein nicht-Microsoft-Präprozessor verwendet wird, insbesondere wenn der angegebene Präprozessor seine Ausgabe nicht an stdout weiterleitet, muss der C-Compilerschalter, der die Ausgabe an stdout umleitet, als Teil des Mittell-Compilers [**/cpp \_ opt**](-cpp-opt.md) -Schalter angegeben werden. Weitere Informationen finden Sie unter [C-präprozessoranforderungen für die mittlere](c-preprocessor-requirements-for-midl.md)

Der Präprozessor wird durch eine Befehls Zeichenfolge aufgerufen, die aus den Informationen besteht, die von den **/cpp \_ cmd**-, [**/cpp \_ opt**](-cpp-opt.md)- [**,/D**](-d.md)-, [**/I**](-i.md)-und [**/U**](-u.md) -Switches an den Mittelwert des compl-Compilers In der folgenden Tabelle wird zusammengefasst, wie die Befehls Zeichenfolge für jede Kombination aus **/cpp- \_ cmd** -und **/cpp- \_ opt** -Switches

Wenn der **/cpp- \_ cmd** -Schalter nicht angegeben ist, ruft der kompil-Compiler den Microsoft C/C++-Compiler auf. In der Buildumgebung wird von der mittleren l eine Cl.exe Binärdatei verwendet.

Wenn der Schalter " [**/cpp \_ opt**](-cpp-opt.md) " nicht vorhanden ist, verkettet der Mittell-Compiler die durch den **/cpp- \_ cmd** -Schalter angegebene Zeichenfolge mit den Informationen, die von den Optionen für die mittlere [**/I**](-i.md), [**/D**](-d.md) und [**/U**](-u.md) angegeben werden. Die Zeichenfolge/E wird auch mit der Aufruf Zeichenfolge für den c-Compiler verkettet, um anzugeben, dass der c/C++-Compiler nur die Vorverarbeitung durchführen soll. Der Schalter [**/nologo**](-nologo.md) wird hinzugefügt, um das C/C++-compilerbanner zu unterdrücken. Der mittlerer l-Compiler verwendet die verketteten Zeichenfolge, um den C-Präprozessor für IDL auf oberster Ebene sowie importierte IDL-Dateien und auch für alle vorhandenen, entsprechenden ACF-Dateien aufzurufen.

Wenn der Schalter " [**/cpp \_ opt**](-cpp-opt.md) " vorhanden ist, was für die aktuellen 32-Bit-und 64-Bit-Plattformen in seltenen Fällen der Fall sein sollte, verkettet der Mittelwert Compiler die durch den Schalter " **/cpp \_ cmd** " angegebene Zeichenfolge mit der durch den **/cpp- \_ opt** -Schalter angegebenen Zeichenfolge. Der mittlerer l-Compiler verwendet die verketteten Zeichenfolge, um die festgestellte präprozessorbinär Datei anstelle des standardpräprozessors aufzurufen. Wenn der **Schalter/cpp \_ opt** vorhanden ist, werden weder die von den Switches [**/I**](-i.md), [**/D**](-d.md)und [**/U**](-u.md) angegebenen Mittelwert-Compileroptionen noch der C-Compilerschalter/E mit der Zeichenfolge verkettet. Sie müssen die/E-Option oder eine entsprechende Option als Teil der Zeichenfolge angeben.



| /cpp \_ cmd vorhanden? | /cpp \_ opt vorhanden? | BESCHREIBUNG                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nein (Standard)       | Nein (Standard)       | Ruft den Microsoft C/C++-Standard Compiler mit Einstellungen auf, die von der Option "mittlere [**/I**](-i.md)", " [**/D**](-d.md) " und " [**/U**](-u.md) " Fügt die präprozessorschalter/E und [**/nologo**](-nologo.md)hinzu. |
| Ja                | Nein                 | Ruft die angegebene präprozessorbinär Datei mit denselben Switches wie oben auf.                                                                                                                                        |
| Nein                 | Ja                | Ruft den Microsoft C-Compiler mit den angegebenen Optionen auf. Verwendet keine Optionen für die Option " [**/I**](-i.md)", " [**/D**](-d.md)" und " [**/U**](-u.md) ". Sie müssen/E als Teil von [**/cpp \_ opt**](-cpp-opt.md)angeben.             |
| Ja                | Ja                | Ruft die angegebene präprozessorbinär Datei mit den angegebenen Optionen auf. Sie müssen Anführungszeichen verwenden.                                                                                                                       |



 

## <a name="examples"></a>Beispiele

**Mittel l/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**

**Mittel l/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**

**Mittel l/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**

**Mittel l/cpp \_ cmd "CL"/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ Opt**](-cpp-opt.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/No \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[C-präprozessoranforderungen für die Mittel l](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




