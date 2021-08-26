---
title: IVMVirtualMachine Name-Eigenschaft (VPCCOMInterfaces.h)
description: Name der Konfiguration des virtuellen Computers.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Name-Eigenschaft Virtueller PC
- Name-Eigenschaft Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219e6fcb24805feb0370bd157d014767a9348e87e500d8c94fa26ff502b6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006800"
---
# <a name="ivmvirtualmachinename-property"></a>IVMVirtualMachine::Name-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Namen der Konfiguration des virtuellen Computers ab und legt den Namen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Namen der Konfiguration des virtuellen Computers an. Die Länge des Namens darf nicht mehr als 80 Zeichen betragen, und die Gesamtlänge des vollqualifizierten Pfads, der die Konfigurationsdatei für den VM-Namen enthält, darf nicht mehr als **MAX \_ PATH** (260) Zeichen umfassen.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                    | Bedeutung                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                       | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                         | Der Parameter ist **NULL.**<br/>                                                           |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>                      | Der -Parameter ist ungültig oder eine leere Zeichenfolge.<br/>                                    |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                 | Die Konfiguration ist unbekannt.<br/>                                                        |
| <dl> <dt>VM \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl>            | Der virtuelle Computer wird ausgeführt oder gespeichert.<br/>                                             |
| <dl> <dt>VM \_ E \_ CONFIG \_ NO \_ NAME</dt> <dt>0xA0040400</dt> </dl>            | Der *parameter virtualMachineName* ist leer.<br/>                                         |
| <dl> <dt>VM \_ E \_ CONFIG \_ NAME TOO \_ \_ LONG</dt> <dt>0xA00400401</dt> </dl>    | Der -Parameter enthält zu viele Zeichen.<br/>                                          |
| <dl> <dt>VM \_ E \_ CONFIG \_ NAME INVALID \_ \_ CHAR</dt> <dt>0xA0040402</dt> </dl> | Der -Parameter enthält eines der folgenden ungültigen Zeichen " \* ?:<>\| \\ /".<br/> |
| <dl> <dt>VM \_ E \_ CONFIG \_ DUPLICATE \_ NAME</dt> <dt>0xA0040403</dt> </dl>     | Der angegebene Name ist bereits als Name eines anderen virtuellen Computers vorhanden.<br/>            |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                 | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



## <a name="remarks"></a>Hinweise

Bei Namen virtueller Computer wird die Groß-/Kleinschreibung nicht beachtet, z. B. beziehen sich "MyVM" und "myvm" auf denselben virtuellen Computer. Dies ist die Standardeigenschaft für [**IVMVirtualMachine**](ivmvirtualmachine.md).

Wenn VPC.exe ausgeführt wird und der virtuelle Computer gespeichert wird, ist das Festlegen der **Name-Eigenschaft** nicht erfolgreich. Wenn VPC.exe nicht ausgeführt wird und der virtuelle Computer gespeichert wird, ist das Festlegen der **Name-Eigenschaft** erfolgreich, wenn VPC.exe das nächste Mal gestartet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

