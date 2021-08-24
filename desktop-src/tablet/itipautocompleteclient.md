---
description: Ermöglicht dem Client das Aufrufen des Anbieterobjekts für den automatischen Abschluss des Texteingabebereichs der Anwendung.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: ITipAutocompleteClient-Schnittstelle (TipAutoComplete.h)
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
ms.openlocfilehash: dac9b1a6c581be8a8fb19df4f812a5866403d949d19739bb8ae99a0fffbe5e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590290"
---
# <a name="itipautocompleteclient-interface"></a>ITipAutocompleteClient-Schnittstelle

Ermöglicht dem Client das Aufrufen des Anbieterobjekts für den automatischen Abschluss des Texteingabebereichs der Anwendung.

## <a name="members"></a>Member

Die **ITipAutocompleteClient-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteClient** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITipAutocompleteClient-Schnittstelle** verfügt über diese Methoden.



| Methode                                                              | Beschreibung                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | Registriert den Anbieter beim Client, damit der Client das Automatische Vervollstehungsanbieterobjekt der Anwendung aufrufen kann.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Ermöglicht dem Client, zu empfehlen, wo die Liste der automatischen Vervollstehungen positioniert werden soll, um eine Überlappung des Eingabebereichs zu vermeiden.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Bestimmt, ob der Eingabebereich bereit ist, damit die Liste der automatischen Vervollstehung angezeigt wird.<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | Aufheben der Registrierung des zugeordneten Anbieters.<br/>                                                                                                                      |
| [**UserSelection**](itipautocompleteclient-userselection.md)       | Benachrichtigt den Eingabebereich, dass der Benutzer etwas in der Liste der automatischen Vervollstehungen ausgewählt hat und den gesamten verbleibenden Text verwirft, der noch nicht eingefügt wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (erfordert auch Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

