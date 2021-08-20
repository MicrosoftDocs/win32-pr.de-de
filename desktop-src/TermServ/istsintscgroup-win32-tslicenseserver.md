---
title: IsTSinTSCGroup-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob ein Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) Mitglied der lokalen Gruppe Terminalservercomputer auf dem Remotedesktop Lizenzserver ist.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- IsTSinTSCGroup-Methode Remotedesktopdienste
- IsTSinTSCGroup-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer Klasse Remotedesktopdienste , IsTSinTSCGroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60608a39beafc061a2271650f468c0a5c86de6892f972187f32519a2d9c91246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940874"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a>IsTSinTSCGroup-Methode der Win32 \_ TSLicenseServer-Klasse

Ruft ab, ob ein Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) Mitglied der lokalen Gruppe Terminalservercomputer auf dem Remotedesktop Lizenzserver ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tsname* \[ In\]
</dt> <dd>

Name des RD-Sitzungshost Servers.

</dd> <dt>

*IsMember* \[ out\]
</dt> <dd>

Boolescher Wert, der angibt, ob der RD-Sitzungshost Server Mitglied der lokalen Gruppe Terminalservercomputer ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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
</dt> </dl>

 

