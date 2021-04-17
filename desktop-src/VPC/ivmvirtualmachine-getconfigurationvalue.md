---
title: Ivmvirtualmachine getconfigurationvalue-Methode (vpccominterfaces. h)
description: Ruft den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer ab.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Getconfigurationvalue-Methode Virtual PC
- Getconfigurationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, getconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391982"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a>Ivmvirtualmachine:: getconfigurationvalue-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigurationKey* \[ in\]
</dt> <dd>

Der Schlüssel, der zum Identifizieren des Konfigurations Werts verwendet wird, der in der \* VMC-Datei gespeichert ist.

</dd> <dt>

*configurationvalue* \[ Out, retval\]
</dt> <dd>

Der Konfigurationswert. Bei diesem Wert kann es sich um einen der folgenden **Variant** -Typen handeln: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ I4** (Integer) oder **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | BESCHREIBUNG                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                          |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>           | Der *ConfigurationKey* -Parameter ist **null** oder leer.<br/> |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>              | Der *configurationvalue* -Parameter ist **null**.<br/>        |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                          |
| <dl> <dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt> </dl> | Die Einstellung wurde nicht gefunden.<br/>                          |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert. Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel zu lesen.

Konfigurationsschlüssel befinden sich in der VMC-Datei der virtuellen Maschine \* im XML-Format. Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.

Um z. b. den Wert des Schlüssels "RAM \_ size" in der folgenden Schlüsselstruktur zu lesen:

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

Um z. b. den Wert des "absoluten" Schlüssels in der folgenden Schlüsselstruktur zu lesen:

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

 

