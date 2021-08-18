---
title: IVMMouse SetButton-Methode (VPCCOMInterfaces.h)
description: Legt den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste fest.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- SetButton-Methode Virtueller PC
- SetButton-Methode Virtual PC, IVMMouse-Schnittstelle
- IVMMouse-Schnittstelle Virtueller PC, SetButton-Methode
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04bdd3d7e0075b050c5184beee0a5da21f184040a03731317f2d61e09c07fd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974110"
---
# <a name="ivmmousesetbutton-method"></a>IVMMouse::SetButton-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Legt den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*buttonIndex* \[ In\]
</dt> <dd>

Der Schaltflächenindex. Eine Liste der Werte finden Sie unter [**VMMouseButton**](vmmousebutton.md).

</dd> <dt>

*down* \[ In\]
</dt> <dd>

Der neue Schaltflächenzustand. Verwenden **Sie TRUE,** wenn der Schaltflächenzustand auf "down" festgelegt werden soll, und **FALSE,** wenn er eingerichtet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                        | BESCHREIBUNG                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | Der Vorgang wurde durchgeführt.<br/>                                                                                                          |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>             | Der *buttonIndex-Parameter* ist ungültig.<br/>                                                                                              |
| <dl> <dt>**VM \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>   | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird derzeit nicht ausgeführt.<br/>                                                   |
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

 

