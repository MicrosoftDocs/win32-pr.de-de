---
title: MCM_SETCOLOR Meldung (kommstrg. h)
description: Legt die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements fest. Sie können diese Nachricht explizit oder mit dem monthcal- \_ SetColor-Makro senden.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- Windows-Steuerelemente für MCM_SETCOLOR Meldung
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105987"
---
# <a name="mcm_setcolor-message"></a>MCM- \_ SetColor-Meldung

Legt die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements fest. Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert vom Typ **int** , der angibt, welche Monatskalender Farbe festgelegt werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC- \_ Hintergrund**</dt> </dl>       | Legen Sie die zwischen den Monaten angezeigte Hintergrundfarbe fest.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ monthbk**</dt> </dl>                | Legen Sie die im Monat angezeigte Hintergrundfarbe fest.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**MCSC- \_ Text**</dt> </dl>                         | Legen Sie die Farbe fest, mit der Text innerhalb eines Monats angezeigt wird.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ titlebk**</dt> </dl>                | Legen Sie die im Titel des Kalenders angezeigte Hintergrundfarbe fest.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TitleText**</dt> </dl>          | Legen Sie die Farbe fest, die verwendet wird, um Text innerhalb des Kalender Titels anzuzeigen.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC- \_ trailingtext**</dt> </dl> | Legen Sie die Farbe fest, die verwendet wird, um den Header Tag und den nachfolgenden Tag Header und nachfolgende Tage sind die Tage aus den vorherigen und den nächsten Monaten, die im Kalender des aktuellen Monats angezeigt werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die Farbe darstellt, die für den angegebenen Bereich des Monats Kalenders festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Farbeinstellung für den angegebenen Teil des Monatskalender-Steuer Elements darstellt, wenn erfolgreich. Andernfalls ist die Rückgabe-1.

## <a name="remarks"></a>Bemerkungen

Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung, es sei denn, *wParam* ist ein MCSC- \_ Hintergrund.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

