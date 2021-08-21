---
description: Stellt eine Verbindung mit einem vorhandenen Drucker im Netzwerk bereit und fügt sie der Liste der verfügbaren Drucker hinzu.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: AddPrinterConnection-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1383277a7a31e5b5e035538ce905607ee1960ee7b70cce4640cfc0e4346c3d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081074"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a>AddPrinterConnection-Methode der \_ Win32-Druckerklasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** stellt eine Verbindung mit einem vorhandenen Drucker im Netzwerk bereit und fügt sie der Liste der verfügbaren Drucker hinzu.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Anzeigename für den Drucker.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**0**
</dt> <dd>

Erfolg

</dd> <dt>

**5**
</dt> <dd>

Zugriff verweigert

</dd> <dt>

**1801**
</dt> <dd>

Ungültiger Druckername

</dd> <dt>

**1930**
</dt> <dd>

Inkompatibler Druckertreiber

</dd> </dl>

## <a name="examples"></a>Beispiele

Im [PowerShell-Beispiel Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) werden alle Druckertreiber von einem angegebenen Druckerserver installiert.

Das [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell-Beispiel listet freigegebene Drucker auf einem Remotecomputer auf und bietet Ihnen die Möglichkeit, ihrem Computer eine Druckerverbindung vom Remotecomputer hinzuzufügen.

Im folgenden VBScript-Codebeispiel wird ein lokaler Drucker hinzugefügt.


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Aufgaben: Drucker und Drucken](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**\_Win32-Drucker**](win32-printer.md)
</dt> </dl>

 

