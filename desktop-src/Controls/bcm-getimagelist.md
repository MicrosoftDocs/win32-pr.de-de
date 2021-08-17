---
title: BCM_GETIMAGELIST (Commctrl.h)
description: Ruft die BUTTON \_ IMAGELIST-Struktur ab, die die einem Schaltflächen-Steuerelement zugewiesene Bildliste beschreibt. Sie können diese Nachricht explizit senden oder das Button \_ GetImageList-Makro verwenden.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba74f358e80871ffad4822fd8088ca6aeb58521d8878254ed920356db5a6daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833911"
---
# <a name="bcm_getimagelist-message"></a>BCM \_ GETIMAGELIST-Nachricht

Ruft die [**BUTTON \_ IMAGELIST-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) ab, die die einem Schaltflächen-Steuerelement zugewiesene Bildliste beschreibt. Sie können diese Nachricht explizit senden oder das [**Button \_ GetImageList-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**BUTTON \_ IMAGELIST-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) die Bildlisteninformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Meldung erfolgreich ist, wird **TRUE zurückgegeben.** Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





