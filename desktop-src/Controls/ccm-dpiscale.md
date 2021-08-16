---
title: CCM_DPISCALE-Nachricht (Commctrl.h)
description: Aktiviert die automatische Skalierung hoher Punkte pro Zoll (DPI) in Tree-View Steuerelementen, List-View Steuerelementen, ComboBoxEx-Steuerelementen, Header-Steuerelementen, Schaltflächen, Symbolleisten-Steuerelementen, Animationssteuerelementen und Bildlisten.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e72cb8ac3acf413e4381580a4ecf38a4f5bd4b2f5b03d6cff7d7abb85c1f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320250"
---
# <a name="ccm_dpiscale-message"></a>CCM \_ DPISCALE-Nachricht

Aktiviert die automatische Skalierung von hohen Punkten pro Zoll (DPI) in [Strukturansicht-Steuerelementen,](tree-view-controls.md) [List-View-Steuerelementen,](list-view-control-reference.md) [ComboBoxEx-Steuerelementen,](comboboxex-controls.md) [Headersteuerelementen,](header-controls.md) [Schaltflächen, Symbolleisten-Steuerelementen,](buttons.md) [Animationssteuerelementen](animation-control-overview.md)und [Bildlisten.](image-lists.md) [](toolbar-controls-overview.md)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Legen Sie auf **TRUE** fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Schnellstart und [Taskleiste](/windows/desktop/shell/taskbar) sollten keine dpi-Skalierung angeben, da die Bilder bereits skaliert sind.

Jedes Steuerelement, das eine mit der SmallIcon-Metrik erstellte Bildliste verwendet, sollte seine Symbole nicht skalieren.

> [!Note]  
> Um diese API verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

