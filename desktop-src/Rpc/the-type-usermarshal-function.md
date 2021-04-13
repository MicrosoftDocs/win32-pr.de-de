---
title: Die type_UserMarshal-Funktion
description: Die Type \_ usermarshal-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390977"
---
# <a name="the-type_usermarshal-function"></a>Der Typ \_ usermarshal-Funktion

Die **<type> \_ usermarshal** -Funktion ist eine Hilfsfunktion für die Attribute " \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) " \] und " \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) " \] . Diese Funktion wird von den Stubdaten aufgerufen, um Daten auf der Client-oder Serverseite zu Mars Hallen. Die-Funktion ist wie folgt definiert:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

Der <type> im Funktionsnamen bedeutet, dass der userm-Typ in der Typdefinition für den **\[ Wire \_ Marshal \]** oder den **\[ Benutzer- \_ Marshal \]** angegeben ist. Dieser Typ ist möglicherweise nicht transaktierbar oder sogar – bei Verwendung mit dem Attribut " **\[ User \_ Marshal \]** " – ein Typ, der dem Mittelwert Compiler unbekannt ist. Der Name des Wire-Typs (der Name des übertragbaren Typs) wird im Funktionsprototyp nicht verwendet. Beachten Sie jedoch, dass der Wire-Typ das von OSF DCE angegebene Netzwerk Layout für die Daten definiert.

Der *pflags* -Parameter ist ein Zeiger auf ein Feld ohne Vorzeichen. Das obere Wort des Flags enthält von OSF-DCE für Gleit Komma-, Byte Reihenfolge-und Zeichen Darstellungen definierte Daten der Datendarstellung von NDR-Daten. Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert. Das genaue Layout der Flags innerhalb des Felds wird in [der Type \_ usersize-Funktion](the-type-usersize-function.md)beschrieben.

Der *pbuffer* -Parameter ist der aktuelle Puffer Zeiger. Dieser Zeiger kann beim Eintrag nicht ausgerichtet werden. Die **<type> \_ usermarshal** -Funktion sollte den Puffer Zeiger entsprechend ausrichten, die Daten Mars Hallen und die neue Puffer Position zurückgeben. dabei handelt es sich um die Adresse des ersten Bytes nach dem gemarshallten Objekt. Beachten Sie, dass die Wire Type-Spezifikation das tatsächliche Layout der Daten im Puffer bestimmt.

Der *pmyobj* -Parameter ist ein Zeiger auf ein Benutzertyp Objekt.

Der Rückgabewert ist die neue Puffer Position, bei der es sich um die Adresse des ersten Bytes nach dem nicht gemarshallten Objekt handelt.

Ein Pufferüberlauf kann auftreten, wenn Sie die Größe der Daten falsch berechnen und versuchen, mehr Daten als erwartet zu Mars Hallen. Sie sollten darauf achten, diese Situation zu vermeiden. Sie können dies überprüfen, indem Sie den Zeiger verwenden, den **<type> \_ usermarshal** zurückgibt. Andernfalls riskieren Sie, dass die NDR-Engine später eine Pufferüberlauf Ausnahme auslöst.

Ausnahmen müssen abgefangen und lokal behandelt werden, Ausnahmen dürfen nicht in der aufzurufenden aufrufsstapel angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 