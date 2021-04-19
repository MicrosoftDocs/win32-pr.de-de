---
description: Die get \_ sessionversion-Methode ruft den 32-Bit-Wert (idealerweise Network Time Protocol oder NTP) ab, der als Sitzungs Version fungiert.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Itsdp:: get_SessionVersion-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372014"
---
# <a name="itsdpget_sessionversion-method"></a>Itsdp:: get \_ sessionversion-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ sessionversion** -Methode ruft den 32-Bit-Wert (idealerweise Network Time Protocol oder NTP) ab, der als Sitzungs Version fungiert. Obwohl dies bei der Erstellung der Sitzung automatisch generiert wird, ist der Benutzer dafür verantwortlich, ihn zu ändern, wenn der SDP geändert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psessionversion* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Sitzungs Versions Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *psessionversion* -Parameter ist ungültig.<br/>           |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *psessionversion* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>    |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                      |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert dieser Methode kann **ulong** lauten, Visual Basic den **ulong** -Typ jedoch nicht unterstützt. Ein **Double** ist der nächste kleinste Typ, der den gesamten erforderlichen Wertebereich umfasst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itsdp**](itsdp.md)
</dt> <dt>

[**Itsdp::p UT \_ sessionversion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




