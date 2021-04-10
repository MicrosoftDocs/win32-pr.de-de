---
title: Iresultproperty Uid-Eigenschaft (wdssharedidl. h)
description: Eindeutiger Bezeichner für die Eigenschaft.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- UID-Eigenschafts Funktionen der Legacy-Windows-Umgebung
- UID-Eigenschaft Legacy-Windows-Umgebungs Funktionen, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Features, UID-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040463"
---
# <a name="iresultpropertyuid-property"></a>Iresultproperty:: UID-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Eindeutiger Bezeichner für die Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt einen Zeiger auf den eindeutigen Bezeichner der Eigenschaft zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





