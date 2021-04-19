---
title: Ivmvirtualpc registervirtualmachine-Methode (vpccominterfaces. h)
description: Registriert eine vorhandene VM-Konfiguration und ruft das Objekt der virtuellen Maschine ab.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Registervirtualmachine-Methode Virtual PC
- Registervirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, registervirtualmachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342471"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a>Ivmvirtualpc:: registervirtualmachine-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Registriert eine vorhandene VM-Konfiguration und ruft das Objekt der virtuellen Maschine ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigurationName* \[ in\]
</dt> <dd>

Der Name des zu registrierenden virtuellen Computers. Der Name darf nicht länger als 80 Zeichen sein, und die kombinierte Länge des Namens und des Pfads darf **maximal \_ zulässige (** 260) Zeichen lang sein. Der angegebene Name kann die VMC-Erweiterung enthalten. Wenn dieser Parameter **null** oder eine leere Zeichenfolge ist, muss der *ConfigurationPath* -Parameter den vollständigen Pfad zur Konfigurationsdatei angeben.

</dd> <dt>

*ConfigurationPath* \[ in\]
</dt> <dd>

Der Pfad zu dem Ordner, der die vorhandene Konfigurationsdatei enthält. Wenn der *ConfigurationName* -Parameter **null** oder eine leere Zeichenfolge ist, muss der vollständige Pfad zur vorhandenen Konfigurationsdatei angegeben werden.

</dd> <dt>

*virtualmachine* \[ Out, retval\]
</dt> <dd>

Ein Zeiger auf ein neues [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das diesen virtuellen Computer darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                          |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Der *ConfigurationName* -Parameter oder der *ConfigurationPath* -Parameter ist ungültig, oder *virtualmachine* ist **null**.<br/>                                                                                                  |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den in den Parametern *ConfigurationName* und *ConfigurationPath* angegebenen Pfad nicht finden.<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt> </dl> | Das System kann die durch den *ConfigurationName* -Parameter und den *ConfigurationPath* -Parameter angegebene Datei nicht finden.<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>    | Der *ConfigurationPath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>    | Der *ConfigurationPath* -Parameter des Parameters gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                                                         |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl> | Der von den Parametern *ConfigurationName* und *ConfigurationPath* angegebene Pfad führt zu einem Pfad, der zu lang ist. Die kombinierte Länge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>  | An diesem Speicherort ist bereits eine Konfigurationsdatei mit diesem Namen vorhanden.<br/>                                                                                                                                   |
| <dl> <dt>**VM \_ E- \_ Konfigurations \_ Name \_ zu \_ lang**</dt> <dt>0xa0040401</dt> </dl>                | Der *ConfigurationName* -Parameter überschreitet 80 Zeichen lang.<br/>                                                                                                                                     |
| <dl> <dt>**VM \_ E- \_ Konfigurations \_ Name ist \_ ungültig \_ char**</dt> <dt>0xa0040402</dt> </dl>            | Der *ConfigurationName* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen \* : "?: <>/ \| \\ " ").<br/>                                                                                                         |
| <dl> <dt>**VM \_ E \_ config \_ Duplicate \_ Name**</dt> <dt>0xa0040403</dt> </dl>                | Es ist bereits ein virtueller Computer mit diesem Namen vorhanden.<br/>                                                                                                                                                     |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/>                                                                                                                   |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                      |



 

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

 

