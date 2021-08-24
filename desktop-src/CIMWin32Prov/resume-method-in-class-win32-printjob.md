---
description: Die Resume WMI-Klassenmethode setzt einen angehaltenen Druckauftrag fort.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Resume-Methode der Win32_PrintJob Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dfc86b9b42c4373467fca89a46b2b4d8f42074e64836c554b325c8aebddf915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588210"
---
# <a name="resume-method-of-the-win32_printjob-class"></a>Resume-Methode der Win32 \_ PrintJob-Klasse

Die **Resume** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) setzt einen angehaltenen Druckauftrag fort.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.

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

Im folgenden VBScript-Codebeispiel werden alle Druckaufträge auf einem Computer fortgesetzt.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
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

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrintJob**](win32-printjob.md)
</dt> </dl>

 

