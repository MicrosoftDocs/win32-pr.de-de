---
title: IVMVirtualPC RemoveConfigurationValue-Methode (VPCCOMInterfaces.h)
description: Entfernt den Wert der angegebenen Konfigurationseinstellung.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- RemoveConfigurationValue-Methode Virtueller PC
- RemoveConfigurationValue-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, RemoveConfigurationValue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281837394967a15bce40173ead0ca02be66eb046bf7c15b63fdded57c2ecef84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998536"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a>IVMVirtualPC::RemoveConfigurationValue-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Entfernt den Wert der angegebenen Konfigurationseinstellung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preferenceKey* \[ In\]
</dt> <dd>

Der Schlüssel, der zum Identifizieren der Einstellung verwendet wird, wie in der Konfigurationsdatei gespeichert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                | Der *preferenceKey-Parameter* ist **NULL.**<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                             | Der *preferenceKey-Parameter* ist ungültig oder eine leere Zeichenfolge.<br/>                    |
| <dl> <dt>**VM \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl>                   | Die Einstellung wurde nicht gefunden.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0XA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

## <a name="remarks"></a>Hinweise

Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Einstellungswert für den aktuellen Benutzer. Sie kann verwendet werden, um Einstellungswerte für kundendefinierte Schlüssel zu entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

