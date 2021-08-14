---
title: IPropertyFilterCollection-AddItem-Eigenschaft (WdsSharedIDL.h)
description: Fügt der Auflistung einen neuen Filter hinzu.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- AddItem-Eigenschaft Legacy Windows-Umgebungsfeatures
- AddItem-Eigenschaft Legacy Windows Umgebungsfeatures , IPropertyFilterCollection-Schnittstelle
- IPropertyFilterCollection-Schnittstelle Legacy Windows Umgebungsfeatures, AddItem-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeafec95549fefa244dff6ff44ad9110150ae1b410e38b423a0a31f09cf54194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755447"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>IPropertyFilterCollection::AddItem-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Fügt der Auflistung einen neuen Filter hinzu.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Eigenschaftswert

gibt einen Zeiger auf die Adresse für den neuen Filter zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





