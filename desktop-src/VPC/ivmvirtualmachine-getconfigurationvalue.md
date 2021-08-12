---
title: IVMVirtualMachine GetConfigurationValue-Methode (VPCCOMInterfaces.h)
description: Ruft den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer ab.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- GetConfigurationValue-Methode Virtueller PC
- GetConfigurationValue-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, GetConfigurationValue-Methode
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
ms.openlocfilehash: 3b58a048b2dd93f6aab7f071912519dac356896d6e32a13809f4560a3db9fb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592715"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a>IVMVirtualMachine::GetConfigurationValue-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*configurationKey* \[ In\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um den Konfigurationswert zu identifizieren, der in der \* VMC-Datei gespeichert ist.

</dd> <dt>

*configurationValue* \[ out, retval\]
</dt> <dd>

Der Konfigurationswert. Dieser Wert kann einer der folgenden **VARIANT-Typen** sein: **VT \_ ARRAY** \| **VT \_ UI1** (unformatierte Bytes), **VT \_ BSTR** (Zeichenfolge), **VT \_ I4** (integer) oder **VT \_ BOOL** (boolescher Wert).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | BESCHREIBUNG                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>           | Der *configurationKey-Parameter* ist **NULL** oder leer.<br/> |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>              | Der *configurationValue-Parameter* ist **NULL.**<br/>        |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                          |
| <dl> <dt>**VM \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | Die Einstellung wurde nicht gefunden.<br/>                          |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ermöglicht den Zugriff auf einen beliebigen Konfigurationswert auf niedriger Ebene. Sie kann verwendet werden, um Konfigurationswerte für kundendefinierte Schlüssel zu lesen.

Konfigurationsschlüssel befinden sich in der VMC-Datei des virtuellen \* Computers im XML-Format. Die Schlüssel werden in einer hierarchischen Weise gespeichert, die den Registrierungsschlüsseln in der Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüsselpfad" erstellt, der die verschiedenen Schlüssel in einem durch Schrägstrich getrennten Format angibt.

Um beispielsweise den Wert des Schlüssels \_ "RAM-Größe" in der folgenden Schlüsselstruktur zu lesen:

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

Die *Pfadzeichenfolge configurationKey* wird wie folgt angegeben:

``` syntax
"hardware/memory/ram_size"
```

Wenn einer der Schlüssel in der gewünschten Struktur einen "id"-Attributwert hat, werden das Attribut und sein Wert unmittelbar nach dem zugehörigen Konfigurationsschlüssel in die *Pfadzeichenfolge configurationKey* eingebettet. Verwenden Sie dabei das folgende Format in Klammern: " \[ @id ="*id \_ value*" \] ".

Um beispielsweise den Wert des "absoluten" Schlüssels zu lesen, der sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

Die *Pfadzeichenfolge configurationKey* wird wie folgt angegeben:

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

