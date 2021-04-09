---
title: PGM_SETSCROLLINFO Meldung (kommstrg. h)
description: Legt die scrollparameter des Pager-Steuer Elements fest, einschließlich des Timeout Werts, der Zeilen pro Timeout und der Pixel pro Zeile. Sie können diese Nachricht explizit oder mithilfe des Pager- \_ Makros setScrollInfo senden.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- Windows-Steuerelemente für PGM_SETSCROLLINFO Meldung
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858821"
---
# <a name="pgm_setscrollinfo-message"></a>PGM- \_ setScrollInfo-Meldung

\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]

Legt die scrollparameter des Pager-Steuer Elements fest, einschließlich des Timeout Werts, der Zeilen pro Timeout und der Pixel pro Zeile. Sie können diese Nachricht explizit oder mithilfe des [**Pager-Makros \_ setScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **uint** , das den Timeout Wert für den Bild Lauf in Millisekunden angibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **uint** , das die Anzahl der Zeilen angibt, die pro Timeout durchlaufen werden. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **uint** , das die Anzahl der Pixel pro Zeile angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.

## <a name="remarks"></a>Bemerkungen

Der *wParam* -Timeout Wert steuert die Rate, mit der das Pager-Steuerelement scrollereignisse generiert, wenn das Steuerelement die Mauseingabe erfasst hat und die linke Maustaste gedrückt wird. Kleinere Werte führen zu einem schnelleren Bildlauf. größere Werte führen zu einem langsameren Bildlauf. Der Standardwert ist ein Achtel der Doppelklick Zeit. Weitere Informationen finden Sie unter [**getdoubleclicktime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).

Standardmäßig scrollt das Pager-Steuerelement bei jedem scrollereignis einen Betrag, der der gesamten Breite oder Höhe des Steuer Elements entspricht, je nachdem, ob das Pager-Steuerelement eine horizontale oder vertikale Ausrichtung aufweist. Die Werte in *LPARAM* werden zum Überschreiben der standardmäßigen scrollmenge verwendet. Wenn Werte ungleich NULL angegeben werden, ist der scrollbetrag das Produkt der beiden Werte (LoWord (*LPARAM*) \* HIWORD (*LPARAM*)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pager \_ setScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

