---
description: Die \_ get MediaTitle-Methode ruft einen Texttitel für die Medien ab, die die Anwendung zu Informations- oder Anzeigezwecken verwenden kann. Dies muss eine ascii-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige BSTR-Zeichenfolge sein.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: ITMedia::get_MediaTitle-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e81dc2c04ee31c3c501c511c3f3bb11cc85aa90dad26e18880692ee360ffac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406060"
---
# <a name="itmediaget_mediatitle-method"></a>ITMedia::get \_ MediaTitle-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ get MediaTitle-Methode** ruft einen Texttitel für die Medien ab, die die Anwendung zu Informations- oder Anzeigezwecken verwenden kann. Dies muss eine ascii-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige **BSTR-Zeichenfolge** sein.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppMediaTitle* \[ out\]
</dt> <dd>

Zeiger auf einen **BSTR,** der den Titel des Mediums enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppMediaTitle-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppMediaTitle-Parameter* belegten Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::Put \_ MediaTitle**](itmedia-put-mediatitle.md)
</dt> </dl>

 

