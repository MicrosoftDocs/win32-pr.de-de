---
title: IVMVirtualMachine GetActivationValue-Methode (VPCCOMInterfaces.h)
description: Ruft den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer ab.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- GetActivationValue-Methode Virtueller PC
- GetActivationValue-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, GetActivationValue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e03d1178df5961ba76a0ab61e74c781315cce07f32657903e5fa3e4e0a7623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123196"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a>IVMVirtualMachine::GetActivationValue-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*activationKey* \[ In\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um den Aktivierungswert zu identifizieren, der in der \* VMC-Datei gespeichert ist.

</dd> <dt>

*activationValue* \[ out, retval\]
</dt> <dd>

Der Aktivierungswert. Dieser Wert kann einer der folgenden **VARIANT-Typen** sein: **VT \_ ARRAY** \| **VT \_ UI1** (unformatierte Bytes), **VT \_ BSTR** (Zeichenfolge), **VT \_ I4** (integer) oder **VT \_ BOOL** (boolescher Wert).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | Beschreibung                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                                                |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>           | Der *activationKey-Parameter* ist **NULL** oder leer.<br/>                          |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>              | Der *activationValue-Parameter* ist **NULL.**<br/>                                 |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                                                |
| <dl> <dt>**VM \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | Die Einstellung wurde nicht gefunden, oder diese Konfiguration verfügt über keine gültige Aktivierung.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Diese Methode ermöglicht den Zugriff auf einen beliebigen Aktivierungswert auf niedriger Ebene. Sie kann verwendet werden, um Aktivierungswerte für kundendefinierte Schlüssel festzulegen. Wenn ein virtueller Computer gestartet wird, wird eine Kopie seiner Konfigurationswerte vorgenommen, die zu einem Satz von Aktivierungswerten wird. Aktivierungswerte werden beibehalten, bis der virtuelle Computer heruntergefahren oder neu gestartet wird. Beachten Sie, Windows virtueller PC die Konfiguration nur zum Speichern von Werten für bestimmte Schlüssel verwenden darf, d.&Windows der Aktivierungswert möglicherweise nie verwendet wird.

Aktivierungsschlüssel werden intern in einer hierarchischen Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüsselpfad" erstellt, der die verschiedenen Schlüssel in einem durch Schrägstrich getrennten Format angibt.

Um beispielsweise den Wert des Schlüssels "Default Action" in \_ der folgenden Schlüsselstruktur zu lesen:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

Die *ActivationKey-Pfadzeichenfolge* wird wie folgt angegeben:

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

