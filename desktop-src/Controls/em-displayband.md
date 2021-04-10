---
title: EM_DISPLAYBAND Meldung (RichEdit. h)
description: Zeigt einen Teil des Inhalts eines Rich-Edit-Steuer Elements an, wie zuvor für ein Gerät mithilfe der EM- \_ Format Bereichs Nachricht formatiert.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- Windows-Steuerelemente für EM_DISPLAYBAND Meldung
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956727"
---
# <a name="em_displayband-message"></a>EM \_ DisplayBand-Meldung

Zeigt einen Teil des Inhalts eines Rich-Edit-Steuer Elements an, wie zuvor für ein Gerät mithilfe der [**EM- \_ Format Bereichs**](em-formatrange.md) Nachricht formatiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die den Anzeigebereich des Geräts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert " **true**".

Wenn der Vorgang fehlschlägt, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Text-und Component Object Model (com)-Objekte werden durch das Rechteck abgeschnitten. Der Clippingbereich muss von der Anwendung nicht festgelegt werden.

Die Bandbreite ist der Prozess, mit dem eine einzelne Seite der Ausgabe mit einem oder mehreren separaten Rechtecke oder Bändern generiert wird. Wenn alle Bänder auf der Seite platziert werden, ergibt sich ein vollständiges Bild. Diese Vorgehensweise wird häufig von Raster Druckern verwendet, die nicht über genügend Arbeitsspeicher oder die Möglichkeit verfügen, eine vollständige Seite gleichzeitig zu Abbildern. Zu den Bandbreiten von Geräten zählen die meisten Punktmatrix Drucker und einige Laserdrucker.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken von Rich Edit-Steuerelementen](printing-rich-edit-controls.md)
</dt> </dl>

 

