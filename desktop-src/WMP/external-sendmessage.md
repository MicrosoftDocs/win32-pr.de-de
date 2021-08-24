---
title: External.sendMessage-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die sendMessage-Methode sendet eine Nachricht an das Plug-In des Onlineshops.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- sendMessage-Windows Media Player
- sendMessage-Methode Windows Media Player , Externe Klasse
- Externe Klasse Windows Media Player , sendMessage-Methode
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4985bae2f9170bdb0db1d6cdb995f2c14fe813bcb061485c179bc058539e84c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648360"
---
# <a name="externalsendmessage-method"></a>External.sendMessage-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **sendMessage-Methode** sendet eine Nachricht an das Plug-In des Onlineshops.

## <a name="syntax"></a>Syntax


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Msg* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die die Meldung enthält.

</dd> <dt>

*Param* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die der Meldung zugeordnete Parameter enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Nachricht wird asynchron gesendet. Das heißt, diese Methode gibt sofort zurück, anstatt auf die Verarbeitung der Nachricht zu warten. Wenn das Plug-In die Verarbeitung der Nachricht abgeschlossen hat, ruft es die [IWMPContentPartnerCallback::SendMessageComplete-Methode](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) auf, die wiederum den [OnSendMessageComplete-Ereignishandler](external-onsendmessagecomplete-event.md) des Skripts aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner::SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





