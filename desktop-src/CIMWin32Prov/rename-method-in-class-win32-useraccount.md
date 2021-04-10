---
description: Benennt einen Benutzerkonto Namen um.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Rename-Methode der Win32_UserAccount-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127364"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Rename-Methode der Win32 \_ User Account-Klasse

Die Methode zum **Umbenennen** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) benennt einen Benutzerkonto Namen um.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Neuer Kontoname.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte zurück. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolg.

</dd> <dt>

**Instanz nicht gefunden.**
</dt> <dd>

1

Die Instanz wurde nicht gefunden.

</dd> <dt>

**Instanz erforderlich**
</dt> <dd>

2

Die Instanz ist erforderlich.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

3

Ungültiger Parameter.

</dd> <dt>

**User not found (Benutzer wurde nicht gefunden)**
</dt> <dd>

4

Der Benutzer wurde nicht gefunden.

</dd> <dt>

**Domäne nicht gefunden**
</dt> <dd>

5

Die Domäne wurde nicht gefunden.

</dd> <dt>

**Der Vorgang ist nur auf dem primären Domänen Controller der Domäne zulässig.**
</dt> <dd>

6

Der Vorgang ist nur auf dem primären Domänen Controller der Domäne zulässig.

</dd> <dt>

**Der Vorgang ist für das letzte Administrator Konto nicht zulässig.**
</dt> <dd>

7

</dd> <dt>

**Der Vorgang ist für angegebene Sondergruppen nicht zulässig. Benutzer, Administrator, lokal oder Gast.**
</dt> <dd>

8

Der Vorgang ist für angegebene Sondergruppen nicht zulässig: Benutzer, Administrator, lokal oder Gast.

</dd> <dt>

**Anderer API-Fehler**
</dt> <dd>

9

Anderer API-Fehler.

</dd> <dt>

**Interner Fehler.**
</dt> <dd>

10

Interner Fehler.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird als Methode implementiert, um einen separaten Kontext für den neuen Namen bereitzustellen, der für den Namen, der der zu ändernden Instanz zugeordnet ist, nicht vom Schlüssel Eigenschafts Wert unterschieden werden kann.

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

[**Win32- \_ Benutzerkonto**](win32-useraccount.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

