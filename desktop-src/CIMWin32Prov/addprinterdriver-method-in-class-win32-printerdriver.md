---
description: Erstellt einen neuen Druckertreiber.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Addprinterdriver-Methode der Win32_PrinterDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392966"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Addprinterdriver-Methode der Win32 \_ PrinterDriver-Klasse

Die **addprinterdriver** -Klassenmethode erstellt einen neuen Druckertreiber.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DriverInfo* \[ in\]
</dt> <dd>

Eine Instanz der Win32-Klasse " [**\_ PrinterDriver**](win32-printerdriver.md) ", die den Druckertreiber darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Werte, die sich von den in der folgenden Liste aufgeführten Werten unterscheiden, finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Erfolg.

</dd> <dt>

**5**
</dt> <dd>

Zugriff verweigert.

</dd> <dt>

**87**
</dt> <dd>

„Der Parameter ist falsch.“ Kann auftreten, wenn das Objekt nicht ordnungsgemäß ausgefüllt ist oder wenn der Treiber im System nicht gefunden werden kann. Alternativ kann sich das Name-Attribut von dem in der INF-Datei angegebenen Modell unterscheiden. Möglicherweise ist auch ein umgekehrter umgekehrter Schrägstrich (" \\ ") für ein pathfile-Attribut vorhanden.

</dd> <dt>

**1797**
</dt> <dd>

Der Druckertreiber ist unbekannt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Bei Verwendung der **addprinterdriver** -Methode müssen Sie " **SeLoadDriverPrivilege** " verwenden, um einen Gerätetreiber zu laden oder zu entladen.

 

## <a name="examples"></a>Beispiele

Mit dem Codebeispiel "[install a Printer Driver that CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript" wird ein hypothetischer Drucker mithilfe eines Druck Treibers installiert, der in Drivers.cab nicht gefunden wurde.

Im folgenden VBScript-Beispiel wird der Druckertreiber für einen Apple LaserWriter 8500-Drucker installiert.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32- \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

