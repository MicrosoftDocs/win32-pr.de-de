---
description: Die \_ put MediaTitle-Methode legt einen Texttitel für die Medien fest, die die Anwendung zu Informations- oder Anzeigezwecken verwenden kann. Dies muss eine ascii-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige BSTR-Zeichenfolge sein.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: ITMedia::p ut_MediaTitle-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd07111cfa737be7ec5750a147ffd8d598e68b819f27f03a901a01fd66fbfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682750"
---
# <a name="itmediaput_mediatitle-method"></a>ITMedia::p ut \_ MediaTitle-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ put MediaTitle-Methode** legt einen Texttitel für die Medien fest, die die Anwendung zu Informations- oder Anzeigezwecken verwenden kann. Dies muss eine ascii-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige **BSTR-Zeichenfolge** sein.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaTitle* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR,** der den Titel des Mediums enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pMediaTitle-Parameter* ist kein gültiger Zeiger.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pMediaTitle-Parameter* ist ungültig.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Speicher für den *pMediaTitle-Parameter* zuzuordnen, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

Diese Funktion kann Daten über das Kabel in unverschlüsselter Form senden. Daher kann eine Person, die im Netzwerk lauscht, die Daten lesen. Das Sicherheitsrisiko beim Senden der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

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

[**ITMedia::get \_ MediaTitle**](itmedia-get-mediatitle.md)
</dt> </dl>

 

