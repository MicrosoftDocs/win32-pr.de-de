---
description: Platziert den Dienst, der durch das Win32 \_ PrinterDriver-Objekt dargestellt wird, im beendeten Zustand.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Stop Service-Methode der Win32_PrinterDriver-Klasse (sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041441"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a>Stop Service-Methode der Win32 \_ PrinterDriver-Klasse

Die **StopService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versetzt den Dienst, der durch das [**Win32 \_ PrinterDriver**](win32-printerdriver.md) -Objekt dargestellt wird, in den Zustand "beendet".

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Werte, die sich von den in der folgenden Liste aufgeführten Werten unterscheiden, finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Der Dienst wurde erfolgreich beendet.

</dd> <dt>

**1**
</dt> <dd>

Die Anforderung wird nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>           |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32- \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

