---
description: Die folgenden Strukturen werden in vspixengine.h deklariert.
MS-HAID: vspixengine.vspixengine\_structures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Direct3D-Diagnose – Erfassungsschnittstellenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 97F142F6-FED1-4AF4-B9E3-BB1E30F3FAD2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 611a8112c1eb99c142c92f63f598e903352528f8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622286"
---
# <a name="span-idvspixenginevspixengine_structuresspandirect3d-diagnostics-capture-interface-structures"></a><span id="vspixengine.vspixengine_structures"></span>Direct3D-Diagnose – Erfassungsschnittstellenstrukturen

Die folgenden Strukturen werden in vspixengine.h deklariert.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In diesem Abschnitt

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Thema</th><th>Beschreibung</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/resourcepair"><strong>ResourcePair</strong></a></p></td><td><p>Stellt eine freigegebene Ressource dar, die als COM-Zeichenfolge codiert ist.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptorheaprecord"><strong>DescriptorHeapRecord</strong></a></p></td><td><p>Stellt Deskriptorheapinformationen dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestageerror"><strong>PipeLineStageError</strong></a></p></td><td><p>Stellt einen Fehler in einer Pipelinephase dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pipelinestage"><strong>PipeLineStage</strong></a></p></td><td><p>Stellt eine Pipelinephase dar, einschließlich Details des verwendeten Shaders.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/experimenttrigger"><strong>ExperimentTrigger</strong></a></p></td><td><p>Stellt Informationen zum Experimenttrigger dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/packedcallpkg"><strong>PackedCallPkg</strong></a></p></td><td><p>Stellt ein Paket mit vier Aufrufen dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/symbolserverinfo"><strong>SymbolServerInfo</strong></a></p></td><td><p>Stellt Informationen zum Debugsymbolserver dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/callstackframe"><strong>CallStackFrame</strong></a></p></td><td><p>Stellt Informationen zu einem Frame auf der Aufrufstapel dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/sourcefileinfo"><strong>SourceFileInfo</strong></a></p></td><td><p>Stellt Informationen zu einer Quellcodedatei dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/summaryitem"><strong>SummaryItem</strong></a></p></td><td><p>Stellt zusammenfassende Informationen zu einem Ereignis dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/debugshader"><strong>DebugShader</strong></a></p></td><td><p>Stellt Informationen zu einem Shader unter dem Debugger dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experiment"><strong>Experiment</strong></a></p></td><td><p>Stellt Informationen zu einem Experiment (Erfassung) dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/issue"><strong>Problem</strong></a></p></td><td><p>Stellt Informationen zu einem Problem dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/point2d"><strong>Point2D</strong></a></p></td><td><p>Stellt einen 2D-Punkt mit Ganzzahlkoordinaten ohne Vorzeichen dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/threaddata3d"><strong>ThreadData3D</strong></a></p></td><td><p>Stellt einen 3D-Index in Threaddaten dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/inputlayoutstruct"><strong>InputLayoutStruct</strong></a></p></td><td><p>Stellt die Eingabelayoutfelder eines Scheitelpunktpuffers dar, eins pro Feld im Scheitelpunktpuffer.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryoperation"><strong>PixelHistoryOperation</strong></a></p></td><td><p>Stellt Informationen zum Pixelverlauf dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryintersection"><strong>PixelHistoryIntersection</strong></a></p></td><td><p>Stellt Informationen zu einem bestimmten dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/meshdatabufferlayoutentry"><strong>MeshDataBufferLayoutEntry</strong></a></p></td><td><p>Stellt Informationen zu einem einzelnen Eintrag im Pufferlayout eines Gitternetzes dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/debugshaderrequestinfo"><strong>DebugShaderRequestInfo</strong></a></p></td><td><p>Stellt Informationen zu einer Shaderdebuggeranforderung dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixengineint4"><strong>PixEngineInt4</strong></a></p></td><td><p>Stellt einen 4D-Vektor mit ganzzahligen Koordinaten mit Vorzeichen dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginepoint4d"><strong>PixEnginePoint4D</strong></a></p></td><td><p>Stellt einen 4D-Punkt mit 64-Bit-Gleitkommakoordinaten (double) dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginechanneldesc"><strong>PixEngineChannelDesc</strong></a></p></td><td><p>Stellt eine Beschreibung eines Farbkanals (Beispielkanals) dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureformatdesc"><strong>PixEngineTextureFormatDesc</strong></a></p></td><td><p>Stellt eine Beschreibung eines Texturformats dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturedescriptor"><strong>PixEngineTextureDescriptor</strong></a></p></td><td><p>Stellt eine Beschreibung einer Texturressource dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureslicedescriptor"><strong>PixEngineTextureSliceDescriptor</strong></a></p></td><td><p>Stellt eine Beschreibung eines Texturslices dar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturesliceindex"><strong>PixEngineTextureSliceIndex</strong></a></p></td><td><p>Stellt den Index eines Texturslices dar.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginehistogram"><strong>PixEngineHistogram</strong></a></p></td><td><p>Stellt ein Histogramm einer Textur dar.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Verwandte Themen

[Direct3D Diagnostics Capture Interface Reference](vspixengine-reference.md)

 

 
