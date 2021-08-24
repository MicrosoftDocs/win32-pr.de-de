---
title: IResultsViewer SortOrderProperty-Eigenschaft (WdsView.h)
description: Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach der Ergebnisse sortiert werden sollen, oder gibt sie zurück.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- SortOrderProperty-Eigenschaft Legacy Windows Umgebungsfeatures
- SortOrderProperty-Eigenschaft Legacy Windows Umgebungsfeatures, IResultsViewer-Schnittstelle
- IResultsViewer-Schnittstelle Legacy Windows Umgebungsfeatures, SortOrderProperty-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01680ac46592887cf4f321b771ff0e46039c775c4e9e9d8ed1edbc893ab45977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829170"
---
# <a name="iresultsviewersortorderproperty-property"></a>IResultsViewer::SortOrderProperty-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach der Ergebnisse sortiert werden sollen, oder gibt sie zurück.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die [**ColumnSortOrder-Eigenschaft**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





