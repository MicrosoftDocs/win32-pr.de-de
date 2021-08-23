---
title: IMAGELISTSTATEFLAGS (Commctrl.h)
description: Die folgenden Flags werden an die IImageList Draw-Methode im fState-Member von IMAGELISTDRAWPARAMS übergeben.
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
ms.openlocfilehash: 3cbb4eef2f744c78e84999e9f07f3ca5a06d5dbf93dbfa26d5c6593d94d4e19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576140"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

Die folgenden Flags werden an die [**IImageList::D raw-Methode**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) im **fState-Member** von [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)übergeben.



| Konstante/Wert                                                                                                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>       | Der Imagezustand wird nicht geändert.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_ 0X00000001**</dt> <dt></dt> </dl>             | Wird nicht unterstützt. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_ SHADOW**</dt> <dt>0x00000002</dt> </dl>       | Wird nicht unterstützt. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_ SATURATE**</dt> <dt>0x00000004</dt> </dl> | Reduziert die Farbsättigung des Symbols auf Graustufen. Dies betrifft nur 32bpp-Images. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_ ALPHA**</dt> <dt>0x00000008</dt> </dl>          | Alpha kombiniert das Symbol. Die Alphamischung steuert die Transparenzebene eines Symbols entsprechend dem Wert des Alphakanals. Der Wert des Alphakanals wird durch den **Framemember** in der [**IMAGELISTDRAWPARAMS-Methode**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) angegeben. Der Alphakanal kann zwischen 0 und 255 sein, wobei 0 vollständig transparent und 255 vollständig deckend ist.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

