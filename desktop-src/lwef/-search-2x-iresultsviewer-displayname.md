---
title: IResultsViewer DisplayName-Eigenschaft (WdsView.h)
description: Lokalisierter Anzeigename des Typs.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- DisplayName-Eigenschaft Legacy Windows-Umgebungsfeatures
- DisplayName-Eigenschaft Legacy Windows Umgebungsfeatures, IResultsViewer-Schnittstelle
- IResultsViewer-Schnittstelle Legacy Windows Umgebungsfeatures, DisplayName-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d3f0c5f7887861d2d757c71a4327ce57af7f39ae3f4811167789c6b4e662ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754395"
---
# <a name="iresultsviewerdisplayname-property"></a>IResultsViewer::D isplayName-Eigenschaft

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Lokalisierter Anzeigename des Typs.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

Zeiger auf einen Wert, der den lokalisierten Anzeigenamen für den Typ empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





