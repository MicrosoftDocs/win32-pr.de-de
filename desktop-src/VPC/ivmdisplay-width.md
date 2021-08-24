---
title: IVMDisplay Width-Eigenschaft (VPCCOMInterfaces.h)
description: Breite der VM-Anzeige in Pixel.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Width-Eigenschaft Virtueller PC
- Width-Eigenschaft Virtual PC , IVMDisplay-Schnittstelle
- IVMDisplay-Schnittstelle Virtueller PC, Width-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db106804f81f52b669b90920699761061d97fb3412dd58b761f7da1701ec53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654220"
---
# <a name="ivmdisplaywidth-property"></a>IVMDisplay::Width-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Breite der Anzeige des virtuellen Computers (VMs) in Pixel ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Breite in Pixel.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                         | Bedeutung                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                                 |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>              | Der Parameter ist **NULL.**<br/>                                    |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl> | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>       |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | Der virtuelle Computer ist ungültig oder wird derzeit nicht ausgeführt.<br/> |
| <dl> <dt>VM \_ E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt> </dl>      | Es konnte keine gültige Anzeige für den virtuellen Computer gefunden werden.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay ist als 960895e9-f743-4498-96aa-261f867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

