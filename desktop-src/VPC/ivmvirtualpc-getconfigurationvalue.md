---
title: IVMVirtualPC GetConfigurationValue-Methode (VPCCOMInterfaces.h)
description: Ruft den Wert der angegebenen Konfigurationseinstellung ab
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- GetConfigurationValue-Methode Virtueller PC
- GetConfigurationValue-Methode Virtual PC , IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , GetConfigurationValue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a483211353474f3328fc4e5da3b80ecf3fbbece53bc306e546f85543ac9027e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591861"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>IVMVirtualPC::GetConfigurationValue-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Wert der angegebenen Konfigurationseinstellung ab

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preferenceKey* \[ In\]
</dt> <dd>

Der Schlüssel, der zum Identifizieren der Einstellung verwendet wird, wie in der Konfigurationsdatei gespeichert.

</dd> <dt>

*preferenceValue* \[ out, retval\]
</dt> <dd>

Der Einstellungswert. Dieser Parameter kann einer der folgenden **VARIANT-Typen** sein: **VT \_ ARRAY** \| **VT \_ UI1** (unformatierte Bytes), **VT \_ BSTR** (Zeichenfolge), **VT \_ I4** (integer) oder **VT \_ BOOL** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                | Der *preferenceKey-* oder *preferenceValue-Parameter* ist **NULL.**<br/>                      |
| <dl> <dt>**VM \_ \_E PREF \_ NOT \_ FOUND**</dt> <dt>0xa0040300</dt> </dl>                   | Die Einstellung wurde nicht gefunden.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0xA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode bietet Zugriff auf einen beliebigen Einstellungswert für den aktuellen Benutzer auf niedriger Ebene. Sie kann verwendet werden, um Einstellungswerte für kundendefinierte Schlüssel abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

