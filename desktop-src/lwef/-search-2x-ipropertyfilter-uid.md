---
title: Eigenschaft ' ipropertyfilter UID ' (wdssharedidl. h)
description: UID für die Eigenschaft, nach der gefiltert werden soll.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- UID-Eigenschafts Funktionen der Legacy-Windows-Umgebung
- UID-Eigenschaft Legacy-Windows-Umgebungs Features, ipropertyfilter-Schnittstelle
- Ipropertyfilter-Schnittstelle ältere Windows-Umgebungs Features, UID-Eigenschaft
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
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340898"
---
# <a name="ipropertyfilteruid-property"></a>Ipropertyfilter:: UID-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





