---
description: Die \_ methode get Item ruft ein Element aus der Auflistung mithilfe eines Indexes ab.
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: ITTimeCollection::get_Item-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422e558c01172d80e97113f84745f86e8d304fba5bf5761ff9135fc9ee59c41b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012660"
---
# <a name="ittimecollectionget_item-method"></a>ITTimeCollection::get \_ Item-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ methode get Item** ruft ein Element aus der Auflistung mithilfe eines Indexes ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Index des abzurufende Elements.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Zeiger auf die gewünschte [**ITTime-Schnittstelle.**](ittime.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pVal-Parameter* ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Index-Parameter* ist ungültig.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die **AddRef-Methode** für die [**ITTime-Schnittstelle**](ittime.md) auf, die von I **TTimeCollection::get \_ Item** zurückgegeben wird. Die Anwendung muss **Release** auf der **ITTime-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




