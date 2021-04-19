---
title: Iresultproperty DataType-Eigenschaft (wdssharedidl. h)
description: Ein Properties-Datentyp.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- DataType-Eigenschaft Legacy-Windows-Umgebungs Features
- DataType-Eigenschaft Legacy-Windows-Umgebungs Funktionen, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Features, DataType-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d887642594ed5ac7f78de1d4eac76fb4709f0dfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345906"
---
# <a name="iresultpropertydatatype-property"></a>Iresultproperty::D atatype-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Ein Properties-Datentyp.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt einen Zeiger auf den Properties-Datentyp zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





