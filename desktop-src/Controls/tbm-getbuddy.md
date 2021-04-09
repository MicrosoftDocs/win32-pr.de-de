---
title: TBM_GETBUDDY Meldung (kommstrg. h)
description: Ruft das Handle für ein Fenster des TrackBar-Steuerelement-Steuer Elements an einem angegebenen Speicherort ab. Der angegebene Speicherort ist relativ zur Ausrichtung des Steuer Elements (horizontal oder vertikal).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- Windows-Steuerelemente für TBM_GETBUDDY Meldung
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957245"
---
# <a name="tbm_getbuddy-message"></a>TBM \_ GetBuddy-Nachricht

Ruft das Handle für ein Fenster des TrackBar-Steuerelement-Steuer Elements an einem angegebenen Speicherort ab. Der angegebene Speicherort ist relativ zur Ausrichtung des Steuer Elements (horizontal oder vertikal).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert, der angibt, welches Adress Fenster Handle von relativer Position abgerufen wird. Die folgenden Werte sind möglich:



| Wert                                                                                                                                    | Bedeutung                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Ruft das Handle für den Kumpel Links von der TrackBar ab. Wenn das TrackBar-Steuerelement den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, ruft die Nachricht den Kumpel über der TrackBar ab.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Ruft das Handle für den Buddy rechts von der TrackBar ab. Wenn das TrackBar-Steuerelement den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, ruft die Nachricht den Kumpel unterhalb der TrackBar ab.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Buddy-Fenster an der von *wParam* angegebenen Position zurück, oder **null** , wenn kein Buddy-Fenster an dieser Stelle vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





