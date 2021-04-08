---
title: Die type_UserFree-Funktion
description: Die Type \_ userfree-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727441"
---
# <a name="the-type_userfree-function"></a>Die Type \_ userfree-Funktion

Die **<type> \_ userfree** -Funktion ist eine Hilfsfunktion für die Attribute " \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) " \] und " \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) " \] . Diese Funktion wird von den Stubdateien aufgerufen, um die Daten auf der Serverseite freizugeben. Die-Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

Der <type> im Funktionsnamen bedeutet, dass der userm-Typ in der Typdefinition für den **\[ Wire \_ Marshal \]** oder den **\[ Benutzer- \_ Marshal \]** angegeben ist.

Der *pflags* -Parameter ist ein Zeiger auf ein Feld **ohne** Vorzeichen. Das obere Wort des Flags enthält von OSF-DCE für Gleit Komma-, Byte Reihenfolge-und Zeichen Darstellungen definierte Daten der Datendarstellung von NDR-Daten. Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert. Das genaue Layout der Flags innerhalb des Felds wird in [der Type \_ usersize-Funktion](the-type-usersize-function.md)beschrieben.

Der *pmyobj* -Parameter ist ein Zeiger auf ein Benutzertyp Objekt. Die NDR-Engine gibt das Objekt der obersten Ebene frei. Sie sind dafür verantwortlich, alle Objekte freizugeben, auf die das Objekt der obersten Ebene verweisen kann.

Ausnahmen müssen abgefangen und lokal behandelt werden, Ausnahmen dürfen nicht in der aufzurufenden aufrufsstapel angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 