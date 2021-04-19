---
description: Ermöglicht dem Client, das Auto Vervollständigen-Anbieter Objekt der Anwendung für den Text Eingabebereich aufzurufen.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Itipautcompleteclient-Schnittstelle (tipauabcomplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362725"
---
# <a name="itipautocompleteclient-interface"></a>Itipauwebcompleteclient-Schnittstelle

Ermöglicht dem Client, das Auto Vervollständigen-Anbieter Objekt der Anwendung für den Text Eingabebereich aufzurufen.

## <a name="members"></a>Member

Die **itipautecompleteclient** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itipautocompleteclient** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itipaudecompleteclient** -Schnittstelle verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adviseprovider**](itipautocompleteclient-adviseprovider.md)     | Registriert den Anbieter beim Client, damit der Client das Auto Vervollständigen-Anbieter Objekt der Anwendung abrufen kann.<br/>                                      |
| [**Preferredrects**](itipautocompleteclient-preferredrects.md)     | Ermöglicht dem Client, vorzuschlagen, wo die Auto Vervollständigen-Liste positioniert werden soll, um die überlappenden Eingabebereich zu vermeiden.<br/>                                               |
| [**Requestshowui**](itipautocompleteclient-requestshowui.md)       | Bestimmt, ob der Eingabebereich bereit ist, die Auto Vervollständigen-Liste angezeigt zu haben.<br/>                                                                             |
| [**Unadviseprovider**](itipautocompleteclient-unadviseprovider.md) | Hebt die Registrierung des zugeordneten Anbieters auf.<br/>                                                                                                                      |
| [**Userselection**](itipautocompleteclient-userselection.md)       | Benachrichtigt den Eingabebereich, dass der Benutzer etwas in der Liste Auto vervollständigen ausgewählt und den verbleibenden Text verworfen hat, der noch nicht eingefügt wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

