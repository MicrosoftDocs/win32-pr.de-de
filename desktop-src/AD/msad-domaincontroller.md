---
title: MSAD_DomainController-Klasse
description: Stellt den Domänen Controller (DC) dar, auf dem der WMI-Anbieter ausgeführt wird.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController-Klasse Active Directory
- MSAD_DomainController Klasse Active Directory, beschrieben
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
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476848"
---
# <a name="msad_domaincontroller-class"></a>MSAD \_ Domain Controller-Klasse

Stellt den Domänen Controller (DC) dar, auf dem der WMI-Anbieter ausgeführt wird.

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

Die **MSAD \_ Domain Controller** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSAD \_ Domain Controller** -Klasse verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**Executekcc**](executekcc-msad-domaincontroller.md) | Ruft die Konsistenzprüfung auf, um die Replikations Topologie zu überprüfen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ Domain Controller** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den allgemeinen Namen des Server Objekts ab.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den X. 500-Pfad des [**NTDS-DSA-**](/windows/desktop/ADSchema/c-ntdsdsa) Objekts ab.

</dd> <dt>

**Iswerben singtolocator**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den-Wert ab, der angibt, ob der Serverlocatorpunkt-Dienst auf dem Domänen Controller ordnungsgemäß Ankündigungen sendet **True** , wenn der Serverlocatorpunkt-Dienst auf dem Domänen Controller ordnungsgemäß Werbung macht. andernfalls **false**.

</dd> <dt>

**Isgc**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den-Wert ab, der angibt, ob der Domänen Controller ein globaler Katalogserver ist. **True** , wenn der Domänen Controller ein globaler Katalogserver ist. andernfalls **false**.

</dd> <dt>

**Isnextridpoolavailable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob der DC einen anderen RID-Pool abgerufen hat. **True** , wenn der Domänen Controller einen anderen RID-Pool abgerufen hat und die Zuordnung von RIDs auf diesem DC fortgesetzt werden kann, auch wenn der aktuelle Pool von RIDs erschöpft ist. andernfalls **false**.

</dd> <dt>

**Isregisteredindns**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob der DC ordnungsgemäß in DNS registriert ist. **True** , wenn der Domänen Controller ordnungsgemäß in DNS registriert ist. andernfalls **false**.

</dd> <dt>

**Issysvolready**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob SYSVOL ordnungsgemäß veröffentlicht wurde. **True** , wenn SYSVOL ordnungsgemäß veröffentlicht wurde. andernfalls **false**.

</dd> <dt>

**Ntdsaguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die GUID ab, die dem [**NTDS-DSA-**](/windows/desktop/ADSchema/c-ntdsdsa) Objekt im Konfigurations Container zugeordnet ist. Das **NTDS-DSA-** Objekt stellt den Active Directory-Domäne Dienst-DSA-Prozess auf dem Server dar.

</dd> <dt>

**Prozentuofridslinks**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Prozentsatz der RIDs ab, die im aktuellen RID-Pool auf diesem DC verbleiben.

</dd> <dt>

**Sitename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Standort ab, an dem der DC vorhanden ist.

</dd> <dt>

**Timeofoldästrepladd**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikations-Add-Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.

</dd> <dt>

**Timeofoldästrepldel**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikations Löschvorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.

</dd> <dt>

**Timeofoldästreplmod**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikations Änderungs Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.

</dd> <dt>

**Timeofoldästreplsync**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikations Synchronisierungs Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.

</dd> <dt>

**Timeofoldästreplupdrefs**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel des ältesten Replikations Aktualisierungs Vorgangs ab, der sich noch in der Warteschlange auf diesem Domänen Controller befindet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Microsoftactivedirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

