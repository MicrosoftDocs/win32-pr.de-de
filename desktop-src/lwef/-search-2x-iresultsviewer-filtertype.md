---
title: IResultsViewer FilterType-Eigenschaft (WdsView.h)
description: Diese Eigenschaft legt den Namen des vordefinierten Typs fest oder gibt diesen zurück, nach dem die Ergebnisse gefiltert werden sollen.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- FilterType-Eigenschaft Legacy Windows-Umgebungsfeatures
- FilterType-Eigenschaft Legacy Windows Umgebungsfeatures, IResultsViewer-Schnittstelle
- IResultsViewer-Schnittstelle Legacy Windows Umgebungsfeatures, FilterType-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8f4e71a469ad68431721d99343b43b28ea0f0a82b7e393f5c402b0d88735db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754306"
---
# <a name="iresultsviewerfiltertype-property"></a>IResultsViewer::FilterType-Eigenschaft

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft legt den Namen des vordefinierten Typs fest oder gibt diesen zurück, nach dem die Ergebnisse gefiltert werden sollen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt den wahrgenommenen Typ fest, der zum Filtern von Ergebnissen verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





