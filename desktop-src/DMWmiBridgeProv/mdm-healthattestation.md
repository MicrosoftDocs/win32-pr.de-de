---
title: MDM_HealthAttestation-Klasse
description: Die MDM HealthAttestation-Klasse ermöglicht IT-Managern von Unternehmen, die Integrität verwalteter Geräte zu bewerten \_ und Unternehmensrichtlinienaktionen durchzuführen.
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
ms.openlocfilehash: 81d1ebf7e4df529c54dc3af125e87569ea0d300f8bb6de3a42e5b670dc43cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165813"
---
# <a name="mdm_healthattestation-class"></a>MDM \_ HealthAttestation-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ HealthAttestation-Klasse** ermöglicht IT-Managern von Unternehmen, die Integrität verwalteter Geräte zu bewerten und Unternehmensrichtlinienaktionen durchzuführen.

Im Folgenden finden Sie eine Liste der Funktionen, die vom HealthAttestation-CSP ausgeführt werden:

-   Sammelt Daten, die zum Überprüfen des Integritätszustands eines Gerätes verwendet werden.
-   Weiterleitung der Daten an den Integritätsnachweisdienst (Health Attestation Service, HAS)
-   Gibt das Integritätsnachweiszertifikat an, das von HAS empfangen wird.
-   Auf Anforderung werden das Integritätsnachweiszertifikat (von HAS empfangen) und die zugehörigen Laufzeitinformationen zur Überprüfung an den MDM-Server weitergeleitet.

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

Die **MDM \_ HealthAttestation-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MDM \_ HealthAttestation-Klasse** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**VerifyHealthMethod**](mdm-healthattestation-verifyhealthmethod.md) | Methode zum Benachrichtigen des Geräts, um eine Anforderung zur Überprüfung des Integritätszertifikats vorzubereiten.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MDM \_ HealthAttestation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[Zertifikat](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **Oktettzeichenfolge**
</dt> </dl>

</dd> <dt>

[CorrelationID](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**CurrentProtocolVersion**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

TBD

</dd> <dt>

[ForceRetriforce](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[HASEndpoint](/windows/client-management/mdm/healthattestation-csp)
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

Identifiziert den Namen des übergeordneten Knotens. Für diese Klasse ist die Zeichenfolge "HealthAttestation".

</dd> <dt>

**MaxSupportedProtocolVersion**
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

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/".

</dd> <dt>

**PreferredMaxProtocolVersion**
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

[TpmReadyStatus](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

