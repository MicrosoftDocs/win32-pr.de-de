---
title: IResultsViewer SortOrderProperty-Eigenschaft (WdsView.h)
description: Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach denen die Ergebnisse sortiert werden, oder gibt Sie zurück.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Sortoriderproperty-Eigenschaft Legacy-Windows-Umgebungs Features
- Sortor Property-Eigenschaft Legacy-Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle Legacy-Windows-Umgebungs Features, sortoriderproperty (Eigenschaft)
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
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338146"
---
# <a name="iresultsviewersortorderproperty-property"></a>Iresultviewer:: sortor Name Property (Eigenschaft)

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach denen die Ergebnisse sortiert werden, oder gibt Sie zurück.

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

Legt die [**columnsortor der**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) -Eigenschaft fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Wdsview. h</dt> </dl> |



 

 





