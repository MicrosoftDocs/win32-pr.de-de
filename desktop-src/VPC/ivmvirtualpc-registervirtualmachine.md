---
title: IVMVirtualPC RegisterVirtualMachine-Methode (VPCCOMInterfaces.h)
description: Registriert eine vorhandene VM-Konfiguration und ruft das Objekt des virtuellen Computers ab.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- RegisterVirtualMachine-Methode Virtueller PC
- RegisterVirtualMachine-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , RegisterVirtualMachine-Methode
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
ms.openlocfilehash: 3752b613bb3adc97d1e0968d989b5c97c616b76883ef89880be7c00d720c62a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998532"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a>IVMVirtualPC::RegisterVirtualMachine-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Registriert eine vorhandene VM-Konfiguration und ruft das Objekt des virtuellen Computers ab.

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

*configurationName* \[ In\]
</dt> <dd>

Der Name des zu registrierenden virtuellen Computers. Die Länge des Namens darf 80 Zeichen nicht überschreiten, und die kombinierte Länge von Name und Pfad darf **MAX \_ PATH** (260) Zeichen nicht überschreiten. Der angegebene Name kann die VMC-Erweiterung enthalten. Wenn dieser Parameter **NULL** oder eine leere Zeichenfolge ist, muss der *configurationPath-Parameter* den vollständigen Pfad zur Konfigurationsdatei angeben.

</dd> <dt>

*configurationPath* \[ In\]
</dt> <dd>

Der Pfad zum Ordner, der die vorhandene Konfigurationsdatei enthält. Wenn der *configurationName-Parameter* **NULL** oder eine leere Zeichenfolge ist, muss der vollständige Pfad zur vorhandenen Konfigurationsdatei angegeben werden.

</dd> <dt>

*virtualMachine* \[ out, retval\]
</dt> <dd>

Ein Zeiger auf ein neues [**IVMVirtualMachine-Objekt,**](ivmvirtualmachine.md) das diesen virtuellen Computer darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                          |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                    | Der *parameter configurationName* oder *configurationPath* ist ungültig, oder *virtualMachine* ist **NULL.**<br/>                                                                                                  |
| <dl> <dt>**HRESULT \_ VON \_ WIN32(FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN)**</dt> <dt>0X80070003</dt> </dl> | Das System kann den durch die Parameter *configurationName* und *configurationPath* angegebenen Pfad nicht finden.<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0x80070002</dt> </dl> | Das System kann die durch die Parameter *configurationName* und *configurationPath* angegebene Datei nicht finden.<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *configurationPath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?:<>/ \| "").<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Der *parameter configurationPath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der durch die Parameter *configurationName* und *configurationPath* angegebene Pfad führt zu einem Pfad, der zu lang ist. Die kombinierte Länge des Pfads muss kleiner als **MAX \_ PATH** (260) Zeichen sein.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>  | An diesem Speicherort ist bereits eine Konfigurationsdatei mit diesem Namen vorhanden.<br/>                                                                                                                                   |
| <dl> <dt>**VM \_ E \_ CONFIG \_ NAME TOO \_ \_ LONG**</dt> <dt>0xA0040401</dt> </dl>                | Der *parameter configurationName* überschreitet 80 Zeichen.<br/>                                                                                                                                     |
| <dl> <dt>**VM \_ E \_ CONFIG \_ NAME INVALID \_ \_ CHAR**</dt> <dt>0xA0040402</dt> </dl>            | Der *configurationName-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?:<>/ \| \\ "").<br/>                                                                                                         |
| <dl> <dt>**VM \_ E \_ CONFIG \_ DUPLICATE \_ NAME**</dt> <dt>0xA0040403</dt> </dl>                | Es gibt bereits einen virtuellen Computer mit diesem Namen.<br/>                                                                                                                                                     |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0xA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                                                                                                   |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Bei Namen virtueller Computer wird die Groß-/Kleinschreibung nicht beachtet, z. B. beziehen sich "MyVM" und "myvm" auf denselben virtuellen Computer.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

