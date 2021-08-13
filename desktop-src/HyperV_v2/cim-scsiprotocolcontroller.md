---
description: Stellt einen Protokollcontroller dar, der eine SCSI-Schnittstelle verwaltet.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: CIM_SCSIProtocolController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f7e3db8cb1d0aa97446d503aff876c0270ddb16e5908b3b1c53c899c7617a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647675"
---
# <a name="cim_scsiprotocolcontroller-class"></a>CIM \_ SCSIProtocolController-Klasse

Stellt einen Protokollcontroller dar, der eine SCSI-Schnittstelle verwaltet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a>Member

Die **CIM \_ SCSIProtocolController-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SCSIProtocolController-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**", "**CIM \_ SCSIProtocolController**.**OtherNameFormat**")
</dt> </dl>

Das Format der **Name-Eigenschaft** des **\_ CIM-SCSIProtocolControllers.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

**FC Port WWN** (2)


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

**iSCSI-Name** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**", "**CIM \_ SCSIProtocolController**.**NameFormat**")
</dt> </dl>

Eine Beschreibung der **NameFormat-Eigenschaft,** wenn **NameFormat** auf "1" (andere) festgelegt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ ProtocolController**](cim-protocolcontroller.md)
</dt> </dl>

 

