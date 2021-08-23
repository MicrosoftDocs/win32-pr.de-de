---
title: IVMDisplay CanResize-Eigenschaft (VPCCOMInterfaces.h)
description: Bestimmt, ob der Gast Auflösungsänderungen zulässt.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- CanResize-Eigenschaft Virtueller PC
- CanResize-Eigenschaft Virtueller PC, IVMDisplay-Schnittstelle
- IVMDisplay-Schnittstelle Virtueller PC, CanResize-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b55bc4ab9599b119988b68df022c098048aeee9ea19194e2c3dcbfdaefde479
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473580"
---
# <a name="ivmdisplaycanresize-property"></a>IVMDisplay::CanResize-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob der Gast Auflösungsänderungen zulässt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a>Eigenschaftswert

**VARIANT \_ TRUE,** wenn der Gast Auflösungsänderungen zulässt, andernfalls **VARIANT \_ FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                              |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                            | Der Parameter ist **NULL.**<br/>                                                                                                                 |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                    | Die Konfiguration ist unbekannt.<br/>                                                                                                              |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                                                                                    |
| <dl> <dt>VM \_ E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt> </dl>                    | Für den virtuellen Computer wurde kein Videogerät gefunden.<br/>                                                                                   |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Die Integrationskomponentenfunktion ist nicht verfügbar. entweder sind die Integrationskomponenten nicht installiert, oder das Feature wurde deaktiviert.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay ist als 960895e9-f743-4498-96aa-261f867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

