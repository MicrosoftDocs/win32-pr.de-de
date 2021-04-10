---
title: Vmlogofftype-Enumeration (vpccominterfaces. h)
description: Gibt an, wie ein virtueller Computer heruntergefahren wird.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Vmlogofftype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040564"
---
# <a name="vmlogofftype-enumeration"></a>Vmlogofftype-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt an, wie ein virtueller Computer (VM) heruntergefahren wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmlogoff \_ Normal**
</dt> <dd>

Die Abmeldung auf der Gast-VM war normal.

</dd> <dt>

<span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmlogoff \_ erzwungen**
</dt> <dd>

Die Abmeldung in der Gast-VM wurde erzwungen.

</dd> <dt>

<span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmlogoff \_ extern**
</dt> <dd>

Die Abmeldung auf der Gast-VM wurde mithilfe der [**ivmguestos:: Abmeldung**](ivmguestos-logoff.md) -Methode ausgeführt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine:: shutdownaktiononquit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

