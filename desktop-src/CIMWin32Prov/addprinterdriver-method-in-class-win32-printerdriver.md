---
description: Erstellt einen neuen Druckertreiber.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: AddPrinterDriver-Methode der Win32_PrinterDriver-Klasse
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
ms.openlocfilehash: 14681c381f8c8b9abbc5b28ec763b959854e2303b9a0b87af762238f4e5a8d27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752800"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>AddPrinterDriver-Methode der Win32 \_ PrinterDriver-Klasse

Die **AddPrinterDriver-Klassenmethode** erstellt einen neuen Druckertreiber.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DriverInfo* \[ In\]
</dt> <dd>

Eine Instanz der [**Win32 \_ PrinterDriver-Klasse,**](win32-printerdriver.md) die den Druckertreiber darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Werte, die sich von denen in der folgenden Liste unterscheiden, finden Sie unter [**WMI-Fehlerkonstanten.**](/windows/desktop/WmiSdk/wmi-error-constants)

<dl> <dt>

**0**
</dt> <dd>

Erfolg.

</dd> <dt>

**5**
</dt> <dd>

Zugriff verweigert:

</dd> <dt>

**87**
</dt> <dd>

„Der Parameter ist falsch.“ Kann auftreten, wenn das Objekt nicht ordnungsgemäß gefüllt ist oder wenn der Treiber im System nicht gefunden werden kann. Alternativ kann sich das Name-Attribut von dem in der INF-Datei angegebenen Modell unterscheiden. Oder es fehlt ein umgekehrter Schrägstrich \\ ("") für ein PathFile-Attribut.

</dd> <dt>

**1797**
</dt> <dd>

Der Druckertreiber ist unbekannt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> Wenn Sie die **AddPrinterDriver-Methode** verwenden, müssen Sie **SeLoadDriverPrivilege** verwenden, um einen Gerätetreiber zu laden oder zu entladen.

 

## <a name="examples"></a>Beispiele

Im Codebeispiel[Install a Printer Driver not Found in Drivers CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript (Install a Printer Driver Not Found in Drivers CAB VBScript) wird ein hypothetischer Drucker mit einem Druckertreiber installiert, der nicht in Drivers.cab gefunden wurde.

Im folgenden VBScript-Beispiel wird der Druckertreiber für einen Apple-Drucker Vom Autor 8500 installiert.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

