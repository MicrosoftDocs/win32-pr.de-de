---
description: Die Create-Methode erstellt eine neue ITTime-Komponente.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: ITTimeCollection::Create-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65949d0584f6ed41d3e1611c790b6b94dfa88a4e11ba18818974af5d38cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762372"
---
# <a name="ittimecollectioncreate-method"></a>ITTimeCollection::Create-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Create-Methode** erstellt eine neue [**ITTime-Komponente.**](ittime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Index des zu erstellenden Elements. (Das Indexarray ist einsbasiertes Array.)

</dd> <dt>

*ppTime* \[ out\]
</dt> <dd>

Zeiger auf die erstellte b-Komponente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *ppTime-Parameter* ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Index-Parameter* ist ungültig.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die **AddRef-Methode** für die [**ITTime-Schnittstelle**](ittime.md) auf, die von **ITTimeCollection::Create zurückgegeben wird.** Die Anwendung muss **Release auf der v-Schnittstelle** aufrufen, um ressourcen frei zu machen, die ihr zugeordnet sind.

Diese Funktion kann Daten unverschlüsselt über das Netzwerk senden. Aus diesem Grund kann eine Person, die im Netzwerk abhört, die Daten lesen. Das Sicherheitsrisiko des Sendens der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




