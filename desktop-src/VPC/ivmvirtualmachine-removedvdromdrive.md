---
title: IVMVirtualMachine RemoveDVDRIVEDrive-Methode (VPCCOMInterfaces.h)
description: Entfernt das angegebene CD- oder DVD-Laufwerk vom virtuellen Computer.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- RemoveDVDRIVEDrive-Methode Virtueller PC
- RemoveDVCHINDrive-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, RemoveDVAFFINDrive-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 693d8eebe30c347b41a2b9b0b115c09f6fea75cd8744baa97aa3aca5cd0d1916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752279"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a>IVMVirtualMachine::RemoveDV INTRADRIVE-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Entfernt das angegebene CD- oder DVD-Laufwerk vom virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dvdDrive* \[ In\]
</dt> <dd>

Das zu entfernende Laufwerk.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | Beschreibung                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                              |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                    | Der Parameter ist **NULL.**<br/>                                 |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                              |
| <dl> <dt>**VM \_ \_E-VM, \_ AUF DER 0XA004020B AUSGEFÜHRT ODER GESPEICHERT \_ \_ WIRD**</dt> <dt></dt> </dl> | Der virtuelle Computer befindet sich in einem ausgeführten oder gespeicherten Zustand.<br/>        |
| <dl> <dt>**VM \_ E \_ LAUFWERK \_ UNGÜLTIGE**</dt> <dt>0xA0040502</dt> </dl>         | Das angegebene Laufwerk ist nicht mit diesem Busstandort verbunden.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                          |



 

## <a name="remarks"></a>Hinweise

Sie können nur ein vorhandenes CD- oder DVD-Laufwerk von einem beendeten virtuellen Computer entfernen.

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

 

