---
title: Iresultsviewer-FilterType-Eigenschaft (wdsview. h)
description: Diese Eigenschaft legt den Namen des vorab bereitgestellten Typs fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- FilterType-Eigenschaft Legacy-Windows-Umgebungs Features
- FilterType-Eigenschaft Legacy-Windows-Umgebungs Funktionen, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle ältere Windows-Umgebungs Features, FilterType-Eigenschaft
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
ms.openlocfilehash: 890d0ceadddb9f3b46ee8b45f109a389472be218
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345337"
---
# <a name="iresultsviewerfiltertype-property"></a>Iresultviewer:: FilterType (Eigenschaft)

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Diese Eigenschaft legt den Namen des vorab bereitgestellten Typs fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.

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

Legt den wahrgenommenen Typ fest, mit dem die Ergebnisse gefiltert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Wdsview. h</dt> </dl> |



 

 





