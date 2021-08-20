---
title: IsSecureAccessAllowed-Methode der Win32_TSLicenseServer Klasse
description: Ruft ab, ob ein Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) client access licenses (RDS \ 160) Remotedesktopdienste Clientzugriffslizenzen anfordern darf. CALs) vom Remotedesktop Lizenzserver.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- IsSecureAccessAllowed-Remotedesktopdienste
- IsSecureAccessAllowed-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer klasse Remotedesktopdienste , IsSecureAccessAllowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6109eb363459432d50d54eb8521f0f23bb54a0836c82f92af20a5b83b64f1d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351361"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>IsSecureAccessAllowed-Methode der Win32 \_ TSLicenseServer-Klasse

Ruft ab, ob ein Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) Remotedesktopdienste Clientzugriffslizenzen (RDS-CALs) vom Remotedesktop anfordern darf.

## <a name="syntax"></a>Syntax


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tsname* \[ In\]
</dt> <dd>

Name des RD-Sitzungshost Servers.

</dd> <dt>

*Zulässig* \[ out\]
</dt> <dd>

Boolescher Wert, der angibt, ob der RD-Sitzungshost Server RDS-CALs vom Lizenzserver anfordern darf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Der zurückgegebene Wert basiert auf der Gruppenrichtlinieneinstellung "Lizenzserversicherheitsgruppe" und der Mitgliedschaft in der lokalen Gruppe Terminalservercomputer auf dem Remotedesktop Lizenzserver.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

