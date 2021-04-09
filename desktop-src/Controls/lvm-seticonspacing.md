---
title: LVM_SETICONSPACING Meldung (kommstrg. h)
description: Legt den Abstand zwischen Symbolen in Listenansicht-Steuerelementen fest, die den LVS- \_ Symbolstil aufweisen. Sie können diese Nachricht explizit oder mithilfe des ListView-Makros "$" senden \_ .
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- Windows-Steuerelemente für LVM_SETICONSPACING Meldung
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
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858654"
---
# <a name="lvm_seticonspacing-message"></a>LVM- \_ Nachricht

Legt den Abstand zwischen Symbolen in Listenansicht-Steuerelementen fest, die den [**LVS- \_**](list-view-window-styles.md) Symbolstil aufweisen. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) -Makros "$" senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Abstand in Pixel an, der zwischen Symbolen auf der x-Achse festgelegt werden soll. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Abstand in Pixel an, der zwischen Symbolen auf der y-Achse festgelegt werden soll. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der den vorherigen Abstand der x-Achse im unteren Wort und den vorherigen Abstand der y-Achse im hohen Wort enthält.

## <a name="remarks"></a>Bemerkungen

Die Werte für *LPARAM* sind relativ zur oberen linken Ecke einer Symbol Bitmap. Um den Abstand zwischen Symbolen festzulegen, die sich nicht überlappen, müssen die *LPARAM* -Werte beispielsweise die Größe des Symbols und den von den Symbolen gewünschten leeren Bereich enthalten. Werte, die die Breite des Symbols nicht einschließen, führen zu Überlappungen.

Wenn Sie den Symbol Abstand definieren, müssen die *LPARAM* -Werte auf 4 oder größer festgelegt werden. Kleinere Werte ergeben nicht das gewünschte Layout. Wenn Sie die Symbole auf den Standardabstand zurücksetzen möchten, legen Sie die *LPARAM* -Werte auf-1 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

