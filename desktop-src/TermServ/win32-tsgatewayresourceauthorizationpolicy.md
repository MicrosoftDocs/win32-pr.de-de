---
title: Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Beschreibt eine Remotedesktop Ressourcenautorisierungsrichtlinie (RD \ 160; RAP). Rd \ 160; MIT WIRD entschieden, ob ein Benutzer berechtigt ist, eine Verbindung mit einer angegebenen Ressource über Remotedesktop Gateway (RD-Gateway) herzustellen.
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy der Remotedesktopdienste
- Win32_TSGatewayResourceAuthorizationPolicy klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9748ddc4feccd504d823025ea70877004417717d625c904ccae4445f05e6eb03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999820"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse

Beschreibt eine Remotedesktop Ressourcenautorisierungsrichtlinie (RD RD RD). Ein RD-GATEWAY wird verwendet, um zu entscheiden, ob ein Benutzer berechtigt ist, eine Verbindung mit einer angegebenen Ressource über Remotedesktop Gateway (RD-Gateway) herzustellen.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse** verfügt über diese Methoden.



| Methode                                                                                          | Beschreibung                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Fügt den vorhandenen Benutzergruppen in der **UserGroupNames-Eigenschaft** die angegebenen Benutzergruppennamen hinzu.<br/>      |
| [**Erstellen**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Erstellt ein RD-RD-RD-SYSTEM.<br/>                                                                                       |
| [**Löschen**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Löscht die aktuelle RD-RD-Löschung.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Entfernt die angegebenen Benutzergruppennamen aus den vorhandenen Benutzergruppen in der **UserGroupNames-Eigenschaft.**<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Legt die **Description-Eigenschaft** für RD-RD-10 fest.<br/>                                                        |
| [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Aktiviert oder deaktiviert RD-RD-BENACHRICHTIGUNG durch Festlegen der **Enabled-Eigenschaft.**<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Legt die **Name-Eigenschaft** für RD-RD-10 fest.<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Legt die **PortNumbers-Eigenschaft** für RD-RD-RD-30 fest.<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Legt die **Eigenschaften ResourceGroupType** und **ResourceGroupName** fest.<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Legt die **UserGroupNames-Eigenschaft** für RD-RD-BENUTZERNAMEN fest.<br/>                                                     |
| [**Aktualisieren**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Aktualisiert das aktuelle RD-RD-RD-UPDATE.<br/>                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibung des RD-RD-WARNs. Diese Eigenschaft wird mit der [**SetDescription-Methode**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) geändert.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob dieses RD-RD-WARE aktiviert ist. Diese Eigenschaft wird mit der [**SetEnabled-Methode**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) geändert.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name des RD-RD-3D- Diese Eigenschaft wird mit der [**SetName-Methode**](setname-win32-tsgatewayresourceauthorizationpolicy.md) geändert.

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste der durch Semikolons getrennten Portnummern, die für diese Richtlinie zulässig sind. Um eine beliebige Portnummer zu ermöglichen, legen Sie " \* " fest.

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste der durch Semikolons getrennten Protokollnamen, die für diese Richtlinie aktiviert sind. Die Namen müssen mit der Rückgabe der [**GetProtocolName-Methode**](getprotocolname-win32-tsgatewayserversettings.md) der [**Win32 \_ TSGatewayServerSettings-Klasse**](win32-tsgatewayserversettings.md) übereinstimmen.

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ressourcengruppenname Diese Eigenschaft wird mit der [**SetResourceGroup-Methode**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) geändert.

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Typ der Ressourcengruppe. Diese Eigenschaft wird mit der [**SetResourceGroup-Methode**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) geändert.

<dt>

"RG"
</dt> <dd>

Ressourcengruppe

</dd> <dt>

"CG"
</dt> <dd>

Computergruppe, wie in Active Directory Domain Services.

</dd> <dt>

"ALL"
</dt> <dd>

Alle Ressourcen.

</dd> </dl>

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Durch Semikolons getrennte Liste von Benutzergruppennamen. Wenn der Benutzer zu einer dieser Benutzergruppen gehört, wird der Zugriff zugelassen. Diese Eigenschaft wird mit den [**Methoden SetUserGroupNames,**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)und [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) geändert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

