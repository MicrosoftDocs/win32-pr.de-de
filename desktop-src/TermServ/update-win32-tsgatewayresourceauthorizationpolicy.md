---
title: Update-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Aktualisiert die aktuelle Remotedesktop Ressourcen Autorisierungs Richtlinie (RD \ 160; Rap).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Update-Methode Remotedesktopdienste
- Update-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, Update-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104282"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Update-Methode der Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"

Aktualisiert die aktuelle Remotedesktop Ressourcen Autorisierungs Richtlinie (RD-RAP).

## <a name="syntax"></a>Syntax


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Name der RD-RAP.

</dd> <dt>

*Beschreibung* \[ in\]
</dt> <dd>

Beschreibung der RD-RAP.

</dd> <dt>

*Aktiviert* \[ in\]
</dt> <dd>

Gibt an, ob die RD-RAP aktiviert werden soll.

</dd> <dt>

*Resourcegroupname* \[ in\]
</dt> <dd>

Name der Ressourcengruppe, die mit dieser RD-RAP verknüpft ist.

</dd> <dt>

*Resourcegrouptype* \[ in\]
</dt> <dd>

Der Ressourcen Gruppentyp.

<dt>

Sorgte
</dt> <dd>

Ressourcengruppe

</dd> <dt>

Gewöhnt
</dt> <dd>

Computer Gruppe, wie in Active Directory Domain Services gespeichert.

</dd> <dt>

Allen
</dt> <dd>

Alle Ressourcen.

</dd> </dl> </dd> <dt>

*Usergroupnames* \[ in\]
</dt> <dd>

Durch Semikolons getrennte Liste von Benutzergruppen Namen. Die Namen weisen das Format *Domäne \\ usergroupname* auf. Wenn der Benutzer zu einer dieser Benutzergruppen gehört, wird der Zugriff zugelassen.

</dd> <dt>

*Protocolnames* \[ in\]
</dt> <dd>

Durch Semikolons getrennte Liste der Protokollnamen, die für diese Richtlinie aktiviert sind. Namen müssen mit der Rückgabe der [**getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) -Methode der Win32-Klasse " [**\_ tgatewayserversettings**](win32-tsgatewayserversettings.md) " identisch sein.

</dd> <dt>

*Portnummern* \[ in\]
</dt> <dd>

Durch Semikolons getrennte Liste von Portnummern, die für diese Richtlinie aktiviert sind. Um eine beliebige Portnummer zuzulassen, legen Sie " \* " fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

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

 

