---
description: Die get \_ mediatitle-Methode ruft einen Text Titel für die Medien ab, der von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden kann. Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige BSTR-Zeichenfolge handeln.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'ITmedia:: get_MediaTitle-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364707"
---
# <a name="itmediaget_mediatitle-method"></a>ITmedia:: get \_ mediatitle-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ mediatitle** -Methode ruft einen Text Titel für die Medien ab, der von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden kann. Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige **BSTR** -Zeichenfolge handeln.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppmediatitle* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der den Titel des Mediums enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppmediatitle* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, der dem *ppmediatitle* -Parameter zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITmedia**](itmedia.md)
</dt> <dt>

[**ITmedia::P UT \_ mediatitle**](itmedia-put-mediatitle.md)
</dt> </dl>

 

