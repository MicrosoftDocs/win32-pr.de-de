---
title: IVMVirtualPC SetConfigurationValue-Methode (VPCCOMInterfaces.h)
description: Legt den Wert der angegebenen Konfigurationseinstellung fest.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- SetConfigurationValue-Methode Virtueller PC
- SetConfigurationValue-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , SetConfigurationValue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d3ea585182794c1e96195fdbef842bc35c86342d390dd59e7077b31d4ef9a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591703"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>IVMVirtualPC::SetConfigurationValue-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Legt den Wert der angegebenen Konfigurationseinstellung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preferenceKey* \[ In\]
</dt> <dd>

Der Schlüssel, der zum Identifizieren der Einstellung verwendet wird, wie in der Konfigurationsdatei pro Benutzer gespeichert (Options.xml in "%LocalAppData% \\ Microsoft \\ Windows Virtual PC").

> [!IMPORTANT]
> Änderungen an Options.xml sollten nur mithilfe der **SetConfigurationValue-Methode** vorgenommen werden. Das Ändern Options.xml mit einer anderen Methode wird nicht unterstützt.

 

</dd> <dt>

*preferenceValue* \[ In\]
</dt> <dd>

Der Einstellungswert. Dieser Wert kann einer der folgenden **VARIANT-Typen** sein: **VT \_ ARRAY** \| **VT \_ UI1** (unformatierte Bytes), **VT \_ BSTR** (Zeichenfolge), **VT \_ UI4** (integer) oder **VT \_ BOOL** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                | Der *preferenceKey-* oder *preferenceValue-Parameter* ist **NULL.**<br/>                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Der *preferenceKey-Parameter* ist ungültig oder eine leere Zeichenfolge.<br/>                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                           | Der aktuelle Benutzer hat nicht genügend Zugriff auf die Konfigurationsdatei.<br/>                  |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0xA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Werte werden für den *preferenceKey-Parameter* unterstützt.



| *preferenceKey-Wert*      | BESCHREIBUNG                                                                                                                                                                           | Datentyp            | Standardwert   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| \_"Leerlauftimeout"<br/> | Anzahl von Sekunden, die vpc.exe warten sollten, bevor sie beendet werden, wenn keine aktiven VMs oder Anwendungen vorhanden sind, die die [Windows Virtual PC Interfaces](virtual-pc-interfaces.md)verwenden.<br/> | "integer"<br/> | „30“<br/> |



 

Diese Methode bietet Zugriff auf einen beliebigen Konfigurationswert auf niedriger Ebene. Sie kann verwendet werden, um Konfigurationswerte für kundendefinierte Schlüssel festzulegen. Seien Sie vorsichtig, wenn Sie diese Methode verwenden, um Systemkonfigurationswerte festzulegen, da keine Fehlerüberprüfung für den Konfigurationswert ausgeführt wird. Außerdem können einige Konfigurationswerte nicht geändert werden, während ein virtueller Computer ausgeführt wird.

Konfigurationsschlüssel befinden sich in der Datei "Options.xml" des virtuellen Computers im XML-Format. Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüsselpfad" erstellt, der die verschiedenen Schlüssel in einem durch Schrägstriche getrennten Format angibt.

So legen Sie beispielsweise den Wert des \_ Schlüssels "Leerlauftimeout" fest, der sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

Die *Pfadzeichenfolge preferenceKey* wird wie folgt angegeben:

``` syntax
"idle_timeout"
```

Wenn einer der Schlüssel in der gewünschten Struktur über einen ID-Attributwert  verfügt, werden das Attribut und sein Wert unmittelbar nach dem zugeordneten Konfigurationsschlüssel in die preferenceKey-Pfadzeichenfolge eingebettet, wobei das folgende formatierte Format in Klammern verwendet wird: " \[ @id ="*id \_ value*" \] ".

So legen Sie z. B. den Wert des Schlüssels "soll" in der folgenden Schlüsselstruktur fest:

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

Die *Pfadzeichenfolge preferenceKey* wird wie folgt angegeben:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

