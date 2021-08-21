---
description: Versetzt den durch das Win32 PrinterDriver-Objekt dargestellten Dienst \_ in den Zustand "Beendet".
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: StopService-Methode der Win32_PrinterDriver-Klasse (Sdoias.h)
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
ms.openlocfilehash: 0ec49d6f5b9c7efcb860ba99eaf7984fa89cfb0bc12cbdfcfe8bde0db95eff1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020398"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a>StopService-Methode der Win32 \_ PrinterDriver-Klasse

Mit der [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** wird der durch das [**Win32 \_ PrinterDriver-Objekt**](win32-printerdriver.md) dargestellte Dienst in den Zustand "Beendet" versetzt.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Werte, die sich von denen in der folgenden Liste unterscheiden, finden Sie unter [**WMI-Fehlerkonstanten.**](/windows/desktop/WmiSdk/wmi-error-constants)

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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>           |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

