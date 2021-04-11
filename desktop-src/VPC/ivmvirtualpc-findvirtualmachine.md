---
title: Ivmvirtualpc findvirtualmachine-Methode (vpccominterfaces. h)
description: Ruft ein Objekt für virtuelle Maschinen ab, das mit der angeforderten Konfiguration übereinstimmt.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Findvirtualmachine-Methode Virtual PC
- Findvirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, findvirtualmachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105201"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a>Ivmvirtualpc:: findvirtualmachine-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft ein Objekt für virtuelle Maschinen ab, das mit der angeforderten Konfiguration übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigurationName* \[ in\]
</dt> <dd>

Der Name des virtuellen Computers, der gefunden werden soll.

</dd> <dt>

*virtualmachine* \[ Out, retval\]
</dt> <dd>

Ein Zeiger auf ein neues [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das diesen virtuellen Computer darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**S \_ Falsch**</dt> <dt>1</dt> </dl>                                           | Die angegebene Konfiguration wurde nicht gefunden.<br/>                                      |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                | Der *ConfigurationName* -Parameter ist ungültig, oder *virtualmachine* ist **null**.<br/>       |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Bei den Namen der virtuellen Computer wird die Groß-/Kleinschreibung nicht beachtet, z. b. "MyVM" und "MyVM" beziehen sich auf denselben virtuellen Computer.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc**](ivmvirtualpc.md)
</dt> </dl>

 

