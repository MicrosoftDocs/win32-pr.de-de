---
title: Ivmvirtualmachine shutdownaktiononquit-Eigenschaft (vpccominterfaces. h)
description: Aktion, die auf dieser virtuellen Maschine ausgeführt werden soll, wenn Sie ausgeführt wird, wenn Windows Virtual PC beendet wird.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Shutdownaktiononquit-Eigenschaft, virtueller PC
- Shutdownaktiononquit-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, shutdownaktiononquit (Eigenschaft)
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
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478330"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>Ivmvirtualmachine:: shutdownaktiononquit (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Aktion ab, die auf diesem virtuellen Computer (VM) ausgeführt wird, wenn Sie ausgeführt wird, wenn Windows Virtual PC beendet wird, oder legt Sie fest.

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

Gibt an, wie diese VM heruntergefahren wird, wenn Sie ausgeführt wird, wenn Windows Virtual PC beendet wird. Eine Liste der Werte finden Sie unter [**vmshutdownaction**](vmshutdownaction.md).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                       |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null** oder kein gültiger-Wert.<br/>                     |
| <dl> <dt>E \_ AccessDenied</dt> <dt>0x80070005</dt> </dl>    | Der aktuelle Benutzer verfügt nicht über ausreichenden Zugriff auf die Konfigurationsdatei.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                       |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                   |



## <a name="remarks"></a>Bemerkungen

Standardmäßig werden virtuelle Computer, die ausgeführt werden, beim Beenden von Windows Virtual PC gespeichert. Durch die Aktion zum herunter **fahren ( \_ 0** ) wird der Zustand der VM gespeichert. Mit der Aktion " **vmshutdownaction \_ Turnoff** (1)" wird der virtuelle Computer ausgeschaltet. Durch die Aktion zum **\_ Herunterfahren von vmshutdownaction** (2) wird das Gast Betriebssystem heruntergefahren, wenn die Integrations Komponenten verfügbar sind, und andernfalls wird die VM gespeichert.

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
</dt> <dt>

[**Vmshutdownaction**](vmshutdownaction.md)
</dt> </dl>

 

