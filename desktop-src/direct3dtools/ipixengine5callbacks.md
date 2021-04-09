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
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124723"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks-Schnittstelle

Rückrufe, die zum Anzeigen von Texturen verwendet werden.

## <a name="members"></a>Member

Die **IPixEngine5Callbacks** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IPixEngine5Callbacks** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPixEngine5Callbacks** -Schnittstelle verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>Freitexturecomplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn eine Textur freigegeben wurde.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>Loadhistogrammcomplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn eine histogrammauslastung abgeschlossen wurde.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>Loadtexturefromfilecomplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Ladevorgang abgeschlossen wurde.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>Loadtextureslicecomplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Slice geladen wurde.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>"Read texelvaluecomplete"</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Texttyp gelesen wurde.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>Rendertexturecomplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Rendering abgeschlossen wurde.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>Savetexturecomplete</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn das Speichern einer Textur abgeschlossen wurde.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
