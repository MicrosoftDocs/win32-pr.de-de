---
title: Imagelistdrawflags (kommctrl. h)
description: Wird an die IImageList-Draw-Methode im fstyle-Member von imagelistdrawparameams übergeben.
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
ms.openlocfilehash: 0743fc2778b3ef693646327fe8206ebedcb89e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949703"
---
# <a name="imagelistdrawflags"></a>Imagelistdrawflags

Übergeben an die [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) -Methode im **fstyle** -Member von [**imagelistdrawpara**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Konstante/Wert                                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**Ild \_ Normales**</dt> <dt>0x00000000</dt> </dl>                      | Zeichnet das Bild mithilfe der Hintergrundfarbe für die Bildliste. Wenn die Hintergrundfarbe der CLR \_ None-Wert ist, wird das Bild transparent mithilfe der Maske gezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**Ild \_ TRANSPARENT**</dt> <dt>0x00000001</dt> </dl>       | Zeichnet das Bild unabhängig von der Hintergrundfarbe transparent mithilfe der Maske. Dieser Wert hat keine Auswirkung, wenn die Bildliste keine Maske enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**Ild \_ BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | Zeichnet das Bild, wobei 25 Prozent mit der durch **rgbfg** angegebenen Blend-Farbe kombiniert werden. Dieser Wert hat keine Auswirkung, wenn die Bildliste keine Maske enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**Ild \_ Fokus**</dt> <dt>0x00000002</dt> </dl>                         | Identisch mit **ild \_ BLEND25**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**Ild \_ BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | Zeichnet das Bild, wobei 50 Prozent mit der durch **rgbfg** angegebenen Blend-Farbe kombiniert werden. Dieser Wert hat keine Auswirkung, wenn die Bildliste keine Maske enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**Ild \_ Ausgewähltes**</dt> <dt>0x00000004</dt> </dl>                | Identisch mit **ild \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**Ild \_ Blend**</dt> <dt>0x00000004</dt> </dl>                         | Identisch mit **ild \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**Ild \_ Maske**</dt> <dt>0x00000010</dt> </dl>                            | Zeichnet die Maske.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**Ild \_ Bild**</dt> <dt>0x00000020</dt> </dl>                         | Wenn für das Overlay keine Maske gezeichnet werden muss, legen Sie dieses Flag fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**Ild \_ ROP**</dt> <dt>0x00000040</dt> </dl>                               | Zeichnet das Bild mithilfe des vom **dwrop** -Member angegebenen Raster Vorgangs Codes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**Ild \_ Overlaymask**</dt> <dt>0x00000f</dt> </dl>       | Um das Überlagerungs Bild aus dem **fstyle** -Element zu extrahieren, verwenden Sie das logische und zum Kombinieren von **fstyle** mit dem **ild \_ overlaymask** -Wert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**Ild \_ Preservealpha**</dt> <dt>0x00001000</dt> </dl> | Behält den Alphakanal im Ziel bei.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**Ild \_ Skalieren**</dt> von <dt>0x00002000</dt> </dl>                         | Bewirkt, dass das Bild auf CX und CY skaliert wird, anstatt abgeschnitten zu werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**Ild \_ Dpiscale**</dt> <dt>0x00004000</dt> </dl>                | Skaliert das Bild auf den aktuellen dpi-Abschnitt der Anzeige.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**Ild \_ Async**</dt> <dt>0x00008000</dt> </dl>                         | **Windows Vista und höher.** Zeichnen Sie das Bild, wenn es im Cache verfügbar ist. Extrahieren Sie Sie nicht automatisch. Die aufgerufene Draw-Methode gibt "E \_ Pending" an die aufrufende Komponente zurück, die dann eine alternative Aktion durchführen sollte, wie z. b., ein weiteres Bild bereitstellen und eine Hintergrundaufgabe in eine Warteschlange stellen, um das Laden des Bilds über " [**forceimagepresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) " mithilfe des "Il \_ Das ild \_ Async-Flag verhindert dann, dass der Extraktions Vorgang den aktuellen Thread blockiert. Dies ist besonders wichtig, wenn eine Draw-Methode aus dem Benutzeroberflächen Thread aufgerufen wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

