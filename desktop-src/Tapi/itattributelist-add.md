---
description: Die Add-Methode fügt das Attribut am angegebenen Index hinzu.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'Itattributelist:: Add-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367843"
---
# <a name="itattributelistadd-method"></a>Itattributelist:: Add-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Add** -Methode fügt das Attribut am angegebenen Index hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index des hinzu zufügenden Attributs.

</dd> <dt>

*pattribute* \[ in\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der den Wert des hinzu zufügenden Attributs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *Index* -oder der *pattribute* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pattribute* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

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

 

