---
title: IVMVirtualMachine RemoveActivationValue-Methode (VPCCOMInterfaces.h)
description: Entfernt den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- RemoveActivationValue-Methode Virtueller PC
- RemoveActivationValue-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC , RemoveActivationValue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fcb531a405f66e39f9821e36f10d3e65e1e8b771472d87d0bce9e415dd672a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653030"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a>IVMVirtualMachine::RemoveActivationValue-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Entfernt den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*activationKey* \[ In\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um den Aktivierungswert zu identifizieren, der in der \* DATEI ".vmc" gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | Beschreibung                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                                                |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>           | Der Parameter ist **NULL** oder leer.<br/>                                          |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                                                |
| <dl> <dt>**VM \_ \_E PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | Die Einstellung wurde nicht gefunden, oder diese Konfiguration verfügt über keine gültige Aktivierung.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Diese Methode bietet Zugriff auf einen beliebigen Aktivierungswert auf niedriger Ebene. Sie kann verwendet werden, um Aktivierungswerte für kundendefinierte Schlüssel zu entfernen. Gehen Sie vorsichtig vor, wenn Sie diese Methode verwenden, um Systemaktivierungswerte zu entfernen, da einige Werte nicht geändert werden können, während der virtuelle Computer ausgeführt wird. Wenn ein virtueller Computer gestartet wird, wird eine Kopie seiner Konfigurationswerte erstellt, die zu einem Satz von Aktivierungswerten wird. Aktivierungswerte werden beibehalten, bis der virtuelle Computer heruntergefahren oder neu gestartet wird. Beachten Sie, dass Windows Virtueller PC nur die Konfiguration zum Speichern von Werten für bestimmte Schlüssel verwenden darf, d. h., der Aktivierungswert darf nie verwendet werden.

> [!Note]  
> Die Sitzung des virtuellen Computers muss ausgeführt werden, bevor Aktivierungswerte geändert werden können.

 

Aktivierungsschlüssel werden intern auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüsselpfad" erstellt, der die verschiedenen Schlüssel in einem durch Schrägstriche getrennten Format angibt.

So entfernen Sie beispielsweise den Wert des \_ Schlüssels "Standardaktion", der sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

Die *Pfadzeichenfolge activationKey* wird wie folgt angegeben:

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

