---
description: Rückruf von Engine zum Behandeln von Fehlern.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipixerrorcallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392470"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span id="vspixengine.ipixerrorcallback"></span>Ipixerrorcallback-Schnittstelle

Rückruf von Engine zum Behandeln von Fehlern.

## <a name="members"></a>Member

Die **ipixerrorcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ipixerrorcallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **ipixerrorcallback** -Schnittstelle verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>Errorlistcallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host von Fehlern benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>Messagescallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host von Meldungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>Warninglistcallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über Warnungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
