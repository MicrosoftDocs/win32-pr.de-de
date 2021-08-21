---
title: LVM_SETICONSPACING Nachricht (Commctrl.h)
description: Legt den Abstand zwischen Symbolen in Listenansichtssteuerelementen mit dem \_ LVS-SYMBOLformat fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetIconSpacing-Makros senden.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5897b0ca6aec7763cc24a0ea538f336e7a2f737f2ddc0e7cb52a2145e570db47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019177"
---
# <a name="lvm_seticonspacing-message"></a>LVM \_ SETICONSPACING-Nachricht

Legt den Abstand zwischen Symbolen in Listenansichtssteuerelementen mit dem [**\_ LVS-SYMBOLformat**](list-view-window-styles.md) fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetIconSpacing-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Abstand in Pixel an, der zwischen Symbolen auf der x-Achse festgelegt werden soll. [**HiWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Abstand in Pixel an, der zwischen Symbolen auf der y-Achse festgelegt werden soll. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der den vorherigen x-Achsenabstand im unteren Wort und den vorherigen Abstand der y-Achse im hohen Wort enthält.

## <a name="remarks"></a>Hinweise

Werte für *lParam* sind relativ zur oberen linken Ecke einer Symbolbitmap. Daher müssen die *lParam-Werte* die Größe des Symbols sowie den zwischen Symbolen gewünschten Leerraum enthalten, um den Abstand zwischen Symbolen festzulegen, die sich nicht überschneiden. Werte, die die Breite des Symbols nicht enthalten, führen zu Überlappungen.

Beim Definieren des Symbolabstands müssen die *lParam-Werte* auf 4 oder größer festgelegt werden. Kleinere Werte ergeben nicht das gewünschte Layout. Um die Symbole auf den Standardabstand zurückzusetzen, legen Sie die *lParam-Werte* auf -1 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

