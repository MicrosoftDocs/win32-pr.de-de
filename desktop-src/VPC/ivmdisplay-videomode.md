---
title: Ivmdisplay videomode-Eigenschaft (vpccominterfaces. h)
description: Ruft den aktuellen Videomodus ab.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- Videomode-Eigenschaft virtueller PC
- Videomode-Eigenschaft virtueller PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, videomode (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956421"
---
# <a name="ivmdisplayvideomode-property"></a>Ivmdisplay:: videomode (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den aktuellen Videomodus ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Der aktuelle Videomodus des Gast Betriebssystems. Eine Liste der Werte finden Sie unter [**vmdisplayvideomode**](vmdisplayvideomode.md).

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

 

