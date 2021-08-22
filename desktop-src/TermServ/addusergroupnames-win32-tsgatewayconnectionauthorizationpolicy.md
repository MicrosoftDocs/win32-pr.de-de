---
title: AddUserGroupNames-Methode der Win32_TSGatewayConnectionAuthorizationPolicy Klasse
description: Fügt der UserGroupNames-Eigenschaft die angegebenen Benutzergruppennamen hinzu.
ms.assetid: 01bbccc3-c2e4-46ad-8649-1a30e001c949
ms.tgt_platform: multiple
keywords:
- AddUserGroupNames-Remotedesktopdienste
- AddUserGroupNames-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy klasse Remotedesktopdienste , AddUserGroupNames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f11e9c801b408db34325b77510a50608e34f0631ce4af132065f7ad3dc4bc41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401740"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>AddUserGroupNames-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Fügt der **UserGroupNames-Eigenschaft** die angegebenen Benutzergruppennamen hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserGroupNames* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste von Benutzergruppennamen, die der **UserGroupNames-Eigenschaft hinzugefügt werden.** Benutzergruppennamen müssen das Format *Domain \\ UserGroupName haben.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Wenn mehrere Benutzergruppennamen im *UserGroupNames-Parameter* enthalten sind und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

