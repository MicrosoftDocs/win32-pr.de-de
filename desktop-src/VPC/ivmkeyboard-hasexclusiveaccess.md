---
title: Ivmkeyboard hasexclusiveaccess-Eigenschaft (vpccominterfaces. h)
description: Gibt an, ob dieses-Objekt über eine exklusive Kontrolle über das Tastatur Gerät der VM verfügt.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Hasexclusiveaccess-Eigenschaft virtueller PC
- Hasexclusiveaccess-Eigenschaft virtueller PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, hasexclusiveaccess (Eigenschaft)
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
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105680"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>Ivmkeyboard:: hasexclusiveaccess (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt an, ob dieses Objekt über eine exklusive Kontrolle über das Tastatur Gerät (VM) des virtuellen Computers verfügt.

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

**True** , wenn exklusiver Zugriff auf das Tastatur Gerät der VM abgerufen wurde, andernfalls **false** .

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                      | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                        | Der *isexclusive* -Parameter ist **null**.<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                                   | Der angeforderte exklusive Modus ist für dieses Gerät bereits festgelegt. Dies kann der Fall sein, wenn Sie versuchen, den exklusiven Modus festzulegen, wenn er bereits abgerufen wurde, oder wenn Sie den exklusiven Modus freigeben möchten, wenn er zuvor noch nicht abgerufen wurde.<br/> |
| <dl> <dt>VM \_ E \_ Set \_ Exclusive \_ Mode \_ Fail</dt> <dt>0xa0040825</dt> </dl> | Der exklusive Modus konnte nicht wie angefordert festgelegt oder freigegeben werden. Dies kann daran liegen, dass der virtuelle Computer nicht mehr ausgeführt wird oder dass ein anderer Prozess bereits exklusiven Modus auf dem Tastatur Gerät der VM erworben hat.<br/>                                 |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>                     | Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmkeyboard**](ivmkeyboard.md)
</dt> </dl>

 

