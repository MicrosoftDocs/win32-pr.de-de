---
title: Restoredefaults-Methode der Win32_TSPermissionsSetting-Klasse (Netfw. h)
description: Stellt die standardmäßigen Berechtigungs Satz Werte für das Terminal wieder her.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Restoredefaults-Methode Remotedesktopdienste
- Restoredefaults-Methode Remotedesktopdienste, Win32_TSPermissionsSetting-Klasse
- Win32_TSPermissionsSetting-Klasse Remotedesktopdienste, restoredefaults-Methode
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858802"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Restoredefaults-Methode der Win32 \_ tspermissionssetting-Klasse

Die **restoredefaults** -Methode stellt die standardmäßigen Berechtigungs Satz Werte für das Terminal wieder her.

## <a name="syntax"></a>Syntax


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück, andernfalls fehlgeschlagen.

## <a name="remarks"></a>Bemerkungen

Die Standard Berechtigungen lauten wie folgt:

-   Die Konten "Administratoren", "System" und "Remotedesktop Help Assistant" verfügen über alle [Remotedesktopdienste Berechtigungen](terminal-services-permissions.md).
-   Das Remotedesktop Benutzerkonto verfügt über die Berechtigungen anmelden, verbinden, Abfrage Informationen und Nachricht senden.
-   Die Konten "lokaler Dienst" und "Netzwerkdienst" verfügen über Abfrage Informationen und die Berechtigung "Nachricht senden".

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| Header<br/>                   | <dl> <dt>Netfw. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tspermissionssetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

