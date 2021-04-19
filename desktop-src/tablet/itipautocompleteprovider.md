---
description: Verwaltet die Seite der Anwendung der automatischen vollständigen Integration des Text Eingabe Bereichs.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Itipauescompleteprovider-Schnittstelle (tipauabcomplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355440"
---
# <a name="itipautocompleteprovider-interface"></a>Itipauescompleteprovider-Schnittstelle

Verwaltet die Seite der Anwendung der automatischen vollständigen Integration des Text Eingabe Bereichs.

## <a name="members"></a>Member

Die **itipauescompleteprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itipautocompleteprovider** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itipaudecompleteprovider** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Auftritt**](itipautocompleteprovider-show.md)                           | Hiermit wird die Liste der Auto Vervollständigen angezeigt oder ausgeblendet.<br/>                                                                 |
| [**Updatepzudingtext**](itipautocompleteprovider-updatependingtext.md) | Wird vom Auto Vervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich eingegeben hat.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> <dt>

[**Itipauwebcompleteclient-Schnittstelle**](itipautocompleteclient.md)
</dt> </dl>

 

