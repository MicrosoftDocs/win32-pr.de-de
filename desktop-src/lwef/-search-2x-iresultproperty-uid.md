---
title: IResultProperty-UID-Eigenschaft (WdsSharedIDL.h)
description: Eindeutiger Bezeichner für die Eigenschaft.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- UID-Eigenschaft Legacy-Windows-Umgebungsfeatures
- UID-Eigenschaft Legacy Windows Umgebungsfeatures, IResultProperty-Schnittstelle
- IResultProperty-Schnittstelle Legacy Windows Umgebungsfeatures, UID-Eigenschaft
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
ms.openlocfilehash: d413a81d6b18091d2e21b4572f5f8e01693829c17942d3e395e2c03a71d467d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754718"
---
# <a name="iresultpropertyuid-property"></a>IResultProperty::UID-Eigenschaft

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Eindeutiger Bezeichner für die Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Eigenschaftswert

gibt einen Zeiger auf den eindeutigen Eigenschaftenbezeichner zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





