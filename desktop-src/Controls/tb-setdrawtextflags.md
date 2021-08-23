---
title: TB_SETDRAWTEXTFLAGS Meldung (Commctrl.h)
description: Legt die Textzeichnungsflags für die Symbolleiste fest.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849bbb0e661c9e8afe246894d2d2f59d99d15a3f096ad2295a7018cf3df26ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543880"
---
# <a name="tb_setdrawtextflags-message"></a>TB \_ SETDRAWTEXTFLAGS-Nachricht

Legt die Textzeichnungsflags für die Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Mindestens ein \_ DT-Flag, das in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)angegeben ist und angibt, welche Bits in *lParam* beim Zeichnen des Texts verwendet werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Mindestens eines der \_ in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)angegebenen DT-Flags, die angeben, wie der Schaltflächentext gezeichnet wird. Dieser Wert wird an die **DrawText-Funktion** übergeben, wenn der Schaltflächentext gezeichnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherigen Textzeichnungsflags zurück.

## <a name="remarks"></a>Hinweise

Mit dem *wParam-Parameter* können Sie angeben, welche Flags beim Zeichnen des Texts verwendet werden, auch wenn diese Flags deaktiviert sind. Wenn Sie z. B. nicht möchten, dass das DT \_ CENTER-Flag beim Zeichnen von Text verwendet wird, fügen Sie das DT \_ CENTER-Flag zu *wParam* hinzu und geben nicht das DT \_ CENTER-Flag in *lParam* an. Dadurch wird verhindert, dass das Steuerelement das DT \_ CENTER-Flag an die [**DrawText-Funktion**](/windows/desktop/api/winuser/nf-winuser-drawtext) übergibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

