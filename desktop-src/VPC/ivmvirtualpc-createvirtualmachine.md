---
title: Ivmvirtualpc-Methode "kreatevirtualmachine" (vpccominterfaces. h)
description: Erstellt eine neue Konfiguration für virtuelle Maschinen und ruft das Objekt der virtuellen Maschine ab.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Der Methode "Virtual PC" der Methode "die Methode"
- Die Methode "Virtual PC" der Methode "ivmvirtualmachine", ivmvirtualpc
- Ivmvirtualpc Interface Virtual PC, Methode "kreatevirtualmachine"
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478153"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a>Ivmvirtualpc:: kreatevirtualmachine-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Erstellt eine neue Konfiguration für virtuelle Maschinen und ruft das Objekt der virtuellen Maschine ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigurationName* \[ in\]
</dt> <dd>

Der Name des zu erstellenden virtuellen Computers. Die Länge des Namens darf nicht länger als 80 Zeichen sein, und die kombinierte Länge des Namens und des Pfads zu VMC-und vmcx-Dateien darf **maximal \_** zulässige (260) Zeichen nicht überschreiten. Die Dateinamen Erweiterungen. vmc und. vmcx werden an das Ende des Namens der virtuellen Maschine angehängt, wenn die Konfigurationsdateien erstellt werden. Wenn dieser Parameter **null** oder eine leere Zeichenfolge ist, muss der *ConfigurationPath* -Parameter den vollständigen Pfad zur VMC-Datei angeben.

</dd> <dt>

*ConfigurationPath* \[ in\]
</dt> <dd>

Der Pfad zu dem Ordner, der die VMC-Datei enthält. Dieser Ordner wird erstellt, wenn er nicht vorhanden ist. Wenn *ConfigurationName* **null** oder eine leere Zeichenfolge ist, muss der vollständige Pfad der neuen Konfigurationsdatei angegeben werden.

</dd> <dt>

*virtualmachine* \[ Out, retval\]
</dt> <dd>

Ein Zeiger auf ein neues [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das diesen virtuellen Computer darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                       |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Der *ConfigurationName* -Parameter oder der *ConfigurationPath* -Parameter ist ungültig, oder der *virtualmachine* -Parameter ist **null**.<br/>                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den vom *ConfigurationPath* -Parameter angegebenen Pfad nicht finden.<br/>                                                                                                                     |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>    | Der *ConfigurationPath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>    | Der *ConfigurationPath* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                                                                |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl> | Der von den Parametern *ConfigurationName* und *ConfigurationPath* angegebene Pfad führt zu einem Pfad, der zu lang ist. Die Gesamtlänge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>  | An diesem Speicherort ist bereits eine Konfigurationsdatei mit diesem Namen vorhanden.<br/>                                                                                                                                |
| <dl> <dt>**VM \_ E \_ config \_ No \_ Name**</dt> <dt>0xa0040400</dt> </dl>                       | Der *ConfigurationName* -Parameter ist leer.<br/>                                                                                                                                                         |
| <dl> <dt>**VM \_ E- \_ Konfigurations \_ Name \_ zu \_ lang**</dt> <dt>0xa0040401</dt> </dl>                | Der *ConfigurationName* -Parameter überschreitet 80 Zeichen lang.<br/>                                                                                                                                  |
| <dl> <dt>**VM \_ E- \_ Konfigurations \_ Name ist \_ ungültig \_ char**</dt> <dt>0xa0040402</dt> </dl>            | Der *ConfigurationName* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen \* : "?: <>/ \| \\ " ").<br/>                                                                                                      |
| <dl> <dt>**VM \_ E \_ config \_ Duplicate \_ Name**</dt> <dt>0xa0040403</dt> </dl>                | Es ist bereits ein virtueller Computer mit diesem Namen vorhanden.<br/>                                                                                                                                                  |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/>                                                                                                                |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Bei den Namen der virtuellen Computer wird die Groß-/Kleinschreibung nicht beachtet, z. b. "MyVM" und "MyVM" beziehen sich auf denselben virtuellen Computer.

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
</dt> </dl>

 

