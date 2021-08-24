---
title: IVMDisplay Height-Eigenschaft (VPCCOMInterfaces.h)
description: Höhe der Anzeige des virtuellen Computers in Pixel.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Height-Eigenschaft Virtueller PC
- Height-Eigenschaft Virtual PC, IVMDisplay-Schnittstelle
- IVMDisplay-Schnittstelle Virtueller PC, Height-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab20a1990d16591bec284514a2d8ad7b3f2a05ea9f6fcae234037078d66f4ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654320"
---
# <a name="ivmdisplayheight-property"></a>IVMDisplay::Height-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Höhe der Anzeige des virtuellen Computers in Pixel ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Höhe in Pixel.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                         | Bedeutung                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                                 |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>              | Der Parameter ist **NULL.**<br/>                                    |
| <dl> <dt>VM \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl> | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>       |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | Der virtuelle Computer ist ungültig oder wird derzeit nicht ausgeführt.<br/> |
| <dl> <dt>VM \_ E \_ \_ KEINE</dt> <dt>0XA0040850</dt> </dl>      | Es wurde keine gültige Anzeige für den virtuellen Computer gefunden.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay ist als 960895e9-f743-4498-96aa-261f867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

