---
title: INapClientManagement GetSystemIsolationInfo-Methode (NapManagement.h)
description: Ruft Informationen zum Isolationsstatus von NapClient ab.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- GetSystemIsolationInfo-Methode NAP
- GetSystemIsolationInfo-Methode NAP, INapClientManagement-Schnittstelle
- INapClientManagement-Schnittstelle NAP, GetSystemIsolationInfo-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414bb5f2d193aa8f7636b94925914afb7eb123d3b497fdc50d20498fa104fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368704"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a>INapClientManagement::GetSystemIsolationInfo-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **GetSystemIsolationInfo-Methode** ruft Informationen zum Isolationsstatus des NapClient ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) die Informationen zum Isolationszustand enthält.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Flag, das angibt, ob sich eine der Verbindungen in einem unbekannten Zustand befinden soll. Wenn eines dieser Flags zutrifft, wird das Flag auf **TRUE festgelegt.** Andernfalls wird das Flag auf **FALSE festgelegt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**RPC \_ E \_ DISCONNECTED**</dt> </dl> | Der NapAgent wird nicht ausgeführt.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Die abgerufenen Isolationsinformationen spiegeln keine unbekannten Zustände wider.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





