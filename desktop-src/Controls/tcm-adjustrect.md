---
title: TCM_ADJUSTRECT Meldung (kommstrg. h)
description: Berechnet den Anzeigebereich eines Registerkarten-Steuer Elements bei Angabe eines Fenster Rechtecks oder berechnet das Fenster Rechteck, das einem angegebenen Anzeigebereich entsprechen würde. Sie können diese Nachricht explizit oder mithilfe des tabstrg-Elements "tabctrl" senden \_ .
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- Windows-Steuerelemente für TCM_ADJUSTRECT Meldung
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342871"
---
# <a name="tcm_adjustrect-message"></a>TCM- \_ Nachricht

Berechnet den Anzeigebereich eines Registerkarten-Steuer Elements bei Angabe eines Fenster Rechtecks oder berechnet das Fenster Rechteck, das einem angegebenen Anzeigebereich entsprechen würde. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg-Elements \_ "tabctrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der auszuführende Vorgang. Wenn dieser Parameter auf **true** festgelegt ist, gibt *LPARAM* ein Anzeige Rechteck an und empfängt das entsprechende Fenster Rechteck. Wenn dieser Parameter auf **false** festgelegt ist, gibt *LPARAM* ein Fenster Rechteck an und empfängt den entsprechenden Anzeigebereich.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das angegebene Rechteck angibt und das berechnete Rechteck empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Meldung gilt nur für Registerkarten-Steuerelemente, die sich im oberen Bereich befinden. Es gilt nicht für Registerkarten-Steuerelemente, die sich auf der Seite oder im unteren Bereich befinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

