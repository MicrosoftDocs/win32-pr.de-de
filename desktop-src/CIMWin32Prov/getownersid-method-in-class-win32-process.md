---
description: Die GetOwnerSID&\# 8194; Die WMI-Klassenmethode Ruft die Sicherheits-ID (SID) für den Besitzer dieses Prozesses ab.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: GetOwnerSID-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344349"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>GetOwnerSID-Methode der Win32- \_ Prozess Klasse

Die Methode " **GetOwnerSID** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " Ruft die Sicherheits-ID (SID) für den Besitzer dieses Prozesses ab.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sid* \[ vorgenommen\]
</dt> <dd>

Gibt den sicherheitsbezeichnerdeskriptor für diesen Prozess zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unzureichende Berechtigungen** (3)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

Der **Pfad wurde nicht gefunden** (9).
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Sonstige** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Beispiele

Im PowerShell-Codebeispiel " [angemeldeter Benutzer auf einem Remote System/s Version 2-](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell-Code" werden Remote Computer abgefragt, um festzustellen, wer angemeldet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Prozess**](win32-process.md)
</dt> </dl>

 

