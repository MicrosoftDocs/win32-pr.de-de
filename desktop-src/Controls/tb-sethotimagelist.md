---
title: TB_SETHOTIMAGELIST Meldung (kommstrg. h)
description: Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen von Hot-Schaltflächen verwendet.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- Windows-Steuerelemente für TB_SETHOTIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956876"
---
# <a name="tb_sethotimagelist-message"></a>TB \_ SetHotImageList-Meldung

Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen von Hot-Schaltflächen verwendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die Bildliste, die festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen von Hot-Schaltflächen verwendet wurde, oder **null** , wenn zuvor keine Bildliste festgelegt wurde.

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche ist heiß, wenn sich der Cursor darüber befindet. Für Symbolleisten-Steuerelemente muss der [**tbstyle- \_ Flat**](toolbar-control-and-button-styles.md) -oder [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil für heiße Elemente verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





