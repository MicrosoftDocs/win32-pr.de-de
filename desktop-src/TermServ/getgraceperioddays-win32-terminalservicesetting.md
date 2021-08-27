---
title: GetGracePeriodDays-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft die Anzahl der Tage ab, die in der Remotedesktopdienste Lizenzierungs-Karenzzeit für einen Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) verbleiben. Ein Wert von 0 (null) gibt an, dass die Toleranzperiode vorbei ist.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- GetGracePeriodDays-Methode Remotedesktopdienste
- GetGracePeriodDays-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste , GetGracePeriodDays-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbfe1a99fb0b4f12db19f018d8acb3aaee6ab15a3560cd9140c3a05f36986585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010120"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>GetGracePeriodDays-Methode der Win32 \_ TerminalServiceSetting-Klasse

Ruft die Anzahl der Tage ab, die in der Remotedesktopdienste Lizenzierungs-Karenzzeit für einen Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) verbleiben. Ein Wert von 0 (null) gibt an, dass die Toleranzperiode vorbei ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DaysLeft* \[ out\]
</dt> <dd>

Die Anzahl der Tage, die in der Toleranzperiode verbleiben.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

