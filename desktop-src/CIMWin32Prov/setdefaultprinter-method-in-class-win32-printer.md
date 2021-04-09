---
description: Die WMI-Klassenmethode SetDefaultPrinter legt den Standardsystem Drucker für den Benutzer fest, der die-Methode aufruft.
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
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861739"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a>SetDefaultPrinter-Methode der Win32- \_ Drucker Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetDefaultPrinter** legt den Standardsystem Drucker für den Benutzer fest, der die-Methode aufruft.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) und einen anderen Wert zurück, wenn ein Fehler auftritt. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

## <a name="examples"></a>Beispiele

Im Beispiel [Installieren eines TCP/IP-Drucker Ports und eines Druckers](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript wird ein TCP/IP-Druckerport installiert, ein Drucker installiert und der Drucker als Standardwert festgelegt.

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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Tasks: Drucker und Drucken](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**Win32- \_ Drucker**](win32-printer.md)
</dt> </dl>

 

