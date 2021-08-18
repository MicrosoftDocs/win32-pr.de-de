---
title: ExplicitLogon-Methode der Win32_TSLogonSetting-Klasse
description: Die ExplicitLogon-Methode legt die Anmeldeinformationen fest, die für die Authentifizierung verwendet werden sollen.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- ExplicitLogon-Methode Remotedesktopdienste
- ExplicitLogon-Methode Remotedesktopdienste , Win32_TSLogonSetting-Klasse
- Win32_TSLogonSetting Klasse Remotedesktopdienste , ExplicitLogon-Methode
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7303f06967d26276c7b43e06109cd9b37d664b960946afdffbb4f6a5a7c18821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137783"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>ExplicitLogon-Methode der Win32 \_ TSLogonSetting-Klasse

Die **ExplicitLogon-Methode** legt die Anmeldeinformationen fest, die für die Authentifizierung verwendet werden sollen.

## <a name="syntax"></a>Syntax


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserName* \[ In\]
</dt> <dd>

Die Anmeldeinformationen für den Benutzernamen.

</dd> <dt>

*Domäne* \[ In\]
</dt> <dd>

Die Anmeldeinformationen für die Domäne.

</dd> <dt>

*Kennwort* \[ In\]
</dt> <dd>

Die Anmeldeinformationen für das Kennwort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Erfolg bei Erfolg zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

