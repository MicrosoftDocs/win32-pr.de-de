---
description: Druckt eine Testseite.
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: PrintTestpage-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344006"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a>PrintTestpage-Methode der Win32- \_ Drucker Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode von **PrintTestPage** druckt eine Testseite.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 PrintTestPage();
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

Im folgenden PowerShell-Codebeispiel wird eine Testseite gedruckt.


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
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

 

