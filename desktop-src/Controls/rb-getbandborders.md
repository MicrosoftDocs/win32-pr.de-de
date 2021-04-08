---
title: RB_GETBANDBORDERS Meldung (kommstrg. h)
description: Ruft die Rahmen eines Bands ab. Das Ergebnis dieser Nachricht kann verwendet werden, um den nutzbaren Bereich in einem Band zu berechnen.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- Windows-Steuerelemente für RB_GETBANDBORDERS Meldung
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956800"
---
# <a name="rb_getbandborders-message"></a>RB \_ getBandBorders-Meldung

Ruft die Rahmen eines Bands ab. Das Ergebnis dieser Nachricht kann verwendet werden, um den nutzbaren Bereich in einem Band zu berechnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Bands, für das die Rahmen abgerufen werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Band Rahmen empfängt. Wenn das Grund leisten-Steuerelement den [**RSB- \_ bandborder**](rebar-control-styles.md) -Stil hat, erhält jedes Element dieser Struktur die Anzahl der Pixel auf der entsprechenden Seite des Bands, die den Rahmen bilden. Wenn das Grund leisten-Steuerelement nicht den **RSB- \_ bandrahmenstil** hat, erhält nur das **linke** Element dieser Struktur gültige Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

