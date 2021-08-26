---
description: Ermöglicht das Ändern des Gruppennamens.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Umbenennen der Win32_Group-Klasse
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
ms.openlocfilehash: cff8f587426b45133716e308ea40785602fea2d5b5d30a99645bfd0c6cc5c4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003020"
---
# <a name="rename-method-of-the-win32_group-class"></a>Umbenennen der Win32 \_ Group-Klasse

Mit **der Methode** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) umbenennen kann der Gruppenname geändert werden.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Der Name des Windows Benutzerkontos in der Domäne, die durch die **Domain-Eigenschaft** dieser Klasse angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **Rename-Methode** kann die in der folgenden Liste aufgeführten Fehlercodes zurückgeben. Informationen zu ganzzahligen Werten, die nicht aufgelistet sind, finden Sie unter [ \_ WMI-Rückgabecodes.](/windows/desktop/WmiSdk/wmi-return-codes)

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolg.

</dd> <dt>

**Instanz nicht gefunden**
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

**Der Vorgang ist nur auf dem primären Domänencontroller der Domäne zulässig.**
</dt> <dd>

6

</dd> <dt>

**Der Vorgang ist für angegebene spezielle Gruppen nicht zulässig. Benutzer, Administrator, lokal oder Gast.**
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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32-Gruppe \_**](win32-group.md)
</dt> <dt>

[**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

