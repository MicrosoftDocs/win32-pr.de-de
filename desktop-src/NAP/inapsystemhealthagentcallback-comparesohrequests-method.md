---
title: INapSystemHealthAgentCallback CompareSoHRequests-Methode (NapSystemHealthAgent.h)
description: Wird vom SHA zum Vergleichen von SoH-Anforderungen verwendet.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- CompareSoHRequests-Methode NAP
- CompareSoHRequests-Methode NAP, INapSystemHealthAgentCallback-Schnittstelle
- INapSystemHealthAgentCallback-Schnittstelle NAP , CompareSoHRequests-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af26786c8ef021794876d8876ae5d8faee65b8cbbfc39b434b000ff502c64c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939435"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>INapSystemHealthAgentCallback::CompareSoHRequests-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthAgentCallback::CompareSoHRequests-Methode** wird vom SHA verwendet, um SoH-Anforderungen zu vergleichen.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ls* \[ In\]
</dt> <dd>

Ein Zeiger auf [**soHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) links vom Vergleichsvorgang.

</dd> <dt>

*rhs* \[ In\]
</dt> <dd>

Ein Zeiger auf [**soHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) rechts vom Vergleichsvorgang.

</dd> <dt>

*isEqual* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **BOOL,** die **TRUE ist,** wenn *ls* und *rhs* semantisch gleich sind, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                               | Beschreibung                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Gibt die erfolgreiche Ausführung an.<br/>                         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Die -Methode wurde vom SHA nicht implementiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Rückrufmethode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Der SHA sollte die SoHs vergleichen und **TRUE zurückgeben,** wenn die SoHs semantisch gleich sind. NapAgent verwendet diese Informationen, um zu bestimmen, ob aufgrund einer Statusänderung des Clientcomputers ein SoH-Austausch initiiert werden soll.

Wenn SHAs inkrementelle IDs oder Zeitstempel in ihren SoH-Wert setzen, sind SoHs möglicherweise semantisch gleich (d. h. sie übermitteln möglicherweise die gleichen Integritätsinformationen), sind aber möglicherweise byteweise ungleich. SHAs sollten diese Funktion implementieren, um die semantische Gleichheit von SoHs zu überprüfen.

Wenn SHAs keine Zeitstempel oder IDs in ihre SoHs setzen, können sie diese Funktion nicht implementieren und **E \_ NOTIMPL zurückgeben.** In diesem Fall führt napAgent einen byteweisen Vergleich für [**soHRequests durch.**](/windows/win32/api/naptypes/ns-naptypes-soh)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





