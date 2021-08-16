---
title: IResultProperty DisplayName-Eigenschaft (WdsSharedIDL.h)
description: Lokalisierter Anzeigename der Eigenschaft.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- DisplayName-Eigenschaft Legacy Windows-Umgebungsfeatures
- DisplayName-Eigenschaft Legacy Windows Umgebungsfeatures, IResultProperty-Schnittstelle
- IResultProperty-Schnittstelle Legacy Windows Umgebungsfeatures, DisplayName-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e15eedcafffbae25b2671b02aaac8fd1e64b625edfea3e040ed2c6067ca953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755162"
---
# <a name="iresultpropertydisplayname-property"></a>IResultProperty::D isplayName-Eigenschaft

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Lokalisierter Anzeigename der Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

gibt einen Zeiger auf den lokalisierten Anzeigenamen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





