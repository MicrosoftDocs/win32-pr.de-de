---
title: Ipropertyfiltercollection GetItem-Eigenschaft (wdssharedidl. h)
description: Gibt einen bestimmten Filter in der Auflistung zurück.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- GetItem-Eigenschaft Legacy Windows-Umgebungs Features
- GetItem-Eigenschaft Legacy Windows-Umgebungs Funktionen, ipropertyfiltercollection-Schnittstelle
- Ipropertyfiltercollection-Schnittstelle Legacy Windows-Umgebungs Features, GetItem-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949727"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>Ipropertyfiltercollection:: GetItem-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Gibt einen bestimmten Filter in der Auflistung zurück.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die Adresse des Filters fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





