---
title: RB_GETBANDBORDERS Nachricht (Commctrl.h)
description: Ruft die Rahmen eines Bands ab. Das Ergebnis dieser Meldung kann verwendet werden, um den verwendbaren Bereich in einem Band zu berechnen.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6b07303c10ef6f466907b11cf0e100927f63480690e77ac3dcbe80df80af97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409712"
---
# <a name="rb_getbandborders-message"></a>RB \_ GETBANDBORDERS-Nachricht

Ruft die Rahmen eines Bands ab. Das Ergebnis dieser Meldung kann verwendet werden, um den verwendbaren Bereich in einem Band zu berechnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Bands, für das die Rahmen abgerufen werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Bandrahmen empfängt. Wenn das Rebar-Steuerelement den [**Stil RBS \_ BANDBORDERS**](rebar-control-styles.md) aufweist, erhält jeder Member dieser Struktur die Anzahl der Pixel auf der entsprechenden Seite des Bands, die den Rahmen bilden. Wenn das Rebar-Steuerelement nicht über den **RBS \_ BANDBORDERS-Stil** verfügt, erhält nur der **linke** Member dieser Struktur gültige Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

