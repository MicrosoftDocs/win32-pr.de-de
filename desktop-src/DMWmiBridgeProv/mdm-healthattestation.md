---
title: MDM_HealthAttestation-Klasse
description: Die MDM \_ healthattestation-Klasse ermöglicht IT-Managern von Unternehmen, die Integrität verwalteter Geräte zu bewerten und Unternehmensrichtlinien Aktionen auszuführen.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- MDM_HealthAttestation-Klasse
- MDM_HealthAttestation-Klasse, beschrieben
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476041"
---
# <a name="mdm_healthattestation-class"></a>MDM \_ healthattestation-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ healthattestation** -Klasse ermöglicht IT-Managern von Unternehmen, die Integrität verwalteter Geräte zu bewerten und Unternehmensrichtlinien Aktionen auszuführen.

Im folgenden finden Sie eine Liste der Funktionen, die vom healthattestation-CSP ausgeführt werden:

-   Sammelt Daten, die zum Überprüfen von Integritäts Zuständen von Geräten verwendet werden.
-   Weiterleitung der Daten an den Integritätsnachweisdienst (Health Attestation Service, HAS)
-   Stellt das Integritäts Nachweis Zertifikat bereit, das von empfangen wird.
-   Bei der Anforderung leitet das Health Attestation-Zertifikat (von hat) und zugehörige Laufzeitinformationen zur Überprüfung an den MDM-Server weiter.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a>Member

Die **MDM \_ healthattestation** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MDM \_ healthattestation** -Klasse verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Verifyhealthmethod**](mdm-healthattestation-verifyhealthmethod.md) | Methode, mit der das Gerät benachrichtigt wird, dass eine Integritäts Zertifikat Überprüfung vorbereitet werden soll.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MDM \_ healthattestation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Certificate](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

**Qualifizierer: octetstring**
</dt> </dl>

</dd> <dt>

[CorrelationID](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**Currentprotocolversion**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

TBD

</dd> <dt>

[Forceretrieve](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Hasendpoint](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "healthattestation".

</dd> <dt>

**Maxsupportedprotocolversion**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

TBD

</dd> <dt>

[Nonce](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".

</dd> <dt>

**Preferredmaxprotocolversion**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

TBD

</dd> <dt>

[Status](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[TPM-Status](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

