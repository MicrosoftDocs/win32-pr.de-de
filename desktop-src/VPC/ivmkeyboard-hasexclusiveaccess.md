---
title: IVMKeyboard HasExclusiveAccess-Eigenschaft (VPCCOMInterfaces.h)
description: Gibt an, ob dieses Objekt die exklusive Kontrolle über das Tastaturgerät des virtuellen Computers hat.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- HasExclusiveAccess-Eigenschaft Virtueller PC
- HasExclusiveAccess-Eigenschaft Virtual PC , IVMKeyboard-Schnittstelle
- IVMKeyboard-Schnittstelle Virtueller PC , HasExclusiveAccess-Eigenschaft
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c01e13e331824a0d1b6834cbb27da7eb4b5420a3cd3dbec94cdbdd494c79c95b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136723"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>IVMKeyboard::HasExclusiveAccess-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt an, ob dieses Objekt die exklusive Kontrolle über das Tastaturgerät des virtuellen Computers (VM) hat.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a>Eigenschaftswert

**TRUE,** wenn exklusiver Zugriff auf das Tastaturgerät des virtuellen Computers erworben wurde, andernfalls **FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                      | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                        | Der *isExclusive-Parameter* ist **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                   | Der angeforderte exklusive Modus ist für dieses Gerät bereits festgelegt. Dies kann passieren, wenn versucht wird, den exklusiven Modus festzulegen, wenn er bereits erworben wurde, oder wenn versucht wird, den exklusiven Modus freizugeben, wenn er zuvor nicht aktiviert wurde.<br/> |
| <dl> <dt>VM \_ E \_ SET EXCLUSIVE MODE \_ \_ \_ FAIL</dt> <dt>0xA0040825</dt> </dl> | Fehler beim Festlegen oder Freigeben des exklusiven Modus wie angefordert. Dies kann daran liegt, dass der virtuelle Computer nicht mehr ausgeführt wird oder weil ein anderer Prozess bereits den exklusiven Modus auf dem Tastaturgerät des virtuellen Computers aktiviert hat.<br/>                                 |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>                     | Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard ist als 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4 definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

