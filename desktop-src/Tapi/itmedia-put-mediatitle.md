---
description: Mit der Put \_ mediatitle-Methode wird ein Text Titel für die Medien festgelegt, die von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden können. Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige BSTR-Zeichenfolge handeln.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: ITmedia::p ut_MediaTitle-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368345"
---
# <a name="itmediaput_mediatitle-method"></a>ITmedia::p UT \_ mediatitle-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **Put \_ mediatitle** -Methode wird ein Text Titel für die Medien festgelegt, die von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden können. Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige **BSTR** -Zeichenfolge handeln.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediatitle* \[ in\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der den Titel des Mediums enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pmediatitle* -Parameter ist kein gültiger Zeiger.<br/>  |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pmediatitle* -Parameter ist ungültig.<br/>            |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pmediatitle* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen. Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.

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

[**ITmedia:: get \_ mediatitle**](itmedia-get-mediatitle.md)
</dt> </dl>

 

