---
title: IMAGELISTDRAWFLAGS (Commctrl.h)
description: Wird an die IImageList Draw-Methode im fStyle-Member von IMAGELISTDRAWPARAMS übergeben.
ms.assetid: 99fd2cb2-0cb0-40c2-b184-b6d8e54397b4
topic_type:
- apiref
api_name:
- ILD_NORMAL
- ILD_TRANSPARENT
- ILD_BLEND25
- ILD_FOCUS
- ILD_BLEND50
- ILD_SELECTED
- ILD_BLEND
- ILD_MASK
- ILD_IMAGE
- ILD_ROP
- ILD_OVERLAYMASK
- ILD_PRESERVEALPHA
- ILD_SCALE
- ILD_DPISCALE
- ILD_ASYNC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e44d863e82cf126c62262a564e5bf8366fbe71dbb75cc6d47bd16634d798cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544540"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Wird an die [**IImageList::D raw-Methode**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) im **fStyle-Member** von [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)übergeben.



| Konstante/Wert                                                                                                                                                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**ILD \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>                      | Zeichnet das Bild mithilfe der Hintergrundfarbe für die Bildliste. Wenn die Hintergrundfarbe der CLR \_ NONE-Wert ist, wird das Bild transparent mithilfe der Maske gezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**ILD \_ TRANSPARENT**</dt> <dt>0x00000001</dt> </dl>       | Zeichnet das Bild transparent mithilfe der Maske, unabhängig von der Hintergrundfarbe. Dieser Wert hat keine Auswirkung, wenn die Bildliste keine Maske enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**ILD \_ BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | Zeichnet das Bild und kombiniert 25 Prozent mit der durch **rgbFg** angegebenen Mischungsfarbe. Dieser Wert hat keine Auswirkung, wenn die Bildliste keine Maske enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**ILD \_ FOCUS**</dt> <dt>0x00000002</dt> </dl>                         | Identisch mit **ILD \_ BLEND25.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**ILD \_ BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | Zeichnet das Bild, wobei 50 Prozent mit der durch **rgbFg** angegebenen Mischungsfarbe kombiniert werden. Dieser Wert hat keine Auswirkung, wenn die Bildliste keine Maske enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**ILD \_ SELECTED**</dt> <dt>0x00000004</dt> </dl>                | Identisch mit **ILD \_ BLEND50.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**ILD \_ BLEND**</dt> <dt>0x00000004</dt> </dl>                         | Identisch mit **ILD \_ BLEND50.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**ILD \_ MASK**</dt> <dt>0x00000010</dt> </dl>                            | Zeichnet die Maske.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**ILD \_ IMAGE**</dt> <dt>0x00000020</dt> </dl>                         | Wenn für die Überlagerung keine Maske gezeichnet werden muss, legen Sie dieses Flag fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**ILD \_ ROP**</dt> <dt>0x00000040</dt> </dl>                               | Zeichnet das Bild mithilfe des raster-Vorgangscodes, der vom **dwRop-Member** angegeben wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**ILD \_ OVERLAYMASK-0x00000F00**</dt> <dt></dt> </dl>       | Um das Überlagerungsbild aus dem **fStyle-Member** zu extrahieren, verwenden Sie das logische AND, um **fStyle** mit dem **ILD \_ OVERLAYMASK-Wert** zu kombinieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**ILD \_ PRESERVEALPHA-0x00001000**</dt> <dt></dt> </dl> | Behält den Alphakanal im Ziel bei.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**ILD \_ SCALE**</dt> <dt>0x00002000</dt> </dl>                         | Bewirkt, dass das Bild auf cx skaliert wird, anstatt abgeschnitten zu werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**ILD \_ DPISCALE**</dt> <dt>0x00004000</dt> </dl>                | Skaliert das Bild auf den aktuellen DPI der Anzeige.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**ILD \_ ASYNCHRONE**</dt> <dt>0x00008000</dt> </dl>                         | **Windows Vista und höher.** Zeichnen Sie das Bild, wenn es im Cache verfügbar ist. Extrahieren Sie sie nicht automatisch. Die aufgerufene draw-Methode gibt E \_ PENDING an die aufrufende Komponente zurück, die dann eine alternative Aktion wie ein anderes Bild bereitstellen und eine Hintergrundaufgabe in die Warteschlange stellen sollte, um das Laden des Bilds über [**ForceImagePresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) mithilfe des ILFIP \_ ALWAYS-Flags zu erzwingen. Das \_ ILD-ASYNC-Flag verhindert dann, dass der Extraktionsvorgang den aktuellen Thread blockiert, und ist besonders wichtig, wenn eine Draw-Methode aus dem Benutzeroberflächenthread aufgerufen wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

