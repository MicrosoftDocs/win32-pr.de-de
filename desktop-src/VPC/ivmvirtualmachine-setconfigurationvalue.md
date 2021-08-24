---
title: IVMVirtualMachine SetConfigurationValue-Methode (VPCCOMInterfaces.h)
description: Legt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer (VM) fest.
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- SetConfigurationValue-Methode Virtueller PC
- SetConfigurationValue-Methode Virtual PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, SetConfigurationValue-Methode
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
ms.openlocfilehash: 7edef64484161f6151b1d2ac14fd6916a7d2a082c0c787b983019305027f4949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652970"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>IVMVirtualMachine::SetConfigurationValue-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*configurationKey* \[ In\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um den Konfigurationswert zu identifizieren, der in der \* VMC-Datei gespeichert ist.

> [!IMPORTANT]
> Änderungen an ".vmc" sollten nur mithilfe \* der **SetConfigurationValue-Methode vorgenommen** werden. Das Ändern von \* ".vmc" mit einer anderen Methode wird nicht unterstützt.

 

</dd> <dt>

*configurationValue* \[ In\]
</dt> <dd>

Der Konfigurationswert. Dieser Wert cay ist  einer der folgenden VARIANT-Typen: **VT \_ ARRAY** \| **VT \_ UI1** (unformatierte Bytes), **VT \_ BSTR** (Zeichenfolge), **VT \_ UI4** (integer) oder **VT \_ BOOL (boolescher** Wert).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | Beschreibung                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>      | Der *configurationKey-Parameter* ist **NULL** oder leer, oder der *parameter configurationValue* ist kein gültiger Variantentyp.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                                                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                        |



 

## <a name="remarks"></a>Hinweise

Die folgenden Werte werden für den *configurationKey-Parameter* unterstützt.



| *configurationKey-Wert*                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Datentyp            | Standardwert     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| "Hardware-/Bios/Zeitsynchronisierung \_ \_ beim \_ Start"<br/>              | "true", wenn die CMOS-Uhr des virtuellen Computers beim Start mit der Hostuhr synchronisiert werden soll; Andernfalls "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | "boolean"<br/> | "true"<br/> |
| "integration/microsoft/host \_ time \_ sync/enabled"<br/> | "true", wenn die Hostzeitsynchronisierung in den Integrationskomponenten aktiviert ist; Andernfalls "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | "boolean"<br/> | "true"<br/> |
| "ui \_ options/auto \_ app \_ publish"<br/>                  | "true", wenn die automatische Veröffentlichung von Anwendungen in den Integrationskomponenten aktiviert ist; Andernfalls "false". Dies wird auch als virtuelle Anwendungen bezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | "boolean"<br/> | "true"<br/> |
| "ui \_ options/seconds \_ to save" (Ui-Optionen/Sekunden zum \_ Speichern)<br/>                   | Die Anzahl der Sekunden, die gewartet werden soll, bevor der virtuelle Computer nach dem Schließen aller Anwendungen speichern wird. Werte unter 20 und mehr als 4.294.968 haben jedoch eine besondere Bedeutung. Weitere Informationen finden Sie in der folgenden Liste.<br/> <dl> <dt><span id="0"></span>0</dt> <dd> Speichern Sie den virtuellen Computer nie.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Warten Sie 20 Sekunden, bevor Sie den virtuellen Computer speichern.<br/> </dd> <dt><span id="214_294_967"></span>21 4,294,967</dt> <dd> Warten Sie die angegebene Anzahl von Sekunden, bevor Sie den virtuellen Computer speichern.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt> <dd> Warten Sie 4.294.968 Sekunden, bevor Sie den virtuellen Computer speichern.<br/> </dd> </dl> | "integer"<br/> | 300<br/>    |



 

Diese Methode ermöglicht den Zugriff auf einen beliebigen Konfigurationswert auf niedriger Ebene. Sie kann verwendet werden, um Konfigurationswerte für kundendefinierte Schlüssel festzulegen. Seien Sie vorsichtig, wenn Sie diese Methode zum Festlegen von Systemkonfigurationswerten verwenden, da keine Fehlerüberprüfung für den Konfigurationswert ausgeführt wird. Darüber hinaus können einige Konfigurationswerte nicht geändert werden, während der virtuelle Computer ausgeführt wird.

Konfigurationsschlüssel befinden sich in der VMC-Datei des virtuellen \* Computers im XML-Format. Die Schlüssel werden in einer hierarchischen Weise gespeichert, die den Registrierungsschlüsseln in der Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüsselpfad" erstellt, der die verschiedenen Schlüssel in einem durch Schrägstrich getrennten Format angibt.

So legen Sie beispielsweise den Wert des Schlüssels \_ "RAM-Größe" fest, der sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

Die *Pfadzeichenfolge configurationKey* wird wie folgt angegeben:

``` syntax
"hardware/memory/ram_size"
```

Wenn einer der Schlüssel in der gewünschten Struktur einen "id"-Attributwert hat, werden das Attribut und sein Wert unmittelbar nach dem zugehörigen Konfigurationsschlüssel in die *Pfadzeichenfolge configurationKey* eingebettet. Verwenden Sie dabei das folgende Format in Klammern: " \[ @id ="*id \_ value*" \] ".

So legen Sie z. B. den Wert des Schlüssels "beschriftung" fest, der sich in der folgenden Schlüsselstruktur befindet:

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

Die *Pfadzeichenfolge configurationKey* wird wie folgt angegeben:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
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
</dt> <dt>

[**IVMVirtualPC::SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

