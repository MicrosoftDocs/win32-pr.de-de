---
title: IResultType PropertyCount-Eigenschaft (WdsSharedIDL.h)
description: Diese Eigenschaft enthält die Anzahl der Eigenschaften, die vom Typ verfügbar gemacht werden.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- PropertyCount-Eigenschaft Legacy Windows-Umgebungsfeatures
- PropertyCount-Eigenschaft Legacy Windows Umgebungsfeatures, IResultType-Schnittstelle
- IResultType-Schnittstelle Legacy Windows Umgebungsfeatures , PropertyCount-Eigenschaft
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6952f2efb6e0d14be22daf71e352747915b2ba05bf543d764ee9af5f496715ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014630"
---
# <a name="iresulttypepropertycount-property"></a>IResultType::P ropertyCount-Eigenschaft

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft enthält die Anzahl der Eigenschaften, die vom Typ verfügbar gemacht werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Eigenschaftswert

gibt die Adresse der Anzahl der verfügbar gemachten Eigenschaften zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





