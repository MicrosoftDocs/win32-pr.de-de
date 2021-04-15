---
title: BCM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft die ImageList-Struktur der Schaltfläche ab \_ , die die einem Schaltflächen-Steuerelement zugewiesene Bildliste beschreibt. Sie können diese Nachricht explizit senden oder das \_ GetImageList-Makro der Schaltfläche verwenden.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Windows-Steuerelemente für BCM_GETIMAGELIST Meldung
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
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476995"
---
# <a name="bcm_getimagelist-message"></a>BCM \_ GetImageList-Meldung

Ruft die [**\_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur der Schaltfläche ab, die die einem Schaltflächen-Steuerelement zugewiesene Bildliste beschreibt. Sie können diese Nachricht explizit senden oder das [**\_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) -Makro der Schaltfläche verwenden.

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

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





