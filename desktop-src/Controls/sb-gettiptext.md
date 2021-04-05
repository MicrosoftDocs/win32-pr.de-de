---
title: SB_GETTIPTEXT Meldung (kommstrg. h)
description: Ruft den QuickInfo-Text für einen Teil in einer Statusleiste ab. Die Statusleiste muss mit dem SBT- \_ Tooltips-Stil erstellt werden, um Quick Infos zu aktivieren.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- Windows-Steuerelemente für SB_GETTIPTEXT Meldung
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859108"
---
# <a name="sb_gettiptext-message"></a>SB \_ GetTipText-Nachricht

Ruft den QuickInfo-Text für einen Teil in einer Statusleiste ab. Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt werden, um Quick Infos zu aktivieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den NULL basierten Index des Teils an, der den QuickInfo-Text empfängt. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Größe des Puffers bei *LPARAM* in Zeichen an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen Zeichen Puffer, der den QuickInfo-Text empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies zu Problemen bei der Anwendung führen. Wenn der Text z. b. zu groß für den *LPARAM* -Puffer ist, kann dies zu einem Pufferüberlauf führen. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ Gettiptextw** (Unicode) und **SB \_ gettiptexta** (ANSI)<br/>               |



 

