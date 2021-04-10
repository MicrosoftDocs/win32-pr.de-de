---
title: TB_BUTTONSTRUCTSIZE Meldung (kommstrg. h)
description: Gibt die Größe der TBBUTTON-Struktur an.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Windows-Steuerelemente für TB_BUTTONSTRUCTSIZE Meldung
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041015"
---
# <a name="tb_buttonstructsize-message"></a>TB \_ buttonstructsize-Meldung

Gibt die Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur an.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur in Bytes.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das System verwendet die Größe, um zu bestimmen, welche Version der Common Control Dynamic Link Library (dll) verwendet wird.

Wenn eine Anwendung die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwendet, um die Symbolleiste zu erstellen, muss die Anwendung diese Nachricht vor dem Senden der Meldung " [**TB \_ AddBitmap**](tb-addbitmap.md) " oder " [**TB \_ AddButtons**](tb-addbuttons.md) " an die Symbolleiste senden. Die Funktion " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) " sendet automatisch **TB " \_ buttonstructsize**", und die Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur ist ein Parameter der Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

