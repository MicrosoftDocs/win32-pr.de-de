---
title: IPropertyFilter UID-Eigenschaft (WdsSharedIDL.h)
description: UID für die Eigenschaft, nach der gefiltert werden soll.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- UID-Eigenschaft Legacy Windows Umgebungsfeatures
- UID-Eigenschaft Legacy Windows Umgebungsfeatures, IPropertyFilter-Schnittstelle
- IPropertyFilter-Schnittstelle Legacy Windows Umgebungsfeatures, UID-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0e96fc2c207a3dc7e11d751cb2e545f6d917036b3ce8f184280807c71f55e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963780"
---
# <a name="ipropertyfilteruid-property"></a>IPropertyFilter::UID-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

UID für die Eigenschaft, nach der gefiltert werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die UID-Eigenschaft fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





