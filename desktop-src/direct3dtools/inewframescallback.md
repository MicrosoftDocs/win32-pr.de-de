---
description: Rückruf von der Engine, der angibt, dass die Analyse neuer Frames erfolgt ist, die dem Protokoll hinzugefügt wurden.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback-Schnittstelle
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
ms.openlocfilehash: 8f9d47e84cf4deeebafa6592853f73e86d8339f8
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787316"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>INewFramesCallback-Schnittstelle

Rückruf von der Engine, der angibt, dass die Analyse neuer Frames erfolgt ist, die dem Protokoll hinzugefügt wurden.

## <a name="members"></a>Members

Die **INewFramesCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INewFramesCallback** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **INewFramesCallback-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Methode</th><th >BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></td><td ><p>Ein Rückruf, der den Host benachrichtigt, dass alle Anforderungen abgebrochen wurden.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></td><td ><p>Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></td><td ><p>Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt, indem ein Cookie verwendet wird, das die Anforderung eindeutig identifiziert.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></td><td ><p>Ein Rückruf, der den Host benachrichtigt, dass neue Frames für die Verarbeitung verfügbar sind.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
