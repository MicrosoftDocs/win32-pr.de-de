---
title: Iconnectionbrokerclient gettargetinfo-Methode (cbclient. h)
description: Fordert Informationen über den Zielcomputer an, an den die Verbindung umgeleitet werden soll.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Gettargetinfo-Methode Remotedesktopdienste
- Gettargetinfo-Methode Remotedesktopdienste, iconnectionbrokerclient-Schnittstelle
- Iconnectionbrokerclient-Schnittstelle Remotedesktopdienste, gettargetinfo-Methode
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
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517369"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>Iconnectionbrokerclient:: gettargetinfo-Methode

Fordert Informationen über den Zielcomputer an, an den die Verbindung umgeleitet werden soll. Diese Methode wird vom Redirector verwendet, um Umleitungs Informationen für die eingehende Verbindungsanforderung zu erhalten.

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

*pconnectioninfo* \[ in\]
</dt> <dd>

Die Adresse einer [**CB- \_ Verbindungs \_**](cb-connection-info.md) Informationsstruktur, die Informationen über die eingehende Verbindungsanforderung enthält.

</dd> <dt>

*Reserviert* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss NULL sein.

</dd> <dt>

*hstatus usevent* \[ in\]
</dt> <dd>

Das Handle eines Ereignisses, das festgelegt wird, wenn ein Update für den Fortschritt der Anforderung vorliegt. Sie sind dafür verantwortlich, dieses Ereignis zu erstellen und zu schließen.

</dd> <dt>

*ptargetinfo* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer [**CB- \_ Ziel \_**](cb-target-info.md) Informationsstruktur, die Informationen über den Zielcomputer empfängt, an den die eingehende Verbindung umgeleitet werden soll. Da es sich hierbei um eine asynchrone Methode handelt, muss dieser Arbeitsspeicher verfügbar bleiben, bis die Anforderung beendet ist. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*pResult* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer **DWORD** -Variablen, die einen Ergebniscode empfängt. Da es sich hierbei um eine asynchrone Methode handelt, muss dieser Arbeitsspeicher verfügbar bleiben, bis die Anforderung beendet ist. Weitere Informationen finden Sie in den Hinweisen.

Bei diesem Ergebniscode handelt es sich um einen der folgenden Werte.

<dt>

0
</dt> <dd>

Erfolg.

</dd> <dt>

0x0000400
</dt> <dd>

Der Zielcomputer konnte nicht gefunden werden.

</dd> <dt>

0x0000401
</dt> <dd>

Der Zielcomputer ist nicht verfügbar.

</dd> <dt>

0x0000402
</dt> <dd>

Fehler beim Laden des Ziel Computers.

</dd> <dt>

0x0000403
</dt> <dd>

Fehler beim Online schalten des Ziel Computers.

</dd> <dt>

0x0000404
</dt> <dd>

Fehler beim Umleiten an den Zielcomputer.

</dd> <dt>

0x0000405
</dt> <dd>

Fehler beim Reaktivieren des virtuellen Computers.

</dd> <dt>

0x0000406
</dt> <dd>

Fehler beim Starten des virtuellen Computers.

</dd> <dt>

0x0000407
</dt> <dd>

Fehler beim Ermitteln der IP-Adresse des virtuellen Computers.

</dd> <dt>

0x0000408
</dt> <dd>

Der Sitzungs Broker konnte keine verfügbaren Computer im Pool finden.

</dd> <dt>

0x0000409
</dt> <dd>

Der Sitzungs Broker hat die Verbindung abgebrochen.

</dd> <dt>

0x0000410
</dt> <dd>

Der Sitzungs Broker konnte die Verbindungseinstellungen nicht überprüfen.

</dd> </dl> </dd> <dt>

*ppcbreq* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines [**iconnectionbrokerrequest**](iconnectionbrokerrequest.md) -Schnittstellen Zeigers, den Sie zum Abrufen von Statusaktualisierungen für einen asynchronen Vorgang verwenden. Diese Schnittstelle wird in Verbindung mit dem *hstatus usevent* -Parameter verwendet, um darauf zu warten und die Ergebnisse dieses asynchronen Vorgangs zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **E \_ Pending** " zurück, wenn die asynchrone Anforderung erstellt wird. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist asynchron. Der *ptargetinfo* -Parameter und der *pResult* -Parameter müssen gültig bleiben, bis die **CB- \_ Status \_ Anforderung \_** von der [**iconnectionbrokerrequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) -Methode abgerufen wurde.

Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Verwenden der Remotedesktopverbindung Broker-Client-API](use-the-remote-desktop-connection-broker-client-api.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Header<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconnectionbrokerclient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





