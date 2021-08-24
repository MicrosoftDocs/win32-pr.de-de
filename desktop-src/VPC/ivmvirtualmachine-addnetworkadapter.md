---
title: IVMVirtualMachine AddNetworkAdapter-Methode (VPCCOMInterfaces.h)
description: Fügt dem virtuellen Computer eine Netzwerkschnittstelle hinzu.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- AddNetworkAdapter-Methode Virtueller PC
- AddNetworkAdapter-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, AddNetworkAdapter-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799aa859ab8cd2bea4da29154af00c6537bfd180b0719f6d0252b1b0ddea8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866739"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>IVMVirtualMachine::AddNetworkAdapter-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Fügt dem virtuellen Computer eine Netzwerkschnittstelle hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*networkAdapter* \[ out, retval\]
</dt> <dd>

Ein [**IVMNetworkAdapter-Objekt.**](ivmnetworkadapter.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                        |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                    | Der *networkAdapter-Parameter* ist **NULL.**<br/>          |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                        |
| <dl> <dt>**VM \_ E \_ PREF \_ ILLEGAL \_ VALUE**</dt> <dt>0xA0040301</dt> </dl>   | Es können nicht mehr als vier (4) Netzwerkadapter hinzugefügt werden.<br/> |
| <dl> <dt>**VM \_ \_E-VM, \_ AUF DER 0XA004020B AUSGEFÜHRT ODER GESPEICHERT \_ \_ WIRD**</dt> <dt></dt> </dl> | Der virtuelle Computer befindet sich in einem ausgeführten oder gespeicherten Zustand.<br/>  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Sie können einem beendeten virtuellen Computer nur eine neue Netzwerkschnittstelle hinzufügen. Der neu erstellte Netzwerkadapter ist nicht mit einem virtuellen Netzwerk verbunden.

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

 

