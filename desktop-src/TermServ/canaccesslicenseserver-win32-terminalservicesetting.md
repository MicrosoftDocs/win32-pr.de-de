---
title: CanAccessLicenseServer-Methode der Win32_TerminalServiceSetting Klasse
description: CanAccessLicenseServer ist nicht mehr verfügbar.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- CanAccessLicenseServer-Remotedesktopdienste
- CanAccessLicenseServer-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , CanAccessLicenseServer-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0512f42d0d814793f4ecd62fda2dd84005a4183e8db736bd16919799b4570a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139143"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>CanAccessLicenseServer-Methode der Win32 \_ TerminalServiceSetting-Klasse

\[**CanAccessLicenseServer** ist ab Windows Server 2008 R2 nicht mehr verfügbar.\]

**Windows Server 2008: **

Bestimmt, ob der Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) Remotedesktopdienste-Clientzugriffslizenzen (RDS-CALs) von einem Remotedesktop-Lizenzserver anfordern darf, basierend auf folgendem Code:

-   Die Gruppenrichtlinieneinstellung "Lizenzserversicherheitsgruppe" auf dem Remotedesktop Lizenzserver.
-   Mitgliedschaft in der lokalen Gruppe Terminalservercomputer auf dem Lizenzserver.

## <a name="syntax"></a>Syntax


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerName* \[ In\]
</dt> <dd>

Der Name des Remotedesktop Lizenzservers.

</dd> <dt>

*AccessAllowed* \[ out\]
</dt> <dd>

Gibt an RD-Sitzungshost ob der RD-Sitzungshost RDS-CALs vom Lizenzserver anfordern darf.

<dt>

0
</dt> <dd>

Die Anforderung ist zulässig.

</dd> <dt>

1
</dt> <dd>

Die Anforderung ist nicht zulässig.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn RD-Sitzungshost Server Zugriff auf den Lizenzserver hat. Gibt **S \_ FALSE zurück,** RD-Sitzungshost Server keinen Zugriff auf den Lizenzserver hat.

## <a name="remarks"></a>Hinweise

Mit der Richtlinieneinstellung "Lizenzserversicherheitsgruppe" können Sie die RD-Sitzungshost angeben, die den Lizenzserver kontaktieren dürfen, um RDS-CALs zu erhalten. Wenn die Richtlinieneinstellung auf dem Lizenzserver aktiviert ist, antwortet der Lizenzserver nur auf RDS CAL-Anforderungen von RD-Sitzungshost-Servern, deren Computerkonten Mitglieder der lokalen Gruppe Terminalservercomputer auf dem Lizenzserver sind.

Um eine Verbindung mit dem \\ \\ CIMV2 TerminalServices-Stammnamespace herzustellen, muss \\ die Authentifizierungsebene den Paketschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Für Visual Basic- und Skriptaufrufe ist dies eine Authentifizierungsebene von **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

