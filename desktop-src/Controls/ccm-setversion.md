---
title: CCM_SETVERSION (Commctrl.h)
description: Diese Meldung wird verwendet, um das Steuerelement darüber zu informieren, dass Sie ein Verhalten erwarten, das einer bestimmten Version zugeordnet ist.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION meldungssteuerelemente Windows
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
ms.openlocfilehash: b9453b99ff9cd23675b3b5d79593071e4ebb3fbb65d06a78d0fe8094154b2486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320100"
---
# <a name="ccm_setversion-message"></a>CCM \_ SETVERSION-Meldung

Diese Meldung wird verwendet, um das Steuerelement darüber zu informieren, dass Sie ein Verhalten erwarten, das einer bestimmten Version zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Versionsnummer.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die in der vorherigen **CCM \_ SETVERSION-Meldung angegebene Version** zurück. Wenn *wParam* auf einen Wert festgelegt ist, der größer als die aktuelle DLL-Version ist, wird -1 zurückgegeben.

## <a name="remarks"></a>Hinweise

In einigen Fällen kann sich ein Steuerelement je nach Version unterschiedlich verhalten. Dies gilt in erster Linie für Fehler, die in späteren Versionen behoben wurden. Mit **der CCM \_ SETVERSION-Meldung** können Sie das Steuerelement darüber informieren, welches Verhalten erwartet wird. Sie können ermitteln, welche Version Sie angegeben haben, indem Sie eine [**CCM \_ GETVERSION-Nachricht**](ccm-getversion.md) senden. Ein Beispiel für die Verwendung dieser Meldung finden Sie unter Benutzerdefiniertes Zeichnen mit List-View [und Tree-View Steuerelementen.](custom-draw.md)

Wenn Sie ComCtl32.dll Version 6 installiert haben, gibt die **CCM \_ SETVERSION-Meldung** Version 6 zurück, unabhängig davon, welchen Wert Sie in *wParam* festgelegt haben.

> [!Note]  
> Diese Meldung legt nur die Versionsnummer für das Steuerelement fest, an das sie gesendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





