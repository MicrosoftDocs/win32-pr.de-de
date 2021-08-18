---
description: Rückruf von der Engine, um Fehler zu behandeln.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixErrorCallback-Schnittstelle
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
ms.openlocfilehash: 36d28785ad940c3d3af3eb2df58759d7b5820cc7bc50ee65db56932385326aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985860"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback-Schnittstelle

Rückruf von der Engine, um Fehler zu behandeln.

## <a name="members"></a>Member

Die **IPixErrorCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixErrorCallback** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPixErrorCallback-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">Beschreibung</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über Fehler benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host von Nachrichten benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über Warnungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
