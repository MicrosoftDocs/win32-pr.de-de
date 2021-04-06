---
title: Iresulttype preceivedtype-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Preceivedtype-Eigenschaft Legacy-Windows-Umgebungs Features
- Preceivedtype-Eigenschaft Legacy Windows-Umgebungs Features, iresulttype-Schnittstelle
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Features, preceivedtype (Eigenschaft)
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858794"
---
# <a name="iresulttypepreceivedtype-property"></a>Iresulttype::P receivedtype-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die Adresse der Zeichenfolge identifyint des Typs im Index zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





