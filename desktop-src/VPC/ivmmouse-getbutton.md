---
title: Ivmmouse getbutton-Methode (vpccominterfaces. h)
description: Ruft den aktuellen Zustand der angegebenen Maustaste ab.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Getbutton-Methode virtueller PC
- Getbutton-Methode Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, getbutton-Methode
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
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743457"
---
# <a name="ivmmousegetbutton-method"></a>Ivmmouse:: getbutton-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*ButtonIndex* \[ in\]
</dt> <dd>

Der Index der Schaltfläche, deren Zustand angefordert wird. Eine Liste der Werte finden Sie unter [**vmmousetbutton**](vmmousebutton.md).

</dd> <dt>

*isdown* \[ Out, retval\]
</dt> <dd>

Der Zustand der aufgeführten Schaltfläche. **True** , wenn die Schaltfläche auf dem virtuellen Computer zurzeit nicht angezeigt wird, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                | Der *isdown* -Parameter ist **null**.<br/>                                                  |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>             | Der *Button Index* -Parameter ist ungültig.<br/>                                            |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>   | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.<br/> |
| <dl> <dt>**VM \_ E \_ Maus \_ nicht \_ aktiv**</dt> <dt>0xa0040800</dt> </dl> | Das Mausgerät wurde nicht eingeschaltet.<br/>                                            |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

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

 

