---
title: INapComponentInfo ConvertErrorCodeToMessageId-Methode (NapCommon.h)
description: Wird vom NAP-System verwendet, um anzufordern, dass der Integritätsclient einen HRESULT-Fehlercode in eine Meldungs-ID konvertiert.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- ConvertErrorCodeToMessageId-Methode NAP
- ConvertErrorCodeToMessageId-Methode NAP, INapComponentInfo-Schnittstelle
- INapComponentInfo-Schnittstelle NAP , ConvertErrorCodeToMessageId-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c670585674713d114f6505a0c3211d599663545f6b06a40669f7fba8b7eddf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621729"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>INapComponentInfo::ConvertErrorCodeToMessageId-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **Rückrufmethode INapComponentInfo::ConvertErrorCodeToMessageId** wird vom NAP-System verwendet, um anzufordern, dass der Integritätsclient einen HRESULT-Fehlercode in eine Meldungs-ID konvertiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*errorCode* \[ In\]
</dt> <dd>

Der [**Fehlercode**](nap-error-constants.md) aus dem NAP-System, der in eine **MessageId** konvertiert werden soll.

</dd> <dt>

*msgId* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**MessageId,**](nap-datatypes.md) die die Ressourcen-ID der entsprechenden lokalisierten Zeichenfolge enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen dieser Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **zurückgegebene MessageId** wird vom NAP-System verwendet, um eine lokalisierte Zeichenfolge abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





