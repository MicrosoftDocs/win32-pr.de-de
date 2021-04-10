---
title: TB_GETITEMDROPDOWNRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck des Dropdown Fensters für ein Symbolleisten Element mit der btns-Dropdown Liste für den Stil \_ ab.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- Windows-Steuerelemente für TB_GETITEMDROPDOWNRECT Meldung
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040231"
---
# <a name="tb_getitemdropdownrect-message"></a>TB \_ getitemdropdownrect-Meldung

Ruft das umgebende Rechteck des Dropdown Fensters für ein Symbolleisten Element mit der [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md)Liste für den Stil ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der null basierte Index des Symbolleisten-Steuer Elements, für das das umgebende Rechteck abgerufen werden soll.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>Ein Zeiger auf eine <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> -Struktur, um die umschließenden Rechteck Informationen zu erhalten. Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich. Die in der **Rect** -Struktur zurückgegebenen Koordinaten werden als Client Koordinaten ausgedrückt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer einen Wert ungleich 0 zurück.

## <a name="remarks"></a>Bemerkungen

Das Element muss den [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

