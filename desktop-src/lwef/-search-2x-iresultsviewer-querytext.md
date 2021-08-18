---
title: IResultsViewer QueryText-Eigenschaft (WdsView.h)
description: Ruft den aktuellen Abfragetext ab oder legt den Text fest.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- QueryText-Eigenschaft Legacy Windows-Umgebungsfeatures
- QueryText-Eigenschaft Legacy Windows Umgebungsfeatures, IResultsViewer-Schnittstelle
- IResultsViewer-Schnittstelle Legacy Windows Umgebungsfeatures, QueryText-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5522419d14bf27a1e836c9caa16e9dabf5a122e4566fd19c868a1f72e3f61d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753585"
---
# <a name="iresultsviewerquerytext-property"></a>IResultsViewer::QueryText-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Ruft den aktuellen Abfragetext ab oder legt den Text fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt den aktuellen Abfragetext fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





