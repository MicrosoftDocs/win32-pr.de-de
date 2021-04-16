---
title: SB_SETTIPTEXT Meldung (kommstrg. h)
description: Legt den QuickInfo-Text für einen Teil in einer Statusleiste fest. Die Statusleiste muss mit dem SBT-Tooltips-Stil erstellt worden sein \_ , um Quick Infos zu aktivieren.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- Windows-Steuerelemente für SB_SETTIPTEXT Meldung
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
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478096"
---
# <a name="sb_settiptext-message"></a>SB-Setup \_ Textnachricht

Legt den QuickInfo-Text für einen Teil in einer Statusleiste fest. Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt worden sein, um Quick Infos zu aktivieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index des Teils, der den QuickInfo-Text empfängt.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Zeichen Puffer, der den neuen QuickInfo-Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Dieser QuickInfo-Text wird in zwei Situationen angezeigt:

-   Wenn der entsprechende Bereich in der Statusleiste nur ein Symbol enthält.
-   Wenn der entsprechende Bereich in der Statusleiste Text enthält, der aufgrund der Größe des Bereichs abgeschnitten wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ "Sttiptextw** (Unicode)" und " **SB \_** " (ANSI)<br/>               |



 

 





