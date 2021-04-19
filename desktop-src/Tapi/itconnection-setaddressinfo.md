---
description: Die setaddressinfo-Methode legt die Adressinformationen fest.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'Itconnection:: setaddressinfo-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364886"
---
# <a name="itconnectionsetaddressinfo-method"></a>Itconnection:: setaddressinfo-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **setaddressinfo** -Methode legt die Adressinformationen fest.

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

*pStartAddress* \[ in\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der die Startadresse enthält.

</dd> <dt>

*Numadkleider* \[ in\]
</dt> <dd>

Anzahl der Adressen, die für die Sitzung verwendet werden sollen.

</dd> <dt>

Gültigkeitsdauer  \[ in\]
</dt> <dd>

Gültigkeitsbereich der Gültigkeits [*Dauer*](t-tapgloss.md) (TTL) für Übertragungen der Adressen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der Parameter " *pStartAddress*", " *numadkleidungs*" oder " *TTL* " ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                  |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                                    |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                                   |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pStartAddress* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itconnection**](itconnection.md)
</dt> </dl>

 

