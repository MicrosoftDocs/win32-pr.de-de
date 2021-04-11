---
title: Ivmvirtualmachine-Name-Eigenschaft (vpccominterfaces. h)
description: Der Name der Konfiguration der virtuellen Maschine.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Name-Eigenschaft virtueller PC
- Name-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Name-Eigenschaft
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
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104102"
---
# <a name="ivmvirtualmachinename-property"></a>Ivmvirtualmachine:: Name-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Namen der Konfiguration der virtuellen Maschine ab und legt ihn fest.

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

Gibt den Namen der Konfiguration der virtuellen Maschine an. Die Länge des Namens darf nicht mehr als 80 Zeichen betragen, und die Gesamtlänge des voll qualifizierten Pfads, der die Konfigurationsdatei für den virtuellen Computer enthält, darf nicht größer als der **Maximale \_ Pfad** (260) sein.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                    | Bedeutung                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                       | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                         | Der-Parameter ist **null**.<br/>                                                           |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>                      | Der-Parameter ist ungültig oder eine leere Zeichenfolge.<br/>                                    |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>                 | Die Konfiguration ist unbekannt.<br/>                                                        |
| <dl> <dt>VM \_ E \_ Pref- \_ VM \_ aktiv</dt> <dt>0xa0040302</dt> </dl>            | Der virtuelle Computer wird ausgeführt oder gespeichert.<br/>                                             |
| <dl> <dt>VM \_ E \_ config \_ No \_ Name</dt> <dt>0xa0040400</dt> </dl>            | Der *virtualmachinename* -Parameter ist leer.<br/>                                         |
| <dl> <dt>VM \_ E- \_ Konfigurations \_ Name \_ zu \_ lang</dt> <dt>0xa00400401</dt> </dl>    | Der-Parameter enthält zu viele Zeichen.<br/>                                          |
| <dl> <dt>VM \_ E- \_ Konfigurations \_ Name ist \_ ungültig \_ char</dt> <dt>0xa0040402</dt> </dl> | Der-Parameter enthält eines der folgenden ungültigen Zeichen \* : "?: <>/ \| \\ " ".<br/> |
| <dl> <dt>VM \_ E \_ config \_ Duplicate \_ Name</dt> <dt>0xa0040403</dt> </dl>     | Der angegebene Name ist bereits als Name eines anderen virtuellen Computers vorhanden.<br/>            |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                 | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



## <a name="remarks"></a>Bemerkungen

Bei den Namen der virtuellen Computer wird die Groß-/Kleinschreibung nicht beachtet, z. b. "MyVM" und "MyVM" verweisen auf denselben virtuellen Computer. Dies ist die Standard Eigenschaft für [**ivmvirtualmachine**](ivmvirtualmachine.md).

Wenn VPC.exe ausgeführt wird und die VM gespeichert wird, wird das Festlegen der **Name** -Eigenschaft nicht erfolgreich ausgeführt. Wenn VPC.exe nicht ausgeführt wird und die VM gespeichert wird, ist das Festlegen der **Name** -Eigenschaft erfolgreich, wenn VPC.exe das nächste Mal gestartet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

