---
description: Ermöglicht, dass der Gruppenname geändert wird.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Rename-Methode der Win32_Group-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345606"
---
# <a name="rename-method-of-the-win32_group-class"></a>Rename-Methode der Win32- \_ Gruppenklasse

Die Methode zum **Umbenennen** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) ermöglicht, dass der Gruppenname geändert wird.

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

Der Name des Windows-Benutzerkontos in der Domäne, die durch die **Domänen** Eigenschaft dieser Klasse angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **Rename** -Methode kann die in der folgenden Liste aufgeführten Fehlercodes zurückgeben. Weitere ganzzahlige Werte als die aufgeführten Werte finden Sie unter [WMI- \_ Rückgabe Codes](/windows/desktop/WmiSdk/wmi-return-codes).

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolg.

</dd> <dt>

**Instanz nicht gefunden.**
</dt> <dd>

1

</dd> <dt>

**Instanz erforderlich**
</dt> <dd>

2

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

3

</dd> <dt>

**Gruppe nicht gefunden**
</dt> <dd>

4

</dd> <dt>

**Domäne nicht gefunden**
</dt> <dd>

5

</dd> <dt>

**Der Vorgang ist nur auf dem primären Domänen Controller der Domäne zulässig.**
</dt> <dd>

6

</dd> <dt>

**Der Vorgang ist für angegebene Sondergruppen nicht zulässig. Benutzer, Administrator, lokal oder Gast.**
</dt> <dd>

7

</dd> <dt>

**Anderer API-Fehler**
</dt> <dd>

8

</dd> <dt>

**Interner Fehler.**
</dt> <dd>

9

</dd> </dl>

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

[**Win32- \_ Gruppe**](win32-group.md)
</dt> <dt>

[**Win32 \_ logicalfilesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

