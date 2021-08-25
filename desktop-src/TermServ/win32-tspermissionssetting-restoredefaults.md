---
title: RestoreDefaults-Methode der Win32_TSPermissionsSetting-Klasse (Netfw.h)
description: Stellt die Standardberechtigungssatzwerte für das Terminal wieder her.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- RestoreDefaults-Methode Remotedesktopdienste
- RestoreDefaults-Methode Remotedesktopdienste , Win32_TSPermissionsSetting-Klasse
- Win32_TSPermissionsSetting-Klasse Remotedesktopdienste , RestoreDefaults-Methode
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
ms.openlocfilehash: 8ef81f4b3008f68129026a90d1b2e98e8c13c298537952175e116c9c8e02c4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769450"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>RestoreDefaults-Methode der Win32 \_ TSPermissionsSetting-Klasse

Die **RestoreDefaults-Methode** stellt die Standardberechtigungssatzwerte für das Terminal wieder her.

## <a name="syntax"></a>Syntax


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt Erfolg bei Erfolg zurück, andernfalls Fehler.

## <a name="remarks"></a>Hinweise

Die Standardberechtigungen sind:

-   Die Konten Administratoren, System und Remotedesktop Help Assistant verfügen über alle [Remotedesktopdienste Berechtigungen.](terminal-services-permissions.md)
-   Das konto Remotedesktop Users verfügt über die Berechtigungen Anmelden, Verbinden, Abfrageinformationen und Nachricht senden.
-   Die Konten lokaler Dienst und Netzwerkdienst verfügen über Abfrageinformationen und die Berechtigung Nachricht senden.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| Header<br/>                   | <dl> <dt>Netfw.h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

