---
description: Erweiterungen der ursprünglichen IPixEngine-Schnittstelle.
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e075859bd8fdf6607ef0b66c3a571fa865e52e40
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786716"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span id="vspixengine.ipixengine2"></span>IPixEngine2-Schnittstelle

Erweiterungen der ursprünglichen IPixEngine-Schnittstelle.

## <a name="members"></a>Members

Die **IPixEngine2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixEngine2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPixEngine2-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Methode</th><th >BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></td><td ><p>Beendet die Auslösung und schließt das Grafikprotokoll ab.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></td><td ><p>Ruft Informationen zum aktuellen Wiedergabecomputer ab.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></td><td ><p>Fordert an, anzugeben, dass das Grafikprotokoll neue Daten darin hat.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></td><td ><p>Legt den aktuellen Wiedergabecomputer für das angegebene Grafikprotokoll fest.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
