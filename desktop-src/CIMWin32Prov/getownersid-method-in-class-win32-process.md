---
description: GetOwnerSid&\# 8194; Die WMI-Klassenmethode ruft die Sicherheits-ID (SID) für den Besitzer dieses Prozesses ab.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: GetOwnerSid-Methode der Win32_Process Klasse
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
ms.openlocfilehash: 2884c0f1cd3cc6e32a2db1ab14824ba3112624002cb10f4d76782d622e069000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918380"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>GetOwnerSid-Methode der Win32 \_ Process-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** ruft die Sicherheits-ID (SID) für den Besitzer dieses Prozesses ab.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sid* \[ out\]
</dt> <dd>

Gibt den Sicherheitsbezeichnerdeskriptor für diesen Prozess zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt null (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unzureichende Berechtigungen** (3)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

**Pfad nicht gefunden** (9)
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Andere** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Beispiele

Im PowerShell-Codebeispiel Find the [logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) (Suchen der angemeldeten Benutzer auf einem/einer Remotesystemversion 2) werden Remotecomputer abgefragt, um zu sehen, wer angemeldet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32-Prozess \_**](win32-process.md)
</dt> </dl>

 

