---
title: GetDomain-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft den Namen der Domäne ab, der der Remotedesktop-Sitzungshost server (RD-Sitzungshost) angehört.
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- GetDomain-Methode Remotedesktopdienste
- GetDomain-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste , GetDomain-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613c3758d605727b50e8fb1bfbeebd1e475b00eb6673196c22be068bafd86499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001558"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a>GetDomain-Methode der Win32 \_ TerminalServiceSetting-Klasse

Ruft den Namen der Domäne ab, der der Remotedesktop-Sitzungshost server (RD-Sitzungshost) angehört.

## <a name="syntax"></a>Syntax


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Domäne* \[ out\]
</dt> <dd>

Der Domänenname des RD-Sitzungshost-Servers.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um eine Verbindung mit dem \\ \\ CIMV2 \\ TerminalServices-Stammnamespace herzustellen, muss die Authentifizierungsebene Paketdatenschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Bei Visual Basic- und Skriptaufrufen ist dies die Authentifizierungsebene **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Beispiel Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

