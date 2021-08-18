---
description: Die put \_ MediaName-Methode legt den Mediennamen fest. Definierte Medien sind Audio, Video, Whiteboard, Text und Daten.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: ITMedia::p ut_MediaName-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d77ffde28406b7fb527ed8679d1f65d6aba537e611b69d1ad31e8679f59fd0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003338"
---
# <a name="itmediaput_medianame-method"></a>ITMedia::p ut \_ MediaName-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **put \_ MediaName-Methode** legt den Mediennamen fest. Definierte Medien sind Audio, Video, Whiteboard, Text und Daten.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaName* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR,** der den festgelegten Mediennamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pMediaName-Parameter* ist kein gültiger Zeiger.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Arbeitsspeicher für den *pMediaName-Parameter* zu reservieren, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher frei zu geben, wenn die Variable nicht mehr benötigt wird.

Diese Funktion kann Daten unverschlüsselt über das Netzwerk senden. Aus diesem Grund kann eine Person, die im Netzwerk abhört, die Daten lesen. Das Sicherheitsrisiko des Sendens der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ MediaName**](itmedia-get-medianame.md)
</dt> </dl>

 

