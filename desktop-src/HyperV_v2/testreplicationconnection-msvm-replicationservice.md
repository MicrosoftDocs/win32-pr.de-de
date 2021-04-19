---
description: Überprüft, ob die Replikation vom aktuellen Host System für das angegebene Wiederherstellungs System aktiviert werden kann.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Testreplicationconnection-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342825"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>Testreplicationconnection-Methode der MSVM- \_ replicationservice-Klasse

Überprüft, ob die Replikation vom aktuellen Host System für das angegebene Wiederherstellungs System aktiviert werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiederherstellungsconnectionpoint* \[ in\]
</dt> <dd>

Der Name des Verbindungs Punkts. Bei einem Wiederherstellungs Cluster ist dies der Name des Broker-Cap. Bei einem eigenständigen Wiederherstellungs Server handelt es sich hierbei um den Namen des Host Systems.

</dd> <dt>

*Wiederherstellserverportnummer* \[ in\]
</dt> <dd>

Die Portnummer des Wiederherstellungs Verbindungs Punkts.

</dd> <dt>

*AuthenticationType* \[ in\]
</dt> <dd>

Das Wiederherstellungs Authentifizierungsschema. Dabei muss es sich um einen der folgenden Werte handeln:

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrierte Authentifizierung** (1)


</dt> <dd>

Kerberos-Authentifizierung.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Zertifikat basierte Authentifizierung** (2)


</dt> <dd>

Zertifikat basierte Authentifizierung.

</dd> </dl> </dd> <dt>

*Certifi-ethumschlag-Druck* \[ in\]
</dt> <dd>

Der Zertifikat Fingerabdruck, der verwendet werden soll, wenn der *AuthenticationType* -Parameter eine Zertifikat basierte Authentifizierung ist.

</dd> <dt>

*Bypassproxyserver* \[ in\]
</dt> <dd>

Umgehen Sie den Proxy Server beim Herstellen einer Verbindung mit dem Replikat Server.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> </dl>

 

