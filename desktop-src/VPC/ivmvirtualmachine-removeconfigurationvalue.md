---
title: Ivmvirtualmachine removeconfigurationvalue-Methode (vpccominterfaces. h)
description: Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Removeconfigurationvalue-Methode Virtual PC
- Removeconfigurationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removeconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477985"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a>Ivmvirtualmachine:: removeconfigurationvalue-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigurationKey* \[ in\]
</dt> <dd>

Der Schlüssel, der zum Identifizieren des Konfigurations Werts verwendet wird, der in der \* VMC-Datei gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | BESCHREIBUNG                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>           | Der-Parameter ist **null** oder leer.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>       |
| <dl> <dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt> </dl> | Die Einstellung wurde nicht gefunden.<br/>       |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert. Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel zu entfernen. Gehen Sie vorsichtig vor, wenn Sie mit dieser Methode Systemkonfigurationswerte entfernen, da einige Werte nicht geändert werden können, während die virtuelle Maschine ausgeführt wird.

Konfigurationsschlüssel befinden sich in der VMC-Datei der virtuellen Maschine \* im XML-Format. Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.

Um beispielsweise den Wert des Schlüssels "RAM size" zu entfernen, der \_ sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:

``` syntax
"hardware/memory/ram_size"
```

Wenn einer der Schlüssel in der gewünschten Struktur über einen "ID"-Attribut Wert verfügt, werden das Attribut und sein Wert in der *ConfigurationKey* -Pfad Zeichenfolge unmittelbar nach dem zugehörigen Konfigurationsschlüssel in folgendem Format in Klammern eingebettet: " \[ @id ="*ID- \_ Wert*" \] ".

Um z. b. den Wert des "absoluten" Schlüssels zu entfernen, der sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
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

 

