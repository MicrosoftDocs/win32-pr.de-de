---
description: Überprüft, ob die Replikation vom aktuellen Hostsystem zum angegebenen Wiederherstellungssystem aktiviert werden kann.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: TestReplicationConnection-Methode der Msvm_ReplicationService-Klasse
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
ms.openlocfilehash: 729412ea2b506aedf09bcc77385c4c8b22d560d8cd8e6fc88b12c059c0bf049c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050380"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>TestReplicationConnection-Methode der Msvm \_ ReplicationService-Klasse

Überprüft, ob die Replikation vom aktuellen Hostsystem zum angegebenen Wiederherstellungssystem aktiviert werden kann.

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

*RecoveryConnectionPoint* \[ In\]
</dt> <dd>

Der Name des Verbindungspunkts. Bei einem Wiederherstellungscluster ist dies der Broker-CAP-Name. Bei einem eigenständigen Wiederherstellungsserver ist dies der Hostsystemname.

</dd> <dt>

*RecoveryServerPortNumber* \[ In\]
</dt> <dd>

Die Portnummer des Wiederherstellungsverbindungspunkts.

</dd> <dt>

*AuthenticationType* \[ In\]
</dt> <dd>

Das Wiederherstellungsauthentifizierungsschema. Dies muss einer der folgenden Werte sein.

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrierte Authentifizierung** (1)


</dt> <dd>

Kerberos-Authentifizierung.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Zertifikatbasierte Authentifizierung** (2)


</dt> <dd>

Zertifikatbasierte Authentifizierung.

</dd> </dl> </dd> <dt>

*CertificateThumbPrint* \[ In\]
</dt> <dd>

Zertifikatfingerabdruck, der verwendet werden soll, wenn der *AuthenticationType-Parameter* die zertifikatbasierte Authentifizierung ist.

</dd> <dt>

*BypassProxyServer* \[ In\]
</dt> <dd>

Umgehen Sie den Proxyserver, wenn Sie eine Verbindung mit dem Replikatserver herstellen.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

