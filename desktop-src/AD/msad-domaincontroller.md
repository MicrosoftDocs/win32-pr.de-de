---
title: MSAD_DomainController-Klasse
description: Stellt den Domänencontroller (DC) dar, auf dem der WMI-Anbieter ausgeführt wird.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController Active Directory-Klasse
- MSAD_DomainController Active Directory-Klasse beschrieben
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a428d1c852d93fb34bfc3188219bd8ffdc5020ae65c5f9191c44d075b603a143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186085"
---
# <a name="msad_domaincontroller-class"></a>MSAD \_ DomainController-Klasse

Stellt den Domänencontroller (DC) dar, auf dem der WMI-Anbieter ausgeführt wird.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a>Member

Die **MSAD \_ DomainController-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSAD \_ DomainController-Klasse** verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | Ruft die Wissenskonsistenzprüfung auf, um die Replikationstopologie zu überprüfen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ DomainController-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den allgemeinen Namen des Serverobjekts ab.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den X.500-Pfad des [**NTDS-DSA-Objekts**](/windows/desktop/ADSchema/c-ntdsdsa) ab.

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob der Locatordienst auf dem Domänencontroller ordnungsgemäß angibt. **TRUE,** wenn der Locatordienst auf dem Domänencontroller ordnungsgemäß ankanzeiget; Andernfalls **FALSE**.

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob der DC ein globaler Katalogserver ist. **TRUE,** wenn der DC ein globaler Katalogserver ist; Andernfalls **FALSE**.

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob der DC einen anderen RID-Pool abgerufen hat. **TRUE,** wenn der DC einen weiteren RID-Pool erhalten hat und die Zuordnung von RIDs auf diesem DC fortgesetzt werden kann, auch wenn der aktuelle Pool von RIDs erschöpft ist; Andernfalls **FALSE**.

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob der DC ordnungsgemäß im DNS registriert ist. **TRUE,** wenn der DC ordnungsgemäß im DNS registriert ist; Andernfalls **FALSE**.

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob sysVol ordnungsgemäß veröffentlicht wurde. **TRUE,** wenn SysVol ordnungsgemäß veröffentlicht wurde; Andernfalls **FALSE**.

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die GUID ab, die dem [**NTDS-DSA-Objekt**](/windows/desktop/ADSchema/c-ntdsdsa) im Konfigurationscontainer zugeordnet ist. Das **NTDS-DSA-Objekt** stellt den Active Directory-Domäne Dienst-DSA-Prozess auf dem Server dar.

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Prozentsatz der RIDs ab, die im aktuellen RID-Pool auf diesem DC übrig bleiben.

</dd> <dt>

**Sitename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Standort ab, an dem der DC vorhanden ist.

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikationshinzufügevorgangs ab, der sich noch in der Warteschlange auf diesem Domänencontroller befindet.

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikationslöschvorgangs ab, der sich noch in der Warteschlange auf diesem Domänencontroller befindet.

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikations-Änderungsvorgangs ab, der sich noch in der Warteschlange auf diesem Domänencontroller befindet.

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikationssynchronisierungsvorgangs ab, der sich noch in der Warteschlange auf diesem Domänencontroller befindet.

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikationsaktualisierungsvorgangs ab, der sich noch in der Warteschlange auf diesem Domänencontroller befindet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

