---
title: IResultsViewer ItemStore-Eigenschaft (WdsView.h)
description: Diese Eigenschaft wird den Namen des Speichers festlegen oder zurückgeben, nach dem Die Ergebnisse gefiltert werden sollen.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- ItemStore-Eigenschaft Legacy Windows Umgebungsfeatures
- ItemStore-Eigenschaft Legacy Windows Umgebungsfeatures, IResultsViewer-Schnittstelle
- IResultsViewer-Schnittstelle Legacy Windows Umgebungsfeatures, ItemStore-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21db485f8bfeb52ac413a2886f5624345e9812f2a0086b143f9a10942f7aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753901"
---
# <a name="iresultsvieweritemstore-property"></a>IResultsViewer::ItemStore-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft wird den Namen des Speichers festlegen oder zurückgeben, nach dem Die Ergebnisse gefiltert werden sollen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die Namen des Speichers fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





