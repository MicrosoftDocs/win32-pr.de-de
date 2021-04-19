---
description: Die get \_ Item-Methode gibt das vom Index angegebene Attribut zurück.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'Itattributelist:: get_Item-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367805"
---
# <a name="itattributelistget_item-method"></a>Itattributelist:: get \_ Item-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ Item** -Methode gibt das vom Index angegebene Attribut zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index des zu entzurufenden Elements.

</dd> <dt>

*PVal* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der die Werte des Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *PVal* -Parameter ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *Index* -Parameter ist ungültig.<br/>                  |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *PVal* -Parameter zugeordneten Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itattributelist**](itattributelist.md)
</dt> </dl>

 

