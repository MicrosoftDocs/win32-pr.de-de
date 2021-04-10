---
title: Die type_UserUnmarshal-Funktion
description: Der Typ \_ userunmarshal-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039565"
---
# <a name="the-type_userunmarshal-function"></a>Der Typ \_ userunmarshal-Funktion

Die **<type> \_ userunmarshal** -Funktion ist eine Hilfsfunktion für das \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] -Attribut und das \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) - \] Attribut. Diese Funktion wird von den Stubdateien aufgerufen, um die Daten auf Client-oder Serverseite zu Mars Hallen. Die-Funktion ist wie folgt definiert:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

Der <type> im Funktionsnamen bedeutet, dass der userm-Typ in der Typdefinition für den **\[ Wire \_ Marshal \]** oder den **\[ Benutzer- \_ Marshal \]** angegeben ist. Dieser Typ kann nicht transaktierbar oder sogar – sein, wenn er mit dem Attribut " **\[ User \_ Marshal \]** " verwendet wird – unbekannt für den mittlerer l-Compiler. Der Name des Wire-Typs (der Name des übertragbaren Typs) wird im Funktionsprototyp nicht verwendet. Beachten Sie jedoch, dass der Wire-Typ das von OSF DCE angegebene Netzwerk Layout für die Daten definiert.

Der *pflags* -Parameter ist ein Zeiger auf ein Feld **ohne** Vorzeichen. Das obere Wort des Flags enthält von OSF-DCE für Gleit Komma-, Byte Reihenfolge-und Zeichen Darstellungen definierte Daten der Datendarstellung von NDR-Daten. Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert. Das genaue Layout der Flags innerhalb des Felds wird in [der Type \_ usersize-Funktion](the-type-usersize-function.md)beschrieben.

Der *pbuffer* -Parameter ist der aktuelle Puffer Zeiger. Dieser Zeiger kann beim Eintrag nicht ausgerichtet werden. Ihre **<type> \_ userunmarshal** -Funktion sollte den Puffer Zeiger entsprechend ausrichten, das Mars Hallen der Daten rückgängig macht und die neue Puffer Position zurückgeben. Dies ist die Adresse des ersten Bytes nach dem nicht gemarshallten Objekt.

Der *pmyobj* -Parameter ist ein Zeiger auf ein benutzerdefiniertes Typobjekt.

In einer heterogenen Umgebung führt die NDR-Engine jede erforderliche Datenkonvertierung aus, bevor die **<type> \_ userunmarshal** -Funktion aufgerufen wird. Beachten Sie, dass die NDR-Engine diese Datenkonvertierung gemäß der für diesen Benutzer Datentyp angegebenen Typdefinition ausführt. Das-Flag gibt die Datendarstellung des Absenders an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 