---
title: IConnectionBrokerClient GetTargetInfo-Methode (Cbclient.h)
description: Fordert Informationen zum Zielcomputer an, auf dem die Verbindung umgeleitet werden soll.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- GetTargetInfo-Remotedesktopdienste
- GetTargetInfo-Methode Remotedesktopdienste , IConnectionBrokerClient-Schnittstelle
- IConnectionBrokerClient-Schnittstelle Remotedesktopdienste , GetTargetInfo-Methode
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df214f23c09b7439843f0d7e8947d40cc32b2bf30eece887c921aac34306fbdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059188"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>IConnectionBrokerClient::GetTargetInfo-Methode

Fordert Informationen zum Zielcomputer an, auf dem die Verbindung umgeleitet werden soll. Diese Methode wird vom Redirector verwendet, um Umleitungsinformationen für die eingehende Verbindungsanforderung zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pConnectionInfo* \[ In\]
</dt> <dd>

Die Adresse einer [**CB \_ CONNECTION \_ INFO-Struktur,**](cb-connection-info.md) die Informationen über die eingehende Verbindungsanforderung enthält.

</dd> <dt>

*Reserviert* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss 0 (null) sein.

</dd> <dt>

*hStatusEvent* \[ In\]
</dt> <dd>

Das Handle eines Ereignisses, das festgelegt wird, wenn ein Update des Status der Anforderung vorkommt. Sie sind für das Erstellen und Schließen dieses Ereignisses verantwortlich.

</dd> <dt>

*pTargetInfo* \[ out\]
</dt> <dd>

Die Adresse einer [**CB \_ TARGET \_ INFO-Struktur,**](cb-target-info.md) die Informationen über den Zielcomputer empfängt, auf dem die eingehende Verbindung umgeleitet werden soll. Da es sich um eine asynchrone Methode handelt, muss dieser Arbeitsspeicher verfügbar bleiben, bis die Anforderung abgeschlossen ist. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*pResult* \[ out\]
</dt> <dd>

Die Adresse einer **DWORD-Variablen,** die einen Ergebniscode empfängt. Da es sich um eine asynchrone Methode handelt, muss dieser Arbeitsspeicher verfügbar bleiben, bis die Anforderung abgeschlossen ist. Weitere Informationen finden Sie in den Hinweisen.

Dieser Ergebniscode ist einer der folgenden Werte.

<dt>

0
</dt> <dd>

Erfolg.

</dd> <dt>

0x0000400
</dt> <dd>

Der Zielcomputer wurde nicht gefunden.

</dd> <dt>

0x0000401
</dt> <dd>

Der Zielcomputer ist nicht verfügbar.

</dd> <dt>

0x0000402
</dt> <dd>

Fehler beim Laden des Zielcomputers.

</dd> <dt>

0x0000403
</dt> <dd>

Fehler beim Online stellen des Zielcomputers.

</dd> <dt>

0x0000404
</dt> <dd>

Fehler beim Umleiten zum Zielcomputer.

</dd> <dt>

0x0000405
</dt> <dd>

Fehler beim Waking des virtuellen Computers.

</dd> <dt>

0x0000406
</dt> <dd>

Fehler beim Starten des virtuellen Computers.

</dd> <dt>

0x0000407
</dt> <dd>

Fehler beim Suchen der IP-Adresse des virtuellen Computers.

</dd> <dt>

0x0000408
</dt> <dd>

Der Sitzungsbroker konnte keine verfügbaren Computer im Pool finden.

</dd> <dt>

0x0000409
</dt> <dd>

Der Sitzungsbroker hat die Verbindung abgebrochen.

</dd> <dt>

0x0000410
</dt> <dd>

Der Sitzungsbroker konnte die Verbindungseinstellungen nicht überprüfen.

</dd> </dl> </dd> <dt>

*ppCbReq* \[ out\]
</dt> <dd>

Die Adresse eines [**IConnectionBrokerRequest-Schnittstellenzeigers,**](iconnectionbrokerrequest.md) den Sie verwenden, um Statusupdates für einen asynchronen Vorgang zu erhalten. Diese Schnittstelle wird in Verbindung mit dem *hStatusEvent-Parameter* verwendet, um auf die Ergebnisse dieses asynchronen Vorgangs zu warten und diese zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **E \_ PENDING zurück,** wenn die asynchrone Anforderung erstellt wird. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode ist asynchron. Die *Parameter pTargetInfo* und *pResult* müssen gültig bleiben, bis die [**IConnectionBrokerRequest::CheckStatus-Methode**](iconnectionbrokerrequest-checkstatus.md) **CB STATUS REQUEST COMPLETED \_ \_ \_ erhält.**

Weitere Informationen zur Verwendung dieser Methode finden Sie unter Verwenden der Remotedesktopverbindung [Broker-Client-API.](use-the-remote-desktop-connection-broker-client-api.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





