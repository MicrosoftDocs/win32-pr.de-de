---
title: IVMMouse Click-Methode (VPCCOMInterfaces.h)
description: Simuliert einen Mausklick.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Klicken Sie auf die Methode Virtueller PC.
- Klicken Sie auf die Methode Virtual PC , IVMMouse-Schnittstelle.
- IVMMouse-Schnittstelle Virtueller PC, Click-Methode
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d1d1aaf538ac6b30a27df904729f2ad3187ebde29cb915c3d7ef35d1e9cf57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974249"
---
# <a name="ivmmouseclick-method"></a>IVMMouse::Click-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simuliert einen Mausklick.

## <a name="syntax"></a>Syntax


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*buttonIndex* \[ In\]
</dt> <dd>

Der Index der Schaltfläche, auf die geklickt wird. Eine Liste der Werte finden Sie unter [**VMMouseButton**](vmmousebutton.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                        | BESCHREIBUNG                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | Der Vorgang wurde durchgeführt.<br/>                                                                                                          |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>             | Der Parameter ist **NULL.**<br/>                                                                                                             |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ 0XA0040206**</dt> <dt></dt> </dl>   | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird derzeit nicht ausgeführt.<br/>                                                   |
| <dl> <dt>**VM \_ E \_ MOUSE NOT ACTIVE \_ \_ 0xA0040800**</dt> <dt></dt> </dl> | Der Vorgang konnte nicht abgeschlossen werden, weil das Mausgerät nicht hochgefahren wird oder derzeit auf dem virtuellen Computer nicht aktiv ist.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

