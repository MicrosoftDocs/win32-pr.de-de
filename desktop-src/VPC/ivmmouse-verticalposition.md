---
title: IVMMouse VerticalPosition-Eigenschaft (VPCCOMInterfaces.h)
description: Absolute y-Koordinate der Maus.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- VerticalPosition-Eigenschaft Virtueller PC
- VerticalPosition-Eigenschaft Virtueller PC, IVMMouse-Schnittstelle
- IVMMouse-Schnittstelle Virtueller PC, VerticalPosition-Eigenschaft
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f202a81e5d95909f1ec223087aceecb2a221c9836d1fcd799734f81a250141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344807"
---
# <a name="ivmmouseverticalposition-property"></a>IVMMouse::VerticalPosition-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die absolute y-Koordinate der Maus ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Eigenschaftswert

Die y-Koordinate, die die neue Position der Maus angibt. Bei Verwendung absoluter Koordinaten gibt dieser Wert die neue y-Koordinate der Maus an. Bei Verwendung relativer Koordinaten gibt dieser Wert die Anzahl der Pixel an, die die Maus in y-Richtung verschoben werden soll.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                                |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                            | Der Parameter ist **NULL.**<br/>                                                                                                                   |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird derzeit nicht ausgeführt.<br/>                                                         |
| <dl> <dt>VM \_ E \_ \_ ADDITIONSFUNKTION NICHT \_ \_ VERFÜGBAR</dt> <dt>0xA0040505</dt> </dl> | Integrationskomponenten müssen installiert werden, um die Mausposition abzurufen oder um die Mausposition festzulegen, wenn absolute Koordinaten verwendet werden.<br/>       |
| <dl> <dt>VM \_ E \_ MIT \_ \_ RELATIVEN KOORDINATEN</dt> <dt>0XA0040802</dt> </dl>   | Das Mausgerät ist derzeit für die Verwendung relativer Mauskoordinaten festgelegt.<br/>                                                                         |
| <dl> <dt>VM \_ E \_ MOUSE \_ NOT \_ ACTIVE</dt> <dt>0xA0040800</dt> </dl>             | Die absoluten Koordinaten können nicht abgerufen werden, wenn das Mausgerät nicht eingeschaltet ist oder es derzeit nicht auf dem virtuellen Computer aktiv ist.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                            |



## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann nicht abgerufen werden, wenn relative Koordinaten verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

