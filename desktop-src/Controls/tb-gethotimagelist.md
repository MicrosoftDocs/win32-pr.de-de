---
title: TB_GETHOTIMAGELIST Meldung (kommstrg. h)
description: Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Hot-Schaltflächen anzuzeigen.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- Windows-Steuerelemente für TB_GETHOTIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104030"
---
# <a name="tb_gethotimagelist-message"></a>TB- \_ gethotimagelist-Meldung

Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Hot-Schaltflächen anzuzeigen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die das-Steuerelement verwendet, um Hot-Schaltflächen anzuzeigen, oder **null** , wenn keine Liste mit den heißen Bildern festgelegt

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche ist heiß, wenn sich der Cursor darüber befindet. Für Symbolleisten-Steuerelemente muss der [**tbstyle- \_ Flat**](toolbar-control-and-button-styles.md) -oder [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil für heiße Elemente verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





