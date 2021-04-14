---
title: Inapcomponentinfo converterrorcodetomess ageid-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um anzufordern, dass der Integritäts Client einen HRESULT-Fehlercode in eine Nachrichten-ID konvertiert.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Converterrorcodetomess ageid-Methode NAP
- Converterrorcodetomess ageid-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo-Schnittstelle NAP, converterrorcodetomess ageid-Methode
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
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478918"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>Inapcomponentinfo:: converterrorcodetomess ageid-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapcomponentinfo:: converterrorcodetomesageid** -Rückruf Methode wird vom NAP-System verwendet, um anzufordern, dass der Integritäts Client einen HRESULT-Fehlercode in eine Nachrichten-ID konvertiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*errorCode* \[ in\]
</dt> <dd>

Der [**Fehlercode**](nap-error-constants.md) aus dem NAP-System, der in eine **MessageId** konvertiert werden soll.

</dd> <dt>

*msgid* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID der entsprechenden lokalisierten Zeichenfolge enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die zurückgegebene **MessageId** wird vom NAP-System verwendet, um eine lokalisierte Zeichenfolge abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Inapcomponentinfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





