---
title: Die type_UserUnmarshal-Funktion
description: Die UserUnmarshal-Funktion vom Typ ist eine Hilfsfunktion für die Attribute \_ \wire \_ marshal\ und \ user \_ marshal\.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9d894b2658de9dc4559cfbef2ad1db2c4e79b0b9313754c4edafbd2c32fc2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016450"
---
# <a name="the-type_userunmarshal-function"></a>Der Typ \_ UserUnmarshal-Funktion

Die **<type> \_ UserUnmarshal-Funktion** ist eine Hilfsfunktion für die Attribute \[ ["wire \_ marshal"](/windows/desktop/Midl/wire-marshal) \] und \[ ["user \_ marshal".](/windows/desktop/Midl/user-marshal) \] Die Stubs rufen diese Funktion auf, um die Daten auf client- oder serverseitiger Seite zu entmarshalieren. Die Funktion ist wie die folgenden definiert:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

Der <type> im Funktionsnamen steht für den userm-Typ, der in der **\[ Wire \_ \] Marshal-** oder User **\[ \_ \] Marshal-Typdefinition** angegeben ist. Dieser Typ kann nicht übersetzt werden oder sogar – bei Verwendung mit dem **\[ \_ \] Benutzer-Marshallattribut** – für den MIDL-Compiler unbekannt sein. Der Name des Kabeltyps (der Name des transmissiblen Typs) wird im Funktionsprototyp nicht verwendet. Beachten Sie jedoch, dass der Wire-Typ das Kabellayout für die Daten definiert, wie von OSF DCE angegeben.

Der *pFlags-Parameter* ist ein Zeiger auf ein Feld mit langen **Flags ohne** Vorzeichen. Das obere Wort des Flags enthält NDR-Datendarstellungsflags, wie von OSF DCE für Gleitkomma-, Byte- und Zeichendarstellungen definiert. Das untere Wort enthält ein Marshallingkontextflag, wie vom COM-Kanal definiert. Das genaue Layout der Flags innerhalb des Felds wird unter [Der Typ \_ UserSize-Funktion beschrieben.](the-type-usersize-function.md)

Der *pBuffer-Parameter* ist der aktuelle Pufferzeiger. Dieser Zeiger kann beim Eintrag ausgerichtet sein oder nicht. Ihre **<type> \_ UserUnmarshal-Funktion** sollte den Pufferzeiger entsprechend ausrichten, die Daten entmarshalieren und die neue Pufferposition zurückgeben, die die Adresse des ersten Byte nach dem nichtmarshalierten Objekt ist.

Der *pMyObj-Parameter* ist ein Zeiger auf ein benutzerdefiniertes Typobjekt.

In einer heterogenen Umgebung führt die NDR-Engine alle erforderlichen Datenkonvertierungen aus, bevor die **<type> \_ UserUnmarshal-Funktion aufruft.** Beachten Sie, dass die NDR-Engine diese Datenkonvertierung gemäß der wire-type-Definition für diesen Benutzerdatentyp vorträgt. Das Flag gibt die Datendarstellung des Absenders an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Marshallingregeln für das \_ Marshallen von Benutzer und das Marshallen von \_ Wire](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_Benutzer-Marshalling](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 