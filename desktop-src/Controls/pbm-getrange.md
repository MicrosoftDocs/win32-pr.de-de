---
title: PBM_GETRANGE Meldung (kommstrg. h)
description: Ruft Informationen über die aktuellen höchst-und tiefstgrenzen eines angegebenen Statusanzeige-Steuer Elements ab.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- Windows-Steuerelemente für PBM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956814"
---
# <a name="pbm_getrange-message"></a>PBM- \_ GetRange-Nachricht

Ruft Informationen über die aktuellen höchst-und tiefstgrenzen eines angegebenen Statusanzeige-Steuer Elements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flagwert, der angibt, welcher Grenzwert als Rückgabewert der Nachricht verwendet werden soll. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                    | Bedeutung                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Gibt den unteren Grenzwert zurück.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Gibt die Obergrenze zurück.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pbrange**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) -Struktur, die mit den höchst-und tiefstgrenzen des Statusanzeige-Steuer Elements aufgefüllt werden soll. Wenn dieser Parameter auf **null** festgelegt ist, gibt das Steuerelement nur das von *wParam* angegebene Limit zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der den von *wParam* angegebenen Grenzwert darstellt. Wenn *LPARAM* nicht **null** ist, muss *LPARAM* auf eine [**pbrange**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) -Struktur verweisen, die mit beiden Limit-Werten gefüllt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





