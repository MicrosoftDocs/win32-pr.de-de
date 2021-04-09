---
title: CCM_SETVERSION Meldung (kommstrg. h)
description: Diese Meldung wird verwendet, um das Steuerelement zu informieren, dass Sie ein Verhalten erwarten, das mit einer bestimmten Version verknüpft ist.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- Windows-Steuerelemente für CCM_SETVERSION Meldung
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040770"
---
# <a name="ccm_setversion-message"></a>CCM- \_ setVersion-Meldung

Diese Meldung wird verwendet, um das Steuerelement zu informieren, dass Sie ein Verhalten erwarten, das mit einer bestimmten Version verknüpft ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Versionsnummer.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die in der vorherigen ccm- **\_ setVersion** -Meldung angegebene Version zurück. Wenn *wParam* auf einen Wert festgelegt ist, der höher als die aktuelle dll-Version ist, wird-1 zurückgegeben.

## <a name="remarks"></a>Bemerkungen

In einigen Fällen kann sich ein Steuerelement abhängig von der jeweiligen Version anders Verhalten. Dies gilt hauptsächlich für Fehler, die in späteren Versionen behoben wurden. Die **ccm- \_ setVersion** -Meldung ermöglicht Ihnen, das Steuerelement zu informieren, welches Verhalten erwartet wird. Sie können ermitteln, welche Version Sie angegeben haben, indem Sie eine [**ccm- \_ GetVersion**](ccm-getversion.md) -Nachricht senden. Ein Beispiel für die Verwendung dieser Nachricht finden Sie unter [benutzerdefiniertes Zeichnen mit List-View und Tree-View Steuerelementen](custom-draw.md).

Wenn Sie ComCtl32.dll Version 6 installiert haben, gibt die **ccm- \_ setVersion** -Nachricht unabhängig von dem Wert, den Sie in *wParam* festlegen, Version 6 zurück.

> [!Note]  
> Mit dieser Meldung wird nur die Versionsnummer für das Steuerelement festgelegt, an das das Steuerelement gesendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





