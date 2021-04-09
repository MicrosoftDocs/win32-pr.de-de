---
description: Entfernt alle Aufträge, einschließlich der derzeit aus der Warteschlange druckbaren Aufträge.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Cancelalljobs-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860767"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a>Cancelalljobs-Methode der Win32- \_ Drucker Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **cancelalljobs** entfernt alle Aufträge, einschließlich der derzeit aus der Warteschlange druckbaren Aufträge.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Erfolg

</dd> <dt>

**5**
</dt> <dd>

Zugriff verweigert

</dd> </dl>

## <a name="examples"></a>Beispiele

Die [Meldung Benutzer benachrichtigen, wenn eine Druck Warteschlange gelöscht wird](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) verwendet Msg.exe, um eine Netzwerk Warnung an alle Benutzer zu senden, die Dokumente in einer Druck Warteschlange für den Löschvorgang verwendet haben. Nach dem Senden der Warnungen löscht das Skript die Druck Warteschlange.

Das Codebeispiel [delete all Print Jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript löscht alle Druckaufträge auf dem lokalen Computer.

Im folgenden VBScript-Beispiel werden alle Druckaufträge für einen Drucker mit dem Namen HP QuietJet gelöscht.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
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

[**Win32- \_ Drucker**](win32-printer.md)
</dt> </dl>

 

