---
title: FindLicenseServers-Methode der Win32_TerminalServiceSetting Klasse
description: Enumeriert alle Remotedesktop Lizenzserver und die Ermittlungsmethode.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- FindLicenseServers-Remotedesktopdienste
- FindLicenseServers-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , FindLicenseServers-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98af0d63c736e5bc82dd13d2abc94786634d7b92ba2c9a4628ae8ffd32a18b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130789"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a>FindLicenseServers-Methode der Win32 \_ TerminalServiceSetting-Klasse

Enumeriert alle Remotedesktop Lizenzserver und die Ermittlungsmethode.

## <a name="syntax"></a>Syntax


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LicenseServersList* \[ out\]
</dt> <dd>

Die Liste der [**Win32 \_ TSDiscoveredLicenseServer-Objekte.**](win32-tsdiscoveredlicenseserver.md) Jedes Objekt in der Ausgabeliste verfügt über den Namen des Remotedesktop Lizenzservers und die Ermittlungsmethode.

</dd> <dt>

*Anzahl* \[ out\]
</dt> <dd>

Die Gesamtanzahl der Remotedesktop lizenzservern in der Ausgabeliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um eine Verbindung mit dem \\ \\ CIMV2 TerminalServices-Stammnamespace herzustellen, muss \\ die Authentifizierungsebene den Paketschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Für Visual Basic- und Skriptaufrufe ist dies eine Authentifizierungsebene von **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

