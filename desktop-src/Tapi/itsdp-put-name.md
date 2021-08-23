---
description: Die put \_ Name-Methode legt den Sitzungsnamen fest.
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: ITSdp::p ut_Name-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8b9155f4c47c0f3dfc2fe4eca27b9589187559e70a3b46e1a7c67c7339857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003238"
---
# <a name="itsdpput_name-method"></a>ITSdp::p ut \_ Name-Methode

\[Steuerelemente und Schnittstellen für Rendezvous-IP-Telefoniekonferenzen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **put \_ Name-Methode** legt den Sitzungsnamen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR,** der den Sitzungsnamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pName-Parameter* ist kein gültiger Zeiger.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Arbeitsspeicher für den *pName-Parameter* zu reservieren, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher frei zu geben, wenn die Variable nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::get \_ Name**](itsdp-get-name.md)
</dt> </dl>

 

