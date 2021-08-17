---
title: IPropertyFilterCollection-GetITem-Eigenschaft (WdsSharedIDL.h)
description: Gibt einen bestimmten Filter innerhalb der Auflistung zurück.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- GetITem-Eigenschaft Legacy Windows-Umgebungsfeatures
- GetITem-Eigenschaft Legacy Windows Umgebungsfeatures, IPropertyFilterCollection-Schnittstelle
- IPropertyFilterCollection-Schnittstelle Legacy Windows Umgebungsfeatures, GetITem-Eigenschaft
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
ms.openlocfilehash: 7436e1fe10c26621f3cf4480be7db9710f80906bea18084a2e775e563db4dd8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451082"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>IPropertyFilterCollection::GetITem-Eigenschaft

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Gibt einen bestimmten Filter innerhalb der Auflistung zurück.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





