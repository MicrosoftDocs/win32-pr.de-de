---
title: Inapenforcementclientconnection-Methode der Setup Methode (natzforcementclient. h)
description: Wird von NAPAgent verwendet, um die Isolations Informationen des Clients festzulegen.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Methode der Methode "stisolationinfo"
- Methode der Setup-Info-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, die Methode "Setup solationinfo"
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740928"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a>Inapenforcementclientconnection:: Setup solationinfo-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: setisolationinfo** -Methode wird vom NAPAgent verwendet, um die Isolations Informationen des Clients festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Struktur, die den konnektivitätszustand des Clients enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Informationen werden von NAPAgent nach der Verarbeitung von sohresponse festgelegt und dürfen nicht vom-Enforcer festgelegt werden.

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

[**Inapenforcementclientconnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





