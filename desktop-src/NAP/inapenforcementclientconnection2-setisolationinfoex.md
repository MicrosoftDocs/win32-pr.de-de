---
title: INapEnforcementClientConnection2-Methode für die Methode "abtisolationinfoex" (natzforcementclient. h)
description: Wird von NAPAgent verwendet, um die Isolations Informationen für den Client festzulegen.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- Methode der Methode "stisolationinfoex"
- Methode von "stisolationinfoex", INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2-Schnittstelle NAP, Methode "-Methode"
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340018"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a>INapEnforcementClientConnection2:: abtisolationinfoex-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientConnection2:: setisolationinfoex** -Methode wird von NAPAgent verwendet, um die Isolations Informationen für den Client festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur, die den konnektivitätszustand des Clients enthält.

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

 

 





