---
title: Ivmmouse VerticalPosition-Eigenschaft (vpccominterfaces. h)
description: Absolute y-Koordinate der Maus.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- VerticalPosition-Eigenschaft virtueller PC
- VerticalPosition-Eigenschaft Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, VerticalPosition (Eigenschaft)
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
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957118"
---
# <a name="ivmmouseverticalposition-property"></a>Ivmmouse:: VerticalPosition (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

Die y-Koordinate, die die neue Position der Maus angibt. Wenn Sie absolute Koordinaten verwenden, gibt dieser Wert die neue y-Koordinate der Maus an. Wenn relative Koordinaten verwendet werden, gibt dieser Wert die Anzahl der Pixel an, die die Maus in der y-Richtung verschoben werden soll.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                                |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                            | Der-Parameter ist **null**.<br/>                                                                                                                   |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl>               | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.<br/>                                                         |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> " </dl> | Integrations Komponenten müssen installiert sein, um die Mausposition abzurufen, oder die Mausposition bei der Verwendung absoluter Koordinaten festzulegen.<br/>       |
| <dl> <dt>VM \_ E \_ verwenden \_ relativer \_ Koordinaten</dt> <dt>0xa0040802</dt> </dl>   | Das Mausgerät ist derzeit auf die Verwendung relativer Maus Koordinaten festgelegt.<br/>                                                                         |
| <dl> <dt>VM \_ E \_ Maus \_ nicht \_ aktiv</dt> <dt>0xa0040800</dt> </dl>             | Die absoluten Koordinaten können nicht abgerufen werden, wenn das Mausgerät nicht eingeschaltet ist oder wenn es auf dem virtuellen Computer zurzeit nicht aktiv ist.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                            |



## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nicht abgerufen werden, wenn relative Koordinaten verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmmouse**](ivmmouse.md)
</dt> </dl>

 

