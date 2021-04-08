---
title: MDM_SecureAssessment-Klasse
description: Die MDM \_ securegutamentclass dient zum Bereitstellen von Konfigurationsinformationen für den Secure Assessment-Browser.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- MDM_SecureAssessment-Klasse
- MDM_SecureAssessment-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949447"
---
# <a name="mdm_secureassessment-class"></a>MDM \_ secureassessment-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ secureassessment**-Klasse wird verwendet, um Konfigurationsinformationen für den Secure Assessment-Browser bereitzustellen.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a>Member

Die **MDM \_ secureassessment** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ secureassessment** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Allowscreenmonitoring](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Allowtextvorschläge](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
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

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "secureassessment".

</dd> <dt>

[Launchuri](/windows/client-management/mdm/secureassessment-csp#launchuri)
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

[Requirements-Druck](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Test Konto](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                            |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. MOF</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dllfür die \\</dt> </dl> |



 

