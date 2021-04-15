---
description: Ruft die System Zertifikate auf einem Host System ab.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Getsystemzertifikate-Methode der Msvm_ReplicationService-Klasse
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
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525241"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a>Getsystemzertifikate-Methode der MSVM \_ replicationservice-Klasse

Ruft die System Zertifikate auf einem Host System ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Encodzertifikate* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung empfängt die Zertifikate, die im persönlichen Speicher für den lokalen Computer verfügbar sind. Jeder Eintrag ist eine Basis 64-codierte Zertifikat Zeichenfolge. Diese Zeichenfolge kann in ein Bytearray konvertiert werden, indem ein X509Certificate2-Objekt erstellt wird.

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

Das **System wird verwendet** (32774).
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

 

 




