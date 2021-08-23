---
title: IResultProperty IndexColumn-Eigenschaft (WdsSharedIDL.h)
description: Name der Eigenschaftenspalte im Index.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- IndexColumn-Eigenschaft Legacy Windows Umgebungsfeatures
- IndexColumn-Eigenschaft Legacy Windows Umgebungsfeatures, IResultProperty-Schnittstelle
- IResultProperty-Schnittstelle Legacy Windows Environment Features , IndexColumn(Eigenschaft)
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a78d91b9e823dbf8d3c7a2273247706f9ae2bb04c6f64d08f5555eb875023c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754773"
---
# <a name="iresultpropertyindexcolumn-property"></a>IResultProperty::IndexColumn (Eigenschaft)

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Name der Eigenschaftenspalte im Index.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Eigenschaftswert

gibt einen Zeiger auf den Spaltennamen im Index zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





