---
title: IVMMouse HorizontalPosition-Eigenschaft (VPCCOMInterfaces.h)
description: Absolute x-Koordinate der Maus.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- HorizontalPosition-Eigenschaft Virtueller PC
- HorizontalPosition-Eigenschaft Virtueller PC, IVMMouse-Schnittstelle
- IVMMouse-Schnittstelle Virtueller PC, HorizontalPosition-Eigenschaft
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2cb3fde1caff23845c653024d9c5e2859b0b7b5df8502dbaea167d3e969a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007150"
---
# <a name="ivmmousehorizontalposition-property"></a>IVMMouse::HorizontalPosition-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die absolute x-Koordinate der Maus ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Eigenschaftswert

Die x-Koordinate, die die neue Position der Maus angibt. Bei Verwendung absoluter Koordinaten gibt dieser Wert die neue x-Koordinate der Maus an. Bei Verwendung relativer Koordinaten gibt dieser Wert die Anzahl der Pixel an, die die Maus in x Richtung verschoben werden soll.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                                |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                            | Der Parameter ist **NULL.**<br/>                                                                                                                   |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird derzeit nicht ausgeführt.<br/>                                                         |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Integrationskomponenten müssen installiert werden, um die Mausposition abzurufen oder um die Mausposition festzulegen, wenn absolute Koordinaten verwendet werden.<br/>       |
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

