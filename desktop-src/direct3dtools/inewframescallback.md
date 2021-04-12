---
description: Rückruf von Engine, der angibt, dass die Verarbeitung neuer Frames, die dem Protokoll hinzugefügt wurden, abgeschlossen ist.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Inewframescallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392866"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>Inewframescallback-Schnittstelle

Rückruf von Engine, der angibt, dass die Verarbeitung neuer Frames, die dem Protokoll hinzugefügt wurden, abgeschlossen ist.

## <a name="members"></a>Member

Die **inewframescallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. In " **inewframescallback** " sind auch folgende Typen von Membern verfügbar:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **inewframescallback** -Schnittstelle verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>Abbrechen</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host benachrichtigt, dass alle Anforderungen abgebrochen wurden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>Cancelusingcallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>Cancelusingcookie</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt, indem er ein Cookie verwendet, das die Anforderung eindeutig identifiziert.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>Newframesavailable</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host benachrichtigt, dass neue Frames zur Verarbeitung verfügbar sind.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
