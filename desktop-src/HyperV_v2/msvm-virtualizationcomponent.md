---
description: Stellt einen Dienst der Microsoft Windows Hyper-V-Plattform dar.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Msvm_VirtualizationComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344668"
---
# <a name="msvm_virtualizationcomponent-class"></a>MSVM- \_ virtualizationcomponent-Klasse

Stellt einen Dienst der Microsoft Windows Hyper-V-Plattform dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a>Member

Die **MSVM- \_ virtualizationcomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ virtualizationcomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine **GUID** , die den Klassen Bezeichner des COM-Objekts des dienstanders darstellt.

</dd> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **experimentell**
</dt> </dl>

Der Kontext, in dem das neu erstellte-Objekt ausgeführt wird. Dieser Wert wird im *dwClsContext* -Parameter an [**cokreateingestance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)übergeben. Diese Eigenschaft ist immer auf 1 festgelegt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen. andernfalls **false**. Diese Eigenschaft ist immer auf " **true**" festgelegt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine sprachneutrale Zeichenfolge, die den Dienst eindeutig identifiziert. Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden: "Hersteller \| Komponenten \| Version". Dieser Name repräsentiert beispielsweise Version 1,0 der Microsoft emulierten Netzwerk Port Komponente: "Microsoft \| emulatednetworkportcomponent \| v 1.0".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM- \_ virtualizationcomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Ende des Supports (Client)<br/>    | Windows 8.1<br/>                                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

