---
title: INapEnforcementClientConnection2 getisolationinfoex-Methode (natzforcementclient. h)
description: Wird verwendet, um Isolations Informationen über den Client zu erhalten.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Getisolationinfoex-Methode NAP
- Getisolationinfoex-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2 Interface NAP, getisolationinfoex-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479347"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a>INapEnforcementClientConnection2:: getisolationinfoex-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientConnection2:: getisolationinfoex** -Methode wird verwendet, um Isolations Informationen über den Client zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur, die die Konnektivität und die erweiterten Zustandsinformationen des Clients enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Informationen werden von NAPAgent nach der Verarbeitung von [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festgelegt und dürfen nicht vom-Enforcer festgelegt werden.

Der SHA muss die [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur durch Aufrufen von [**freeisolationinfoex**](freeisolationinfoex.md)freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





