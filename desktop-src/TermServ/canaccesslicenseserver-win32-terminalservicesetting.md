---
title: Canaccesslicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Canaccesslicenseserver ist nicht mehr verfügbar.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Canaccesslicenseserver-Methode Remotedesktopdienste
- Canaccesslicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, canaccesslicenseserver-Methode
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
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103174"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Canaccesslicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse

\[**Canaccesslicenseserver** ist nicht mehr für die Verwendung ab Windows Server 2008 R2 verfügbar.\]

* * Windows Server 2008: * *

Bestimmt, ob der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) von einem Remotedesktop Lizenzserver basierend auf folgenden Anforderungen anfordern kann:

-   Die Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" auf dem Remotedesktop-Lizenzserver.
-   Mitgliedschaft in der lokalen Gruppe "Terminal Server Computer" auf dem Lizenz Server.

## <a name="syntax"></a>Syntax


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* \[ in\]
</dt> <dd>

Der Name des Remotedesktop Lizenzservers.

</dd> <dt>

*AccessAllowed* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob der RD-Sitzungshost Server RDS-CALs vom Lizenzserver anfordern darf.

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

Gibt **S \_ OK** zurück, wenn der RD-Sitzungshost Server Zugriff auf den Lizenzserver hat. Gibt **" \_ false** " zurück, wenn der RD-Sitzungshost Server keinen Zugriff auf den Lizenzserver hat.

## <a name="remarks"></a>Bemerkungen

Mit der Richtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" können Sie die RD-Sitzungshost Server angeben, die den Lizenzserver zum Abrufen von RDS-CALs kontaktieren dürfen. Wenn die Richtlinien Einstellung auf dem Lizenzserver aktiviert ist, antwortet der Lizenzserver nur auf RDS-Client Zugriffs Anforderungen von RD-Sitzungshost Servern, deren Computer Konten Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Lizenzserver sind.

Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6. Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

