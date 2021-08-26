---
title: PBM_GETRANGE Meldung (Commctrl.h)
description: Ruft Informationen zu den aktuellen hohen und niedrigen Grenzwerten eines bestimmten Statusanzeige-Steuerelements ab.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 007a62386180e7b47edca201236cd1dacc86df696b5705d02ec1da0acb89761c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986400"
---
# <a name="pbm_getrange-message"></a>PBM \_ GETRANGE-Nachricht

Ruft Informationen zu den aktuellen hohen und niedrigen Grenzwerten eines bestimmten Statusanzeige-Steuerelements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flagwert, der angibt, welcher Grenzwert als Rückgabewert der Nachricht verwendet werden soll. Dieser Parameter kann einer der folgenden Werte sein:



| Wert                                                                                                                                    | Bedeutung                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE!</dt> </dl>    | Gibt den unteren Grenzwert zurück.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE!</dt> </dl> | Gibt den hohen Grenzwert zurück.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PBRANGE-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) die mit den hohen und niedrigen Grenzwerten des Statusanzeige-Steuerelements gefüllt werden soll. Wenn dieser Parameter auf **NULL** festgelegt ist, gibt das Steuerelement nur den von *wParam* angegebenen Grenzwert zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen INT zurück, der den von *wParam* angegebenen Grenzwert darstellt. Wenn *lParam* nicht **NULL** ist, muss *lParam* auf eine [**PBRANGE-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) verweisen, die mit beiden Grenzwerten gefüllt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





