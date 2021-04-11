---
title: Ivmvirtualmachine removeactivationvalue-Methode (vpccominterfaces. h)
description: Entfernt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Removeactivationvalue-Methode Virtual PC
- Removeactivationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removeactivationvalue-Methode
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
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040701"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a>Ivmvirtualmachine:: removeactivationvalue-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Entfernt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*activationkey* \[ in\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um den Aktivierungs Wert zu identifizieren, wie er in der \* VMC-Datei gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | BESCHREIBUNG                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                                                |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>           | Der-Parameter ist **null** oder leer.<br/>                                          |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                                                |
| <dl> <dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt> </dl> | Die Einstellung wurde nicht gefunden, oder für diese Konfiguration ist keine gültige Aktivierung vorhanden.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode bietet Zugriff auf niedriger Ebene auf jeden Aktivierungs Wert. Sie kann verwendet werden, um Aktivierungs Werte für Kunden definierte Schlüssel zu entfernen. Gehen Sie vorsichtig vor, wenn Sie diese Methode zum Entfernen von System Aktivierungs Werten verwenden, da einige Werte nicht geändert werden können, während die virtuelle Maschine ausgeführt wird. Wenn ein virtueller Computer gestartet wird, wird eine Kopie seiner Konfigurationswerte erstellt, die zu dem Satz von Aktivierungs Werten wird. Aktivierungs Werte werden so lange beibehalten, bis der virtuelle Computer heruntergefahren oder neu gestartet wird. Beachten Sie, dass Windows Virtual PC die Konfiguration möglicherweise nur zum Speichern von Werten für bestimmte Schlüssel verwendet, d. h., der Aktivierungs Wert darf nie verwendet werden.

> [!Note]  
> Die Sitzung für virtuelle Computer muss ausgeführt werden, bevor Aktivierungs Werte geändert werden können.

 

Aktivierungsschlüssel werden auf hierarchische Weise wie die Registrierungsschlüssel in Windows gespeichert. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.

Um z. b. den Wert des Schlüssels "Default Action" zu entfernen, der \_ sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

Die Pfad Zeichenfolge von *activationkey* wird wie folgt angegeben:

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

