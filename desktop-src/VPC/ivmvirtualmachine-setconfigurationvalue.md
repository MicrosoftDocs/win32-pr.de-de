---
title: Ivmvirtualmachine setconfigurationvalue-Methode (vpccominterfaces. h)
description: Legt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer (VM) fest.
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Setconfigurationvalue-Methode Virtual PC
- Setconfigurationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, setconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344489"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>Ivmvirtualmachine:: setconfigurationvalue-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Legt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer (VM) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigurationKey* \[ in\]
</dt> <dd>

Der Schlüssel, der zum Identifizieren des Konfigurations Werts verwendet wird, der in der \* VMC-Datei gespeichert ist.

> [!IMPORTANT]
> Änderungen sollten \* nur mit der **setconfigurationvalue** -Methode an ". vmc" vorgenommen werden. Das ändern \* von ". vmc" mit einer anderen Methode wird nicht unterstützt.

 

</dd> <dt>

*configurationvalue* \[ in\]
</dt> <dd>

Der Konfigurationswert. Dieser Wert ist einer der folgenden **Variant** -Typen: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) oder **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                                                                            |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>      | Der *ConfigurationKey* -Parameter ist **null** oder leer, oder der *configurationvalue* -Parameter ist kein gültiger VARIANT-Typ.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                                                                            |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Werte werden für den *ConfigurationKey* -Parameter unterstützt.



| *ConfigurationKey* -Wert                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Datentyp            | Standardwert     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| "Hardware/BIOS/Zeit \_ Synchronisierung \_ beim \_ Start"<br/>              | "true", wenn die VM-CMOS-Uhr beim Start mit der hostuhr synchronisiert werden soll. andernfalls "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | booleschen<br/> | "true"<br/> |
| "Integration/Microsoft/ \_ hostzeit \_ Synchronisierung/aktiviert" "<br/> | "true", wenn die Host Zeitsynchronisierung in den Integrations Komponenten aktiviert ist. andernfalls "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | booleschen<br/> | "true"<br/> |
| "UI \_ -Optionen/Automatische \_ App- \_ Veröffentlichung"<br/>                  | "true", wenn die automatische Veröffentlichung von Anwendungen in den Integrations Komponenten aktiviert ist. andernfalls "false". Dies wird auch als virtuelle Anwendungen bezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | booleschen<br/> | "true"<br/> |
| "Benutzeroberflächen \_ Optionen/-Sekunden \_ zum \_ Speichern"<br/>                   | Anzahl von Sekunden, die gewartet werden soll, bevor die VM gespeichert wird, nachdem alle Anwendungen geschlossen wurden. Werte unter 20 und mehr als 4.294.968 haben jedoch eine besondere Bedeutung. Weitere Informationen finden Sie in der folgenden Liste:<br/> <dl> <dt><span id="0"></span>0</dt> <dd> Speichern Sie die VM nie.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Warten Sie 20 Sekunden, bevor Sie den virtuellen Computer speichern.<br/> </dd> <dt><span id="214_294_967"></span>21 4.294.967</dt> <dd> Warten Sie die angegebene Anzahl von Sekunden, bevor Sie den virtuellen Computer speichern.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt> <dd> Warten Sie 4.294.968 Sekunden, bevor Sie den virtuellen Computer speichern.<br/> </dd> </dl> | Zah<br/> | 300<br/>    |



 

Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert. Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel festzulegen. Gehen Sie vorsichtig vor, wenn Sie diese Methode verwenden, um Systemkonfigurations Werte festzulegen, da für den Konfigurations Wert keine Fehlerüberprüfung durchgeführt wird. Außerdem können einige Konfigurationswerte nicht geändert werden, während der virtuelle Computer ausgeführt wird.

Konfigurationsschlüssel befinden sich in der VMC-Datei der virtuellen Maschine \* im XML-Format. Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.

So legen Sie beispielsweise den Wert für den Schlüssel "RAM size" fest, der \_ sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:

``` syntax
"hardware/memory/ram_size"
```

Wenn einer der Schlüssel in der gewünschten Struktur über einen "ID"-Attribut Wert verfügt, werden das Attribut und sein Wert in der *ConfigurationKey* -Pfad Zeichenfolge unmittelbar nach dem zugehörigen Konfigurationsschlüssel in folgendem Format in Klammern eingebettet: " \[ @id ="*ID- \_ Wert*" \] ".

So legen Sie beispielsweise den Wert des "Golf"-Schlüssels fest, der sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
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
</dt> <dt>

[**Ivmvirtualpc:: setconfigurationvalue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

