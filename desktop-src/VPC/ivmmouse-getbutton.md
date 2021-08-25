---
title: IVMMouse GetButton-Methode (VPCCOMInterfaces.h)
description: Ruft den aktuellen Zustand der angegebenen Maustaste ab.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- GetButton-Methode Virtueller PC
- GetButton-Methode Virtual PC , IVMMouse-Schnittstelle
- IVMMouse-Schnittstelle Virtueller PC, GetButton-Methode
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af37a303c90fb9c60020f19f22767ec508c53fdc54bcefa533dabc780c38f16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007160"
---
# <a name="ivmmousegetbutton-method"></a>IVMMouse::GetButton-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*buttonIndex* \[ In\]
</dt> <dd>

Der Index der Schaltfläche, deren Zustand angefordert wird. Eine Liste der Werte finden Sie unter [**VMMouseButton**](vmmousebutton.md).

</dd> <dt>

*isDown* \[ out, retval\]
</dt> <dd>

Der Zustand der angegebenen Schaltfläche. **TRUE,** wenn die Schaltfläche derzeit auf dem virtuellen Computer nicht angezeigt wird, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                        | Beschreibung                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                | Der *isDown-Parameter* ist **NULL.**<br/>                                                  |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>             | Der *buttonIndex-Parameter* ist ungültig.<br/>                                            |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,**</dt> <dt>0xA0040206</dt> </dl>   | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird derzeit nicht ausgeführt.<br/> |
| <dl> <dt>**VM \_ E \_ MOUSE \_ NOT \_ ACTIVE**</dt> <dt>0xA0040800</dt> </dl> | Das Mausgerät wurde nicht eingeschaltet.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

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

 

