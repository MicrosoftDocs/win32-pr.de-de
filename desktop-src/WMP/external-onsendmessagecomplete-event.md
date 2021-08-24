---
title: External.OnSendMessageComplete-Ereignis
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.OnSendMessageComplete-Ereignis
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- External.OnSendMessageComplete-Windows Media Player
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dede59d2c52f20050a490e6ded1389e63884e598868e9736195280e3269a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648730"
---
# <a name="externalonsendmessagecomplete-event"></a>External.OnSendMessageComplete-Ereignis

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **OnSendMessageComplete-Ereignis** tritt auf, wenn der Onlineshop die Verarbeitung einer Nachricht abgeschlossen hat. Das Skript auf der Ermittlungsseite hat die Nachricht zuvor durch Aufrufen von [External.sendMessage gesendet.](external-sendmessage.md)

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dies ist eine Schreibeigenschaft, die den Namen der Funktion im Skript angibt, Windows Media Player beim Auftreten des Ereignisses aufruft.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, verfügt über die folgenden Parameter.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*
</dt> <dd>

Dieselbe Zeichenfolge, die im **Msg-Parameter** von **sendMessage übergeben wurde.**

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*
</dt> <dd>

Dieselbe Zeichenfolge, die im **Parameter Param** von **sendMessage übergeben wurde.**

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Ergebnis*
</dt> <dd>

**Eine Zeichenfolge,** die das Ergebnis der Nachrichtenbehandlung enthält. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **sendMessage-Methode** ruft [IWMPContentPartner::SendMessage auf,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)die asynchron zurückgibt. Das heißt, es wird zurückgegeben, bevor der Onlineshop die Verarbeitung der Nachricht beendet. Wenn der Onlineshop die Verarbeitung der Nachricht abgeschlossen hat, ruft er [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)auf, der wiederum den **OnSendMessageComplete-Ereignishandler** des Skripts aufruft.

Wenn der Onlineshop **IWMPContentPartnerCallback::SendMessageComplete** aufruft, stellt er einen Ergebniscode im *bstrResult-Parameter* zur Verfügung. Windows Media Player interpretiert diesen Ergebniscode nicht. Stattdessen wird Windows Media Player Ergebniscode an den **OnSendMessageComplete-Ereignishandler** im *Result-Parameter* übergeben.

Keiner der Parameter (*Msg*, *Param*, *Result*) des **OnSendMessageComplete-Ereignishandlers** wird von Windows Media Player. Die Parameter haben nur eine Bedeutung für den Onlineshop.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.sendMessage**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner::SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





