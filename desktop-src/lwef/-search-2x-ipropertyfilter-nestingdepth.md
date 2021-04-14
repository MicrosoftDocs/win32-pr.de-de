---
title: "' Ipropertyfilter '-Eigenschaft ' nestingtiefe ' (wdssharedidl. h)"
description: Filtert die Tiefe innerhalb eines geschachtelten Satzes von Klammern.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Eigenschaften der Legacy-Windows-Umgebung von nestingtiefe
- Nestingtiefe-Eigenschaft Legacy Windows-Umgebungs Funktionen, ipropertyfilter-Schnittstelle
- Ipropertyfilter Interface Legacy Windows-Umgebungs Features, nestingtiefe (Eigenschaft)
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391885"
---
# <a name="ipropertyfilternestingdepth-property"></a>Ipropertyfilter:: nestingtiefe-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Filtert die Tiefe innerhalb eines geschachtelten Satzes von Klammern.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die Zahl fest, die die Tiefe der geschachtelten Klammern angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





