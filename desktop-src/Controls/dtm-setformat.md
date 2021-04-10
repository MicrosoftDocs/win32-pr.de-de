---
title: DTM_SETFORMAT Meldung (kommstrg. h)
description: Legt die Anzeige eines DTP-Steuer Elements auf der Grundlage einer angegebenen Format Zeichenfolge fest. Sie können diese Nachricht explizit senden oder das DateTime- \_ SetFormat-Makro verwenden.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- Windows-Steuerelemente für DTM_SETFORMAT Meldung
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040809"
---
# <a name="dtm_setformat-message"></a>DTM- \_ SetFormat-Meldung

Legt die Anzeige eines DTP-Steuer Elements auf der Grundlage einer angegebenen Format Zeichenfolge fest. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine NULL terminierte [Format Zeichenfolge](date-and-time-picker-controls.md) , die die gewünschte Anzeige definiert. Wenn dieser Parameter auf **null** festgelegt wird, wird das Steuerelement auf die Standardformat Zeichenfolge für den aktuellen Stil zurückgesetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Es ist zulässig, zusätzliche Zeichen innerhalb der Format Zeichenfolge einzuschließen, um eine umfangreichere Anzeige zu erhalten. Alle nicht Formatierungszeichen müssen jedoch in einfache Anführungszeichen eingeschlossen werden. Die Format Zeichenfolge "" heute beispielsweise: "hh": 'm ": es ddddmmmdd", "yyy", erzeugt eine Ausgabe wie "Today is: 04:22:31 Tuesday Mar 23, 1996".

> [!Note]  
> Ein DTP-Steuerelement verfolgt Gebiets Schema Änderungen, wenn es die Standardformat Zeichenfolge verwendet. Wenn Sie eine benutzerdefinierte Format Zeichenfolge festlegen, wird Sie nicht als Reaktion auf Gebiets Schema Änderungen aktualisiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DTM \_ Setformatw** (Unicode) und **DTM \_ setformata** (ANSI)<br/>               |



 

 





