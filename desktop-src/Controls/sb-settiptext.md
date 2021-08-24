---
title: SB_SETTIPTEXT-Nachricht (Commctrl.h)
description: Legt den QuickInfo-Text für ein Teil in einer Statusleiste fest. Die Statusleiste muss mit dem SBT \_ TOOLTIPS-Stil erstellt worden sein, um QuickInfos zu aktivieren.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864ba53066b000f9f7ae65365341238a701b4e70bc4ce8cc70adba923d57a5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637020"
---
# <a name="sb_settiptext-message"></a>SB \_ SETTIPTEXT-Nachricht

Legt den QuickInfo-Text für ein Teil in einer Statusleiste fest. Die Statusleiste muss mit dem [**SBT \_ TOOLTIPS-Stil**](status-bar-styles.md) erstellt worden sein, um QuickInfos zu aktivieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Teils, der den QuickInfo-Text empfängt.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Zeichenpuffer, der den neuen QuickInfo-Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Dieser QuickInfo-Text wird in zwei Situationen angezeigt:

-   Wenn der entsprechende Bereich in der Statusleiste nur ein Symbol enthält.
-   Wenn der entsprechende Bereich in der Statusleiste Text enthält, der aufgrund der Größe des Bereichs abgeschnitten wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ SETTIPTEXTW** (Unicode) und **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





