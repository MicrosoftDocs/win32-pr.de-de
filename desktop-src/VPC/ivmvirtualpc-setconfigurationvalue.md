---
title: Ivmvirtualpc setconfigurationvalue-Methode (vpccominterfaces. h)
description: Legt den Wert der angegebenen Konfigurationseinstellung fest.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Setconfigurationvalue-Methode Virtual PC
- Setconfigurationvalue-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, setconfigurationvalue-Methode
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
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518467"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>Ivmvirtualpc:: setconfigurationvalue-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*preferecekey* \[ in\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um die Einstellung zu identifizieren, wie Sie in der Konfigurationsdatei pro Benutzer (Options.xml in "% LocalAppData% \\ Microsoft \\ Windows Virtual PC") gespeichert ist.

> [!IMPORTANT]
> Es sollten Änderungen vorgenommen werden, die nur mit der **setconfigurationvalue** -Methode Options.xml werden. Das Ändern von Options.xml mit einer anderen Methode wird nicht unterstützt.

 

</dd> <dt>

*preferumcevalue* \[ in\]
</dt> <dd>

Der bevorzugte Wert. Dieser Wert kann einer der folgenden **Variant** -Typen sein: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) oder **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                | Der *preferecekey* -Parameter oder der *preferendcevalue* -Parameter ist **null**.<br/>                      |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                             | Der *preferencekey* -Parameter ist ungültig oder eine leere Zeichenfolge.<br/>                    |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**E \_ AccessDenied**</dt> <dt>0x80070005</dt> </dl>                           | Der aktuelle Benutzer verfügt nicht über ausreichenden Zugriff auf die Konfigurationsdatei.<br/>                  |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Werte werden für den *preferecekey* -Parameter unterstützt.



| *preferecekey* -Wert      | BESCHREIBUNG                                                                                                                                                                           | Datentyp            | Standardwert   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| "Leerlauf \_ Timeout"<br/> | Anzahl der Sekunden, die vpc.exe warten soll, bis der Vorgang beendet ist, wenn die [Windows Virtual PC-Schnittstellen](virtual-pc-interfaces.md)keine aktiven VMS oder Anwendungen verwenden.<br/> | Zah<br/> | „30“<br/> |



 

Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert. Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel festzulegen. Gehen Sie vorsichtig vor, wenn Sie diese Methode verwenden, um Systemkonfigurations Werte festzulegen, da für den Konfigurations Wert keine Fehlerüberprüfung durchgeführt wird. Außerdem können einige Konfigurationswerte nicht geändert werden, während ein virtueller Computer ausgeführt wird.

Konfigurationsschlüssel befinden sich im XML-Format in der Datei "Options.xml" der virtuellen Maschine. Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows. Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.

So legen Sie beispielsweise den Wert für den Schlüssel "Leerlauf Timeout" fest, der \_ sich in der folgenden Schlüsselstruktur befindet:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

Die Pfad *Zeichenfolge für den preferencekey* wird wie folgt angegeben:

``` syntax
"idle_timeout"
```

Wenn einer der Schlüssel in der gewünschten Struktur über einen "ID"-Attribut Wert verfügt, werden das Attribut und sein Wert in der Pfad *Zeichenfolge "preferencekey* " direkt nach dem zugehörigen Konfigurationsschlüssel in folgendem Format in Klammern eingebettet: " \[ @id ="*ID- \_ Wert*" \] ".

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

Die Pfad *Zeichenfolge für den preferencekey* wird wie folgt angegeben:

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
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc**](ivmvirtualpc.md)
</dt> <dt>

[**Ivmvirtualmachine:: setconfigurationvalue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

