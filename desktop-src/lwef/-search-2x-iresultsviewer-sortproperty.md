---
title: Iresultsviewer SortProperty-Eigenschaft (wdsview. h)
description: Diese Eigenschaft legt die indexcolumn der Eigenschaft fest, nach der die Ergebnisse sortiert werden, oder gibt Sie zurück.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- SortProperty-Eigenschaft Legacy-Windows-Umgebungs Features
- SortProperty-Eigenschaft Legacy Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle ältere Windows-Umgebungs Funktionen, SortProperty-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858860"
---
# <a name="iresultsviewersortproperty-property"></a>Iresultviewer:: SortProperty-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Diese Eigenschaft legt die indexcolumn der Eigenschaft fest, nach der die Ergebnisse sortiert werden, oder gibt Sie zurück.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die indexcolumn-Eigenschaft fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Wdsview. h</dt> </dl> |



 

 





