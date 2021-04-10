---
title: Ivmkeyboard tybäuerciitext-Methode (vpccominterfaces. h)
description: Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- Tybäuerciitext-Methode virtueller PC
- Tybäuerciitext-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, tybäuerciitext-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104271"
---
# <a name="ivmkeyboardtypeasciitext-method"></a>Ivmkeyboard:: tybäuerciitext-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Text* \[ in\]
</dt> <dd>

Die ASCII-Text Zeichenfolge, die in den virtuellen Computer eingegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>      | Die angegebene Zeichenfolge ist leer.<br/>    |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



 

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

 

