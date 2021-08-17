---
description: Die WMI-Klassenmethode SetDefaultPrinter legt den Standardsystemdrucker für den Benutzer fest, der die Methode aufruft.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: SetDefaultPrinter-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d896fe76946881ebbc52591da1bfce1fbc0fb99ce4adfb02418aa35b912f0e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440180"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a>SetDefaultPrinter-Methode der \_ Win32-Druckerklasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultPrinter** legt den Standardsystemdrucker für den Benutzer fest, der die Methode aufruft.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, und einen anderen Wert, wenn ein Fehler auftritt. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

## <a name="examples"></a>Beispiele

Im Beispiel Install a TCP/IP Printer Port and Printer VBScript [(TCP/IP-Druckerport installieren und VBScript-Drucker)](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) wird ein TCP/IP-Druckerport installiert, ein Drucker installiert und anschließend der Standarddrucker festgelegt.

Im folgenden VBScript-Codebeispiel wird der Standarddrucker auf einem Computer festgelegt.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
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

[WMI-Aufgaben: Drucker und Drucken](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**\_Win32-Drucker**](win32-printer.md)
</dt> </dl>

 

