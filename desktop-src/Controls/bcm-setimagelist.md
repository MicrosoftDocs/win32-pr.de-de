---
title: BCM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem Schaltflächen-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das \_ SetImageList-Makro der Schaltfläche verwenden.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- Windows-Steuerelemente für BCM_SETIMAGELIST Meldung
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
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040510"
---
# <a name="bcm_setimagelist-message"></a>BCM \_ SetImageList-Meldung

Weist einem Schaltflächen-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das [**\_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) -Makro der Schaltfläche verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Schaltflächen- \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur, die Bildlisten Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

Die Bildliste, auf die im **HIML** -Member der [**Schaltfläche \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur verwiesen wird, muss entweder ein einzelnes Bild enthalten, das für alle Zustände oder einzelne Bilder für jeden Zustand verwendet werden soll. Die folgenden Zustände sind in vssym32. h definiert.

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

Beachten Sie, dass PSB \_ stylushot nur auf Tablet-Computern verwendet wird.

Jeder Wert ist ein Index des entsprechenden Bilds in der Bildliste. Wenn nur ein Bild vorhanden ist, wird es für alle Zustände verwendet. Wenn die Bildliste mehr als ein Bild enthält, entspricht jeder Index einem Zustand der Schaltfläche. Wenn für jeden Zustand kein Bild bereitgestellt wird, wird für diese Zustände ohne Bilder nichts gezeichnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





