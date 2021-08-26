---
title: TB_BUTTONSTRUCTSIZE Meldung (Commctrl.h)
description: Gibt die Größe der TBBUTTON-Struktur an.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE Meldung Windows-Steuerelementen
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
ms.openlocfilehash: ceed10eec9038b338d060f28acdab8a10aa88aecef6b264b6d6d0682168f4937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919140"
---
# <a name="tb_buttonstructsize-message"></a>TB \_ BUTTONSTRUCTSIZE-Nachricht

Gibt die Größe der [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) an.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Größe der [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) in Bytes.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das System verwendet die Größe, um zu bestimmen, welche Version der DLL (Common Control Dynamic Link Library) verwendet wird.

Wenn eine Anwendung die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwendet, um die Symbolleiste zu erstellen, muss die Anwendung diese Nachricht an die Symbolleiste senden, bevor die [**TB \_ ADDBITMAP-**](tb-addbitmap.md) oder [**TB \_ ADDBUTTONS-Nachricht**](tb-addbuttons.md) gesendet wird. Die [**CreateToolbarEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) sendet automatisch **TB \_ BUTTONSTRUCTSIZE,** und die Größe der [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) ist ein Parameter der Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

