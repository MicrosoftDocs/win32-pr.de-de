---
description: Verwaltet die Anwendungsseite der automatischen Integration des Texteingabebereichs.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: ITipAutocompleteProvider-Schnittstelle (TipAutoComplete.h)
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
ms.openlocfilehash: 66c1e38c419e7eb37745864b447249d55b384b6c832293bd3fab4d0cc171e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031868"
---
# <a name="itipautocompleteprovider-interface"></a>ITipAutocompleteProvider-Schnittstelle

Verwaltet die Anwendungsseite der automatischen Integration des Texteingabebereichs.

## <a name="members"></a>Member

Die **ITipAutocompleteProvider-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteProvider** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITipAutocompleteProvider-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | Beschreibung                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Zeigen**](itipautocompleteprovider-show.md)                           | Zeigt die Liste der automatischen Vervollstehungen an oder blendet sie aus.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Wird vom AutoVervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich eingegeben hat.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (erfordert auch Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> <dt>

[**ITipAutocompleteClient-Schnittstelle**](itipautocompleteclient.md)
</dt> </dl>

 

