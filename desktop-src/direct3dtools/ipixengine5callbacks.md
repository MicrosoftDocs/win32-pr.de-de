---
description: Rückrufe, die zum Anzeigen von Texturen verwendet werden.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e4d672909d0d0bc332f40d672d7c658ecb5d3049
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628076"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks-Schnittstelle

Rückrufe, die zum Anzeigen von Texturen verwendet werden.

## <a name="members"></a>Member

Die **IPixEngine5Callbacks-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixEngine5Callbacks** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPixEngine5Callbacks-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">Beschreibung</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn eine Textur frei wurde.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, mit der der Host benachrichtigt wird, wenn ein Histogramm geladen wurde.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Texturladeprogramm abgeschlossen wurde.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, mit der der Host benachrichtigt wird, wenn ein Texturslice geladen wurde.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, mit der der Host benachrichtigt wird, wenn ein Texelwert gelesen wurde.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, mit der der Host benachrichtigt wird, wenn ein Texturrendering abgeschlossen wurde.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn das Speichern einer Textur abgeschlossen wurde.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
