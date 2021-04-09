---
title: Ivmkeyboard-presskey-Methode (vpccominterfaces. h)
description: Simuliert, dass eine Taste gedrückt wird.
ms.assetid: d945128a-ffde-465c-b615-83a1d5dc789f
keywords:
- Press Key-Methode Virtual PC
- Press Key-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, presskey-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.PressKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8175447a819afa7f761899a7e0dd3cbbcc780631
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040740"
---
# <a name="ivmkeyboardpresskey-method"></a>Ivmkeyboard::P resskey-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simuliert, dass eine Taste gedrückt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT PressKey(
  [in] BSTR key
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der Schlüsselcode für den zu drückenden Schlüssel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                   |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>                                      |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>      | Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmkeyboard**](ivmkeyboard.md)
</dt> </dl>

 

