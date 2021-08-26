---
title: DTM_SETFORMAT Meldung (Commctrl.h)
description: Legt die Anzeige eines DTP-Steuerelements (Date and Time Picker) basierend auf einer angegebenen Formatzeichenfolge fest. Sie können diese Nachricht explizit senden oder das DateTime \_ SetFormat-Makro verwenden.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 17d4bb08694b63c21f1790d0a1366dd34d1083592bdeb62d532a32a96be3857a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877860"
---
# <a name="dtm_setformat-message"></a>FEHLERMELDUNG \_ SETFORMAT

Legt die Anzeige eines DTP-Steuerelements (Date and Time Picker) basierend auf einer angegebenen Formatzeichenfolge fest. Sie können diese Nachricht explizit senden oder das [**DateTime \_ SetFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine auf null endende [Formatzeichenfolge,](date-and-time-picker-controls.md) die die gewünschte Anzeige definiert. Wenn Sie diesen Parameter auf **NULL** festlegen, wird das Steuerelement auf die Standardformatzeichenfolge für den aktuellen Stil zurückgesetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

Es ist akzeptabel, zusätzliche Zeichen in die Formatzeichenfolge aufzunehmen, um eine umfangreichere Anzeige zu erzeugen. Alle nicht formatierten Zeichen müssen jedoch in einfache Anführungszeichen eingeschlossen werden. Beispielsweise würde die Formatzeichenfolge "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" eine Ausgabe wie "Today is: 04:22:31 Tuesday Mar 23, 1996" erzeugen.

> [!Note]  
> Ein DTP-Steuerelement verfolgt Gebietsschemaänderungen nach, wenn es die Standardformatzeichenfolge verwendet. Wenn Sie eine benutzerdefinierte Formatzeichenfolge festlegen, wird sie nicht als Reaktion auf Gebietsschemaänderungen aktualisiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **MF \_ SETFORMATW** (Unicode) und **MF \_ SETFORMATA** (ANSI)<br/>               |



 

 





