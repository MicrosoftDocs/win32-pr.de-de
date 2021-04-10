---
title: Setusergroupnames-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt die usergroupnames-Eigenschaft für die Remotedesktop-Ressourcen Autorisierungs Richtlinie fest (RD \ 160; Rap).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Setusergroupnames-Methode Remotedesktopdienste
- Setusergroupnames-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, setusergroupnames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104289"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Setusergroupnames-Methode der Win32- \_ Klasse "zgatewayresourceauthorizationpolicy"

Legt die **usergroupnames** -Eigenschaft für die Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Usergroupnames* \[ in\]
</dt> <dd>

Durch Semikolons getrennte Liste von Benutzergruppen Namen. Die Namen weisen das Format *Domäne \\ usergroupname* auf. Wenn der Benutzer zu einer dieser Benutzergruppen gehört, wird der Zugriff zugelassen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Wenn sich mehrere Benutzergruppen Namen im *usergroupnames* -Parameter befinden und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

