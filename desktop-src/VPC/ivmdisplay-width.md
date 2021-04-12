---
title: Ivmdisplay Width-Eigenschaft (vpccominterfaces. h)
description: Breite der VM-Anzeige in Pixel.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Width Property Virtual PC
- Width-Eigenschaft Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, Width-Eigenschaft
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
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518803"
---
# <a name="ivmdisplaywidth-property"></a>Ivmdisplay:: Width-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Breite der Anzeige des virtuellen Computers (VM) in Pixel ab.

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
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>              | Der-Parameter ist **null**.<br/>                                    |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl> | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>       |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>      | Der virtuelle Computer ist ungültig oder wird zurzeit nicht ausgeführt.<br/> |
| <dl> <dt>VM \_ E \_ keine \_ Anzeige</dt> <dt>0xa0040850</dt> </dl>      | Für den virtuellen Computer kann keine gültige Anzeige gefunden werden.<br/>     |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdisplay**](ivmdisplay.md)
</dt> </dl>

 

