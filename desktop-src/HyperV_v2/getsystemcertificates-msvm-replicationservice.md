---
description: Ruft die Systemzertifikate auf einem Hostsystem ab.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: GetSystemCertificates-Methode der Msvm_ReplicationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bdc3fe1e2a12809dceb14a23e087d3e844f5e1a51401171b68dfe41303739c2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253620"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a>GetSystemCertificates-Methode der Msvm \_ ReplicationService-Klasse

Ruft die Systemzertifikate auf einem Hostsystem ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncodedCertificates* \[ out\]
</dt> <dd>

Falls erfolgreich, empfängt die Zertifikate, die aus dem persönlichen Speicher für den lokalen Computer verfügbar sind. Jeder Eintrag ist eine Base64-codierte Zertifikatzeichenfolge. Diese Zeichenfolge kann durch Erstellen eines X509Certificate2-Objekts in ein Bytearray konvertiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
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

**Ungültiger** Parameter (32773)
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

 




