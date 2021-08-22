---
title: IPropertyFilterCollection RemoveItem-Eigenschaft (WdsSharedIDL.h)
description: Entfernt einen bestimmten Filter aus der Auflistung.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- RemoveItem-Eigenschaft Legacy Windows Umgebungsfeatures
- RemoveItem-Eigenschaft Legacy Windows Environment Features , IPropertyFilterCollection-Schnittstelle
- IPropertyFilterCollection-Schnittstelle Legacy Windows Environment Features , RemoveItem-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54822e95e2ea7d6e10fdd5bbf833adb63b51cb01e8d860ce77f550432b41e926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755419"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>IPropertyFilterCollection::RemoveItem (Eigenschaft)

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Entfernt einen bestimmten Filter aus der Auflistung.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a>Eigenschaftswert

Akzeptiert einen Zeiger auf den Index, damit der Filter entfernt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





