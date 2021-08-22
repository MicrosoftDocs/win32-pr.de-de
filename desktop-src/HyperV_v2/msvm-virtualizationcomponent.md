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
ms.openlocfilehash: ab2d2d5652f2969ad20ee70077d23375371e3507991a16b6d5e6dda2245678ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068430"
---
# <a name="msvm_virtualizationcomponent-class"></a>Msvm \_ VirtualizationComponent-Klasse

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

Die **Msvm \_ VirtualizationComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualizationComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine **GUID,** die den Klassenbezeichner des COM-Objekts des Diensts darstellt.

</dd> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Experimentell**
</dt> </dl>

Der Kontext, in dem das neu erstellte Objekt ausgeführt wird. Dieser Wert wird im *dwClsContext-Parameter* an [**CoCreateInstance übergeben.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Diese Eigenschaft ist immer auf 1 festgelegt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** ist, dass diese Instanz aktiviert ist und zum Abschließen von Clientanforderungen verwendet werden kann. andernfalls **False.** Diese Eigenschaft ist immer auf **True festgelegt.**

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine sprachneutrale Zeichenfolge, die den Dienst eindeutig identifiziert. Das folgende Format wird empfohlen, um Namenskonflikte zu vermeiden: \| \| "Herstellerkomponentenversion". Dieser Name stellt beispielsweise Version 1.0 der Microsoft Emulated Network Port Component dar: "Microsoft \| EmulatedNetworkPortComponent \| V1.0".

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ VirtualizationComponent-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Ende des Supports (Client)<br/>    | Windows 8.1<br/>                                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

