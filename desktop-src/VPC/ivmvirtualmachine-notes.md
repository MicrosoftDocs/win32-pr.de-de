---
title: IVMVirtualMachine Notes-Eigenschaft (VPCCOMInterfaces.h)
description: Hinweise für den virtuellen Computer.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Notes-Eigenschaft Virtueller PC
- Notes-Eigenschaft Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC , Notes-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6e5e492330286bd60175983895a39ad7b0c91997f7fd36c966647d530a91c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471510"
---
# <a name="ivmvirtualmachinenotes-property"></a>IVMVirtualMachine::Notes-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Hinweise für den virtuellen Computer ab und legt sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die Hinweise für den virtuellen Computer an. Die maximale Länge der Zeichenfolge beträgt 65.536 Zeichen.

Um Notizen zu entfernen, übergeben Sie eine leere Zeichenfolge.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                       |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>                                          |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>      | Der Parameter ist ungültig oder enthält mehr als 65.536 Zeichen.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

