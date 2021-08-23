---
title: IVMKeyboard ReleaseKey-Methode (VPCCOMInterfaces.h)
description: Simuliert einen Schlüssel, der freigegeben wird.
ms.assetid: 112bf11d-d768-4487-ab41-e915aa4e6a24
keywords:
- ReleaseKey-Methode Virtueller PC
- ReleaseKey-Methode Virtual PC , IVMKeyboard-Schnittstelle
- IVMKeyboard-Schnittstelle Virtueller PC, ReleaseKey-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.ReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6610cf6aad2a6838a1437f9be33cbf93847a64a9266e07c424b4209bccd5a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136673"
---
# <a name="ivmkeyboardreleasekey-method"></a>IVMKeyboard::ReleaseKey-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simuliert einen Schlüssel, der freigegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* \[ In\]
</dt> <dd>

Der Schlüsselcode für den Schlüssel, der freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | Beschreibung                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                   |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>      | Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                               |



 

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

 

