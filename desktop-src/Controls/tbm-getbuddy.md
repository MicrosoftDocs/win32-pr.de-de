---
title: TBM_GETBUDDY (Commctrl.h)
description: Ruft das Handle in ein Trackbar-Steuerelement-Fenster an einer bestimmten Position ab. Die angegebene Position ist relativ zur Ausrichtung des Steuerelements (horizontal oder vertikal).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY meldungssteuerelemente Windows
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
ms.openlocfilehash: 6e03053981ed16b97d68d5b2f0c77db64062d64fd2df7b5a347e4757736d4844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829614"
---
# <a name="tbm_getbuddy-message"></a>TBM \_ GETBUDDY-Nachricht

Ruft das Handle in ein Trackbar-Steuerelement-Fenster an einer bestimmten Position ab. Die angegebene Position ist relativ zur Ausrichtung des Steuerelements (horizontal oder vertikal).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der angibt, welches Fensterhand handle nach relativer Position abgerufen wird. Die folgenden Werte sind möglich:



| Wert                                                                                                                                    | Bedeutung                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE!</dt> </dl>    | Ruft das Handle links von der Trackleiste an der Leiste ab. Wenn das Trackbar-Steuerelement den [**TBS \_ VERT-Stil**](trackbar-control-styles.md) verwendet, ruft die Meldung die Leiste oberhalb der Trackleiste ab.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE!</dt> </dl> | Ruft den Handpunkt rechts von der Trackleiste ab. Wenn das Trackbar-Steuerelement den [**TBS \_ VERT-Stil**](trackbar-control-styles.md) verwendet, ruft die Meldung die Leiste unterhalb der Trackleiste ab.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an das Fenster an der von *wParam* angegebenen Position zurück, oder **NULL,** wenn an dieser Position kein Fenster vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





