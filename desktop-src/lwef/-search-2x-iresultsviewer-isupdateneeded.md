---
title: IResultsViewer IsUpdateNeeded-Eigenschaft (WdsView.h)
description: Dadurch wird TRUE zurückgegeben, wenn die Sichtabfrage geändert wurde und aktualisiert werden muss.
ms.assetid: 68ae1f68-0585-4bc5-bea4-eb55f3626093
keywords:
- IsUpdateNeeded-Eigenschaft Legacy Windows Umgebungsfeatures
- IsUpdateNeeded-Eigenschaft Legacy Windows Umgebungsfeatures, IResultsViewer-Schnittstelle
- IResultsViewer-Schnittstelle Legacy Windows Environment Features , IsUpdateNeeded-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.IsUpdateNeeded
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c013692509ddebe5c0f6530e9abf4b17aa2c356c6eade829bdc2dbad52465f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753881"
---
# <a name="iresultsviewerisupdateneeded-property"></a>IResultsViewer::IsUpdateNeeded -Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Dadurch wird TRUE zurückgegeben, wenn die Sichtabfrage geändert wurde und aktualisiert werden muss.

## <a name="syntax"></a>Syntax

## <a name="property-value"></a>Eigenschaftswert

Wenn aufgerufen wird, wird ein Zeiger auf das Flag zurückgegeben, das darauf hinweist, dass sich die Abfrage geändert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                        |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





