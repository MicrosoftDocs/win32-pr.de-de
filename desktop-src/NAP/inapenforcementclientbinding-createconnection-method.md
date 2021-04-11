---
title: Inapenforcementclientbinding-Methode "fiateconnetction" (napforcementclient. h)
description: Wird von enforcern zum Erstellen von Verbindungs Objekten verwendet.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- Methode "deeconnetction" für NAP
- Anateconnetction-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, Methode "kreateconnetction"
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040404"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a>Inapenforcementclientbinding:: kreateconnetction-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientbinding:: kreateconnetction** -Factorymethode wird von enforcern zum Erstellen von Verbindungs Objekten verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindung* \[ vorgenommen\]
</dt> <dd>

Ein com-Zeiger auf eine neue [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle, die vom NAP-System zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Inapenforcementclientbinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**Inapenforcementclientconnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





