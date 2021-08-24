---
description: Die SetAddressInfo-Methode legt die Adressinformationen fest.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: ITConnection::SetAddressInfo-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d90fd6e92e115966df709626b7b58c739d292fedca4fb855999bc3fd8cd853b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774930"
---
# <a name="itconnectionsetaddressinfo-method"></a>ITConnection::SetAddressInfo-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetAddressInfo-Methode** legt die Adressinformationen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStartAddress* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR,** der die Startadresse enthält.

</dd> <dt>

*NumAddresses* \[ In\]
</dt> <dd>

Anzahl der Adressen, die für die Sitzung verwendet werden sollen.

</dd> <dt>

*Ttl* \[ In\]
</dt> <dd>

[*Gültigkeitsdauer (Time-to-Live,*](t-tapgloss.md) TTL) für Übertragungen an den Adressen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Parameter pStartAddress,* *NumAddresses* oder *Ttl* ist ungültig.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>                  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                                   |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Speicher für den *pStartAddress-Parameter* zuzuweisen, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

