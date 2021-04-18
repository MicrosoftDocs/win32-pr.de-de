---
title: Ivmvirtualmachine-Speicher Eigenschaft (vpccominterfaces. h)
description: Menge an physischem Arbeitsspeicher auf dem virtuellen Computer in Megabyte.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Arbeitsspeicher Eigenschaft (Virtual PC)
- Arbeitsspeicher Eigenschaft virtueller PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Arbeitsspeicher (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338518"
---
# <a name="ivmvirtualmachinememory-property"></a>Ivmvirtualmachine:: memory (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Menge des physischen Speichers auf dem virtuellen Computer in Megabyte ab und legt Sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die Menge des physischen Speichers in Megabyte an.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                         | Bedeutung                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                  |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>              | Der-Parameter ist **null**.<br/>                     |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>           | Der-Parameter ist ungültig oder liegt außerhalb des zulässigen Bereichs.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                  |
| <dl> <dt>VM \_ E \_ Pref \_ nicht \_ gefunden</dt> <dt>0xa0040300</dt> </dl> | Die Einstellung wurde nicht gefunden.<br/>                  |
| <dl> <dt>VM \_ E \_ Pref- \_ VM \_ aktiv</dt> <dt>0xa0040302</dt> </dl> | Der virtuelle Computer wird ausgeführt oder gespeichert.<br/>       |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>              |



## <a name="remarks"></a>Bemerkungen

Der physische Arbeitsspeicher auf einem virtuellen Computer muss mindestens 4 MB betragen. Die Obergrenze für den Arbeitsspeicher hängt von der Host Konfiguration ab, kann jedoch höchstens 3.712 MB betragen.

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

 

