---
title: Inapsohconstructor-Initialisierungs Methode (napprotocol. h)
description: Initialisiert ein SoH-Protokoll Paket im NAP-System.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode, NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949805"
---
# <a name="inapsohconstructorinitialize-method"></a>Inapsohconstructor:: Initialize-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsohconstructor:: Initialize** -Methode initialisiert ein SoH-Protokoll Paket im NAP-System.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des SHA-oder SHV-Pakets enthält, von dem das Paket erstellt wird.

</dd> <dt>

*isrequest* \[ in\]
</dt> <dd>

Ein **boolescher** Wert, der **true** ist, wenn das Paket ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) sein soll, und **false** , wenn es sich um einen **sohresponse**-Wert handeln soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode muss genau einmal pro Paket aufgerufen werden.

Die in *ID* angegebene [systemhealthentityid](nap-datatypes.md) ist der erste TLV im neu erstellten SoH-Paket und hat den Attributtyp [**sohattributetypesystemhealthid**](sohattributetype-enum.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Napprotocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napprotocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsohconstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





