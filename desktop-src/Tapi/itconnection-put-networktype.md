---
description: Die \_ methode put NetworkType legt den Netzwerktyp fest.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: ITConnection::p ut_NetworkType-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f9d14090d04db639c95df59b051da77f2631064becff5bbb1873b37e82c745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774990"
---
# <a name="itconnectionput_networktype-method"></a>ITConnection::p ut \_ NetworkType-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ methode put NetworkType** legt den Netzwerktyp fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNetworkType* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR,** der den Netzwerktyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pNetworkType-Parameter* ist ungültig.<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Speicher für den *pNetworkType-Parameter* zu belegen, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

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
</dt> <dt>

[**ITConnection::get \_ NetworkType**](itconnection-get-networktype.md)
</dt> </dl>

 

