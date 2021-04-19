---
title: Inapsystemhealthagentcallback comparesohrequests-Methode (napsystemhealthagent. h)
description: Wird vom SHA zum Vergleichen von SoH-Anforderungen verwendet.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Comparesohrequests-Methode NAP
- Comparesohrequests-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, comparesohrequests-Methode
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
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338551"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>Inapsystemhealthagentcallback:: comparesohrequests-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentcallback:: comparesohrequests** -Methode wird vom SHA zum Vergleichen von SoH-Anforderungen verwendet.

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

*LHS* \[ in\]
</dt> <dd>

Ein Zeiger auf den [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) Links vom Vergleichs Vorgang.

</dd> <dt>

*RHS* \[ in\]
</dt> <dd>

Ein Zeiger auf den [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) auf der rechten Seite des Vergleichs Vorgangs.

</dd> <dt>

*IsEqual* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **booleschen** Wert, der **true** ist, wenn *LHS* und *RHS* semantisch gleich sind, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                               | Beschreibung                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Gibt die erfolgreiche Ausführung an.<br/>                         |
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Die Methode wurde nicht vom SHA implementiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Der SHA sollte die SoHs vergleichen und **true** zurückgeben, wenn die SoHs semantisch gleich sind. Der NAPAgent verwendet diese Informationen, um zu bestimmen, ob ein SoH-Austausch aufgrund einer Änderung des Zustands des Client Computers initiiert werden soll.

Wenn SHAs inkrementelle IDs oder Zeitstempel in Ihrem SoH abgelegt haben, sind SoHs möglicherweise semantisch gleich (d. h., Sie können dieselben Integritäts Informationen vermitteln), Sie können jedoch Byte Weise ungleich sein. Diese Funktion sollte von SHAs implementiert werden, um die semantische Gleichheit von SoHs zu überprüfen.

Wenn SHAs keine Zeitstempel oder IDs in ihren SoHs abgelegt haben, können Sie diese Funktion nicht implementieren und **E \_ notimpl** zurückgeben. In diesem Fall führt der NAPAgent einen Byte weisen Vergleich der [**sohrequests**](/windows/win32/api/naptypes/ns-naptypes-soh)durch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthagentcallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





