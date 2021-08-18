---
description: Setzt eine angehaltene Druckwarteschlange fort.
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Resume-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2663136708d26e026e0f2166cfc13177ef484e27f9f68edbfe1865a4178f255a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588230"
---
# <a name="resume-method-of-the-win32_printer-class"></a>Resume-Methode der \_ Win32-Druckerklasse

Die **Resume** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) setzt eine angehaltene Druckwarteschlange fort.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

</dd> </dl>

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

[**\_Win32-Drucker**](win32-printer.md)
</dt> <dt>

[**Pause-Methode**](pause-method-in-class-win32-printer.md)
</dt> </dl>

 

