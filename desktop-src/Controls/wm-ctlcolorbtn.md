---
title: WM_CTLCOLORBTN Meldung (Winuser. h)
description: Die "WM \_ ctlcolorbtn"-Meldung wird vor dem Zeichnen der Schaltfläche an das übergeordnete Fenster einer Schaltfläche gesendet. Das übergeordnete Fenster kann die Text-und Hintergrundfarben der Schaltfläche ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das diese Nachricht verarbeitet.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- Windows-Steuerelemente für WM_CTLCOLORBTN Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949407"
---
# <a name="wm_ctlcolorbtn-message"></a>WM \_ ctlcolorbtn-Nachricht

Die " **WM \_ ctlcolorbtn** "-Meldung wird vor dem Zeichnen der Schaltfläche an das übergeordnete Fenster einer Schaltfläche gesendet. Das übergeordnete Fenster kann die Text-und Hintergrundfarben der Schaltfläche ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das diese Nachricht verarbeitet.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **hdc** , der das Handle für den Anzeige Kontext der Schaltfläche angibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **HWND** , das das Handle für die Schaltfläche angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie ein Handle für einen Pinsel zurückgeben. Das System verwendet den Pinsel zum Zeichnen des Hintergrunds der Schaltfläche.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben. Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.

Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für die Schaltfläche aus. Schaltflächen mit den Formen " [**b \_ Push Button**](button-styles.md)", " [**b \_ DEFPUSHBUTTON**](button-styles.md)" oder "SB [**\_ Push like**](button-styles.md) " verwenden den zurückgegebenen Pinsel nicht. Schaltflächen mit diesen Stilen werden immer mit den Standardsystem Farben gezeichnet. Das Zeichnen von Push-Schaltflächen erfordert mehrere verschiedene Pinsel Gesichter, Hervorhebung und Schatten, aber die **WM \_ ctlcolorbtn** -Meldung ermöglicht nur die Rückgabe eines einzelnen Pinsels. Verwenden Sie zum Bereitstellen einer benutzerdefinierten Darstellung für pushschaltflächen eine vom Besitzer gezeichnete Schaltfläche. Weitere Informationen finden Sie unter [Erstellen von Owner-Drawn](user-controls-intro.md)-Steuerelementen.

Die " **WM \_ ctlcolorbtn** "-Nachricht wird nie zwischen Threads gesendet. Sie wird nur innerhalb eines Threads gesendet.

Die Textfarbe eines Kontrollkästchens oder Options Felds gilt für das Feld bzw. die Schaltfläche, das Häkchen und den Text. Das Fokus Rechteck für diese Schaltflächen bleibt die Standardfarbe des Systems (normalerweise schwarz). Die Textfarbe eines Gruppen Felds bezieht sich auf den Text, jedoch nicht auf die Zeile, in der das Feld definiert ist. Die Textfarbe einer Schaltfläche für den Push gilt nur für das Fokus Rechteck. Dies hat keine Auswirkung auf die Farbe des Texts.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben. Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt. Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

