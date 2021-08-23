---
title: UpdateDirectConnectLicenseServer-Methode der Win32_TerminalServiceSetting-Klasse
description: UpdateDirectConnectLicenseServer ist nicht mehr verfügbar.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- UpdateDirectConnectLicenseServer-Methode Remotedesktopdienste
- UpdateDirectConnectLicenseServer-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting Klasse Remotedesktopdienste , UpdateDirectConnectLicenseServer-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca08147141ddbac5a2a483a2bf4a3aaf1e776b3694be115d3ee22ae76d3f058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868910"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>UpdateDirectConnectLicenseServer-Methode der Win32 \_ TerminalServiceSetting-Klasse

\[**UpdateDirectConnectLicenseServer** ist ab Windows Server 2008 R2 nicht mehr für die Verwendung verfügbar.\]

**Windows Server 2008:** Aktualisiert die Liste der Ermittlungslizenzserver. Die Serverliste wird durch Semikolons (";") getrennt.

## <a name="syntax"></a>Syntax


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LicenseServerList* \[ In\]
</dt> <dd>

Liste der Lizenzserver.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

