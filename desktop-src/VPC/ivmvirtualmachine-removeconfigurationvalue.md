---
title: IVMVirtualMachine RemoveConfigurationValue-Methode (VPCCOMInterfaces.h)
description: Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- RemoveConfigurationValue-Methode Virtueller PC
- RemoveConfigurationValue-Methode Virtual PC , IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC , RemoveConfigurationValue-Methode
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
ms.openlocfilehash: 130feab953b5116ae8d6194f23cefc88c6792cf584ec884edd359ce6fc44a906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752289"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a>IVMVirtualMachine::RemoveConfigurationValue-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*configurationKey* \[ In\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um den Konfigurationswert zu identifizieren, der in der \* VMC-Datei gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                      | Beschreibung                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>           | Der Parameter ist **NULL** oder leer.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>       |
| <dl> <dt>**VM \_ \_E PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | Die Einstellung wurde nicht gefunden.<br/>       |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



 

## <a name="remarks"></a>Hinweise

Diese Methode bietet Zugriff auf einen beliebigen Konfigurationswert auf niedriger Ebene. Sie kann verwendet werden, um Konfigurationswerte für kundendefinierte Schlüssel zu entfernen. Gehen Sie vorsichtig vor, wenn Sie diese Methode verwenden, um Systemkonfigurationswerte zu entfernen, da einige Werte nicht geändert werden können, während der virtuelle Computer ausgeführt wird.

Konfigurationsschlüssel befinden sich in der VMC-Datei des virtuellen Computers \* im XML-Format. Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüsselpfad" erstellt, der die verschiedenen Schlüssel in einem durch Schrägstriche getrennten Format angibt.

Um z. B. den Wert des \_ Schlüssels "RAM-Größe" in der folgenden Schlüsselstruktur zu entfernen:

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

Die *Pfadzeichenfolge configurationKey* wird wie folgt angegeben:

``` syntax
"hardware/memory/ram_size"
```

Wenn einer der Schlüssel in der gewünschten Struktur über einen "id"-Attributwert verfügt, werden das Attribut und sein Wert unmittelbar nach dem zugeordneten Konfigurationsschlüssel in die *configurationKey-Pfadzeichenfolge* eingebettet, wobei das folgende format in Klammern verwendet wird: " \[ @id =" id *\_ value*" \] ".

Um z. B. den Wert des "absoluten" Schlüssels in der folgenden Schlüsselstruktur zu entfernen:

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
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

