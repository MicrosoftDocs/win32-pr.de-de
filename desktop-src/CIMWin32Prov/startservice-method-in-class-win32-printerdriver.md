---
description: Mit der StartService-Methode wird der Dienst in den Zustand Gestartet versetzt.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: StartService-Methode der Win32_PrinterDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe5afb79f2c5d74f2e9a68093cb98ac0b8597d767a747c8bd66b766ba72dd00f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752380"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a>StartService-Methode der Win32 \_ PrinterDriver-Klasse

Mit der **StartService-Methode** wird der Dienst in den Zustand Gestartet versetzt.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Werte, die sich von denen in der folgenden Liste unterscheiden, finden Sie unter [**WMI-Fehlerkonstanten.**](/windows/desktop/WmiSdk/wmi-error-constants)

<dl> <dt>

**0**
</dt> <dd>

Der Dienst wurde erfolgreich gestartet.

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
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

