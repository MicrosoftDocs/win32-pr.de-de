---
title: Imageliststateflags (kommctrl. h)
description: Die folgenden Flags werden an die IImageList-Draw-Methode im fstate-Member von imagelistdrawparameams übergeben.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040443"
---
# <a name="imageliststateflags"></a>Imageliststateflags

Die folgenden Flags werden an die [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) -Methode im **fstate** -Member von [**imagelistdrawparameams**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)übergeben.



| Konstante/Wert                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_ Normales**</dt> <dt>0x00000000</dt> </dl>       | Der Bild Zustand wird nicht geändert.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_ Glanz**</dt> <dt>0x00000001</dt> </dl>             | Wird nicht unterstützt. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_ Schatten**</dt> <dt>0x00000002</dt> </dl>       | Wird nicht unterstützt. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_ Voll**</dt> ständig <dt>0x00000004</dt> </dl> | Verringert die Farbsättigung des Symbols auf Graustufen. Dies betrifft nur 32 bpp-Images. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_ Alpha**</dt> <dt>0x00000008</dt> </dl>          | Alpha blendet das Symbol aus. Alpha Blending steuert die Transparenz Ebene eines Symbols entsprechend dem Wert des Alphakanals. Der Wert des Alphakanals wird durch das **Frame** -Element in der [**imagelistdrawparameams**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) -Methode angegeben. Der Alphakanal kann zwischen 0 und 255 liegen, wobei 0 vollständig transparent ist und 255 vollständig deckend ist.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

