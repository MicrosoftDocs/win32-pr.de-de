---
description: Die Create-Methode erstellt ein neues Medium mit Standardeigenschaften, fügt es der Sammlung am angegebenen Index hinzu und gibt einen Zeiger auf die ITMedia-Schnittstelle zurück.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: ITMediaCollection::Create-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a2b11624b6a22a9bf1bff7b87538d3c7e915892a4ec7b816ee3d6c4d03821d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060868"
---
# <a name="itmediacollectioncreate-method"></a>ITMediaCollection::Create-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Create-Methode** erstellt ein neues Medium mit Standardeigenschaften, fügt es der Sammlung am angegebenen Index hinzu und gibt einen Zeiger auf die [**ITMedia-Schnittstelle**](itmedia.md) zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Index für das neue Element. Der Mindestwert für den Index ist 1, und der maximale Wert für den Index ist die aktuelle Anzahl von Elementen + 1.

</dd> <dt>

*ppMedia* \[ out\]
</dt> <dd>

Zeiger auf erstellte [**ITMedia-Schnittstelle.**](itmedia.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppMedia-Parameter* ist kein gültiger Zeiger.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Index-Parameter* ist ungültig.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die meisten C- und C++-Listen sind 0-basiert, aber dieser Index basiert aus Visual Basic Kompatibilität auf 1, was bedeutet, dass das erste Element eine Indexnummer von 1 hat.

TAPI ruft die **AddRef-Methode** auf der [**ITMedia-Schnittstelle**](itmedia.md) auf, die von **ITMediaCollection::Create** zurückgegeben wird. Die Anwendung muss **Release** auf der [**ITMedia-Schnittstelle**](itmedia.md) aufrufen, um zugeordnete Ressourcen freizugeben.

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

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




