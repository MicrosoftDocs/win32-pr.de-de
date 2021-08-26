---
title: Die type_UserMarshal-Funktion
description: Die UserMarshal-Funktion vom Typ ist eine Hilfsfunktion für die Attribute \_ \wire \_ marshal\ und \user \_ marshal\.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffea134b78ae8187fce3fab7876150c0a7a8cd7f892ebac602966712ec1b60e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016470"
---
# <a name="the-type_usermarshal-function"></a>Der Typ \_ UserMarshal-Funktion

Die **<type> \_ UserMarshal-Funktion** ist eine Hilfsfunktion für die Attribute \[ ["wire \_ marshal"](/windows/desktop/Midl/wire-marshal) \] und \[ ["user \_ marshal".](/windows/desktop/Midl/user-marshal) \] Die Stubs rufen diese Funktion auf, um Daten auf Client- oder Serverseite zu marshallen. Die Funktion ist wie die folgenden definiert:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

Der <type> im Funktionsnamen steht für den userm-Typ, der in der **\[ Wire \_ \] Marshal-** oder User **\[ \_ \] Marshal-Typdefinition** angegeben ist. Dieser Typ kann nicht übersetzt werden oder sogar – bei Verwendung mit dem **\[ Benutzer-Marshallattribut \_ \]** – ein Typ sein, der dem MIDL-Compiler unbekannt ist. Der Name des Kabeltyps (der Name des transmissiblen Typs) wird im Funktionsprototyp nicht verwendet. Beachten Sie jedoch, dass der Wire-Typ das Kabellayout für die Daten definiert, wie von OSF DCE angegeben.

Der *pFlags-Parameter* ist ein Zeiger auf ein Feld mit langen Flags ohne Vorzeichen. Das obere Wort des Flags enthält NDR-Datendarstellungsflags, wie von OSF DCE für Gleitkomma-, Byte- und Zeichendarstellungen definiert. Das untere Wort enthält ein Marshallingkontextflag, wie vom COM-Kanal definiert. Das genaue Layout der Flags innerhalb des Felds wird unter [Der Typ \_ UserSize-Funktion beschrieben.](the-type-usersize-function.md)

Der *pBuffer-Parameter* ist der aktuelle Pufferzeiger. Dieser Zeiger kann beim Eintrag ausgerichtet sein oder nicht. Ihre **<type> \_ UserMarshal-Funktion** sollte den Pufferzeiger entsprechend ausrichten, die Daten marshallen und die neue Pufferposition zurückgeben, die die Adresse des ersten Byte nach dem gemarshallten Objekt ist. Beachten Sie, dass die Wire Type Specification das tatsächliche Layout der Daten im Puffer bestimmt.

Der *pMyObj-Parameter* ist ein Zeiger auf ein Benutzertypobjekt.

Der Rückgabewert ist die neue Pufferposition, die die Adresse des ersten Byte nach dem nichtmarshalierten Objekt ist.

Pufferüberlauf kann auftreten, wenn Sie die Größe der Daten falsch berechnen und versuchen, mehr Daten als erwartet zu marshallen. Achten Sie darauf, diese Situation zu vermeiden. Sie können dies mithilfe des Zeigers überprüfen, den **<type> \_ UserMarshal** zurückgibt. Andernfalls besteht die Gefahr, dass die NDR-Engine später eine Pufferüberlaufausnahme auslöst.

Ausnahmen müssen lokal erfasst und behandelt werden. Ausnahmen dürfen nicht die Aufrufliste nach oben propagiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Marshallingregeln für das \_ Marshallen von Benutzer und das Marshallen von \_ Wire](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_Benutzer-Marshalling](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 