---
title: Externes. onsendmessagecomplete-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onsendmessagecomplete-Ereignis
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Externe. onsendmessagecomplete-Ereignisfenster Media Player
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
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367439"
---
# <a name="externalonsendmessagecomplete-event"></a>Externes. onsendmessagecomplete-Ereignis

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **onsendmessagecomplete** -Ereignis tritt auf, wenn der Online Shop die Verarbeitung einer Nachricht abgeschlossen hat. Das Skript auf der Ermittlungs Seite hat die Nachricht zuvor durch Aufrufen von " [extern. SendMessage](external-sendmessage.md)" gesendet.

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, verfügt über die folgenden Parameter.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Meldung*
</dt> <dd>

Dieselbe Zeichenfolge, die im **msg** -Parameter von **SendMessage** übergeben wurde.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*
</dt> <dd>

Dieselbe Zeichenfolge, die im **param** -Parameter von **SendMessage** übergeben wurde.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Dadurch*
</dt> <dd>

Eine **Zeichen** Folge, die das Ergebnis der Nachrichten Behandlung enthält. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **SendMessage** -Methode ruft [iwmpcontentpartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)auf, das asynchron zurückgegeben wird. Das heißt, es wird zurückgegeben, bevor der Online Shop die Verarbeitung der Nachricht abschließt. Wenn der Online Shop die Verarbeitung der Nachricht abgeschlossen hat, wird [iwmpcontentpartnercallback:: sendmessagecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)aufgerufen, das wiederum den **onsendmessagecomplete** -Ereignishandler des Skripts aufruft.

Wenn der Onlinespeicher **iwmpcontentpartnercallback:: sendmessagecomplete** aufruft, liefert er einen Ergebniscode im *bstrinresult* -Parameter. Der Ergebniscode wird von Windows Media Player nicht interpretiert. Stattdessen übergibt Windows Media Player den Ergebniscode an den **onsendmessagecomplete** -Ereignishandler im *Ergebnis* Parameter.

Keiner der Parameter (*msg*, *param*, *Result*) des **onsendmessagecomplete** -Ereignis Handlers wird von Windows Media Player interpretiert. Die Parameter sind nur für den Online Shop von Bedeutung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. SendMessage**](external-sendmessage.md)
</dt> <dt>

[**Iwmpcontentpartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**Iwmpcontentpartnercallback:: sendmessagecomplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





