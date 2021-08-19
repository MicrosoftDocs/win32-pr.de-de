---
title: IVMVirtualMachine ShutdownActionOnQuit-Eigenschaft (VPCCOMInterfaces.h)
description: Aktion, die auf diesem virtuellen Computer ausgeführt werden soll, wenn er ausgeführt wird, Windows virtueller PC beendet wird.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- ShutdownActionOnQuit -Eigenschaft Virtueller PC
- ShutdownActionOnQuit-Eigenschaft Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, ShutdownActionOnQuit -Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c859a0f1715685e07ba13d6fb06fc99dc08f712fd20fa56a4672a2cc857b1591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124700"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>IVMVirtualMachine::ShutdownActionOnQuit (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Aktion ab, die auf diesem virtuellen Computer (VM) ausgeführt werden soll, wenn er ausgeführt wird, wenn Windows virtueller PC beendet wird, und legt diese fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, wie dieser virtuelle Computer heruntergefahren wird, wenn er ausgeführt wird, Windows virtueller PC beendet wird. Eine Liste der Werte finden Sie unter [**VMShutdownAction**](vmshutdownaction.md).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                       |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der -Parameter **ist NULL** oder kein gültiger Wert.<br/>                     |
| <dl> <dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt> </dl>    | Der aktuelle Benutzer hat nicht genügend Zugriff auf die Konfigurationsdatei.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                   |



## <a name="remarks"></a>Hinweise

Standardmäßig werden ausgeführte VMs gespeichert, wenn Windows virtueller PC beendet wird. Mit der Aktion **vmShutdownAction \_ Save** (0) zum Herunterfahren wird der Status des virtuellen Computers speichern. Die **Aktion vmShutdownAction \_ TurnOff** (1) deaktiviert den virtuellen Computer. Mit **der Aktion vmShutdownAction \_ Shutdown** (2) wird das Gastbetriebssystem heruntergefahren, wenn die Integrationskomponenten verfügbar sind, und die VM wird andernfalls speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

