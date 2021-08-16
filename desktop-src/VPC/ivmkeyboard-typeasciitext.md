---
title: IVMKeyboard TypeAsciiText-Methode (VPCCOMInterfaces.h)
description: Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- TypeAsciiText-Methode Virtueller PC
- TypeAsciiText-Methode Virtueller PC, IVMKeyboard-Schnittstelle
- IVMKeyboard-Schnittstelle Virtueller PC, TypeAsciiText-Methode
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
ms.openlocfilehash: c05e1c2afce1fa21aa1017a2ac7975ddcf49d850e2dbbc3cfb12e69798600554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345264"
---
# <a name="ivmkeyboardtypeasciitext-method"></a>IVMKeyboard::TypeAsciiText-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Text* \[ In\]
</dt> <dd>

Die ASCII-Textzeichenfolge, die innerhalb des virtuellen Computers eingegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>      | Die angegebene Zeichenfolge ist leer.<br/>    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard ist als 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4 definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

