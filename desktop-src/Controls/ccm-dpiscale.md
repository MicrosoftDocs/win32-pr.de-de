---
title: CCM_DPISCALE Meldung (kommstrg. h)
description: Ermöglicht die automatische Skalierung von hohen DPI-Werten (dpi) in Tree-View Steuerelementen, List-View Steuerelementen, ComboBoxEx-Steuerelementen, Header Steuerelementen, Schaltflächen, Symbolleisten-Steuerelementen, Animations Steuerelementen und Bildlisten.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Windows-Steuerelemente für CCM_DPISCALE Meldung
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
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104517"
---
# <a name="ccm_dpiscale-message"></a>CCM \_ dpiscale-Nachricht

Aktiviert die automatische Skalierung von hohen dpi [-](tree-view-controls.md)Werten (dpi) in Strukturansicht-Steuerelementen, [Listenansicht-](list-view-control-reference.md)Steuerelementen, [ComboBoxEx](comboboxex-controls.md)-Steuerelementen, [Header](header-controls.md)Steuerelementen, [Schalt](buttons.md)Flächen, [Symbol](toolbar-controls-overview.md)leisten-Steuerelementen, [Animations Steuerelementen](animation-control-overview.md)und [Bildlisten](image-lists.md).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Auf " **true**" festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Die Schnellstart-und [Taskleiste](/windows/desktop/shell/taskbar) sollten keine DPI-Skalierung angeben, da die Bilder bereits skaliert sind.

Jedes Steuerelement, das eine mit der SmallIcon-Metrik erstellte Bildliste verwendet, sollte seine Symbole nicht skalieren.

> [!Note]  
> Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

