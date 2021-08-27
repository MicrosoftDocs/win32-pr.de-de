---
title: IVMVirtualMachine SetActivationValue-Methode (VPCCOMInterfaces.h)
description: Legt den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer fest.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- SetActivationValue-Methode Virtueller PC
- SetActivationValue-Methode Virtual PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, SetActivationValue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f7c669db848a668d294e509ad65a56ef19aebd53d0c718f12e524cfc16a940
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124720"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a>IVMVirtualMachine::SetActivationValue-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Legt den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*activationKey* \[ In\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um den Aktivierungswert zu identifizieren, der in der \* VMC-Datei gespeichert ist.

</dd> <dt>

*activationValue* \[ In\]
</dt> <dd>

Der Aktivierungswert. Dieser Wert kann einer der folgenden **VARIANT-Typen** sein: **VT \_ ARRAY** \| **VT \_ UI1** (unformatierte Bytes), **VT \_ BSTR** (Zeichenfolge), **VT \_ UI4** (integer) oder **VT \_ BOOL** (boolescher Wert).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | BESCHREIBUNG                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                                                                                       |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>           | Der *activationKey-Parameter* ist **NULL** oder leer, oder der *activationValue-Parameter* ist kein gültiger Variantentyp.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                                                                                       |
| <dl> <dt>**VM \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | Die Konfiguration verfügt über keine gültige Aktivierung.<br/>                                                                          |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                   |



 

## <a name="remarks"></a>Hinweise

Diese Methode ermöglicht den Zugriff auf einen beliebigen Aktivierungswert auf niedriger Ebene. Sie kann verwendet werden, um Aktivierungswerte für kundendefinierte Schlüssel festzulegen. Seien Sie vorsichtig, wenn Sie diese Methode zum Festlegen von Systemaktivierungswerten verwenden, da keine Fehlerüberprüfung für den Aktivierungswert ausgeführt wird. Außerdem können einige Aktivierungswerte nicht geändert werden, während der virtuelle Computer ausgeführt wird. Wenn ein virtueller Computer gestartet wird, wird eine Kopie seiner Konfigurationswerte vorgenommen, die zu einem Satz von Aktivierungswerten wird. Aktivierungswerte werden beibehalten, bis der virtuelle Computer heruntergefahren oder neu gestartet wird. Beachten Sie, Windows virtueller PC die Konfiguration nur zum Speichern von Werten für bestimmte Schlüssel verwenden darf, d.&Windows der Aktivierungswert möglicherweise nie verwendet wird.

> [!Note]  
> Die Sitzung des virtuellen Computers muss ausgeführt werden, bevor Aktivierungswerte geändert werden können.

 

Aktivierungsschlüssel werden intern in einer hierarchischen Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüsselpfad" erstellt, der die verschiedenen Schlüssel in einem durch Schrägstrich getrennten Format angibt.

So legen Sie beispielsweise den Wert des Schlüssels "Default \_ Action" fest, der sich in der folgenden Schlüsselstruktur befindet:

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
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

