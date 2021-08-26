---
title: BCM_SETIMAGELIST (Commctrl.h)
description: Weist einem Schaltflächen-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das Button \_ SetImageList-Makro verwenden.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5c88020bb139c358b17386b003bfb9de9cfcd4e769b9262ed90e23f3f95e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921560"
---
# <a name="bcm_setimagelist-message"></a>BCM \_ SETIMAGELIST-Meldung

Weist einem Schaltflächen-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das [**Button \_ SetImageList-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) verwenden.

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

 

Die Bildliste, auf die im **himl-Member** der [**BUTTON \_ IMAGELIST-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) verwiesen wird, sollte entweder ein einzelnes Bild enthalten, das für alle Zustände oder einzelne Bilder für jeden Zustand verwendet werden soll. Die folgenden Zustände sind in vssym32.h definiert.

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

Beachten Sie, dass PBS \_ STYLUSHOT nur auf Tabletcomputern verwendet wird.

Jeder Wert ist ein Index für das entsprechende Bild in der Bildliste. Wenn nur ein Bild vorhanden ist, wird es für alle Zustände verwendet. Wenn die Bildliste mehr als ein Bild enthält, entspricht jeder Index einem Zustand der Schaltfläche. Wenn nicht für jeden Zustand ein Bild bereitgestellt wird, wird für diese Zustände ohne Bilder nichts gezeichnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





