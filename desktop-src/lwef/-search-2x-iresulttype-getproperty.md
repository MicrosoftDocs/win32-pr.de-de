---
title: IResultType GetProperty-Eigenschaft (WdsSharedIDL.h)
description: Diese Eigenschaft enthält angegebene Eigenschafteninformationen.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- GetProperty-Eigenschaft Legacy Windows-Umgebungsfeatures
- GetProperty-Eigenschaft Legacy Windows Umgebungsfeatures, IResultType-Schnittstelle
- IResultType-Schnittstelle Legacy Windows Umgebungsfeatures, GetProperty-Eigenschaft
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f35a0f2bce8fb4e098a2452b6d5575fa9843283562f7f1d051b588d9a0c8cd05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481104"
---
# <a name="iresulttypegetproperty-property"></a>IResultType::GetProperty-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft enthält angegebene Eigenschafteninformationen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die Adresse der angegebenen Eigenschafteninformationen fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





