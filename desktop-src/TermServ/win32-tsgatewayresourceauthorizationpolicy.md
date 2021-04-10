---
title: Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Beschreibt eine Remotedesktop Ressourcen Autorisierungs Richtlinie (RD \ 160; Rap). A RD \ 160; Rap wird verwendet, um zu entscheiden, ob ein Benutzer autorisiert ist, über Remotedesktop Gateway (RD-Gateway) eine Verbindung mit einer angegebenen Ressource herzustellen.
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste
- Win32_TSGatewayResourceAuthorizationPolicy Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040530"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"

Beschreibt eine Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP). Eine RD-RAP wird verwendet, um zu entscheiden, ob ein Benutzer autorisiert ist, über Remotedesktop Gateway (RD-Gateway) eine Verbindung mit einer angegebenen Ressource herzustellen.

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

Die Win32-Klasse " **\_ zgatewayresourceauthorizationpolicy** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zgatewayresourceauthorizationpolicy** " verfügt über diese Methoden.



| Methode                                                                                          | BESCHREIBUNG                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Addusergroupnames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Fügt die angegebenen Benutzergruppen Namen den vorhandenen Benutzergruppen in der **usergroupnames** -Eigenschaft hinzu.<br/>      |
| [**Stelle**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Erstellt eine RD-RAP.<br/>                                                                                       |
| [**Lösch**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Löscht die aktuelle RD-RAP.<br/>                                                                              |
| [**Removeusergroupnames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Entfernt die angegebenen Benutzergruppen Namen aus den vorhandenen Benutzergruppen in der **usergroupnames** -Eigenschaft.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Legt die **Description** -Eigenschaft für die RD-RAP fest.<br/>                                                        |
| [**Abgeleitete**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Aktiviert oder deaktiviert die RD-RAP durch Festlegen der **aktivierten** Eigenschaft.<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Legt die **Name** -Eigenschaft für die RD-RAP fest.<br/>                                                               |
| [**Setportnumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Legt die **portnumbers** -Eigenschaft für die RD-RAP fest.<br/>                                                        |
| [**"Abtresourcegroup"**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Legt die Eigenschaften **resourcegrouptype** und **resourcegroupname** fest.<br/>                                     |
| [**Setusergroupnames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Legt die **usergroupnames** -Eigenschaft für die RD-RAP fest.<br/>                                                     |
| [**Aktualisieren**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Aktualisiert die aktuelle RD-RAP.<br/>                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "t- **\_ gatewayresourceauthorizationpolicy** " verfügt über diese Eigenschaften.

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibung der RD-RAP. Diese Eigenschaft wird mit der [**setDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) -Methode geändert.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob diese RD-RAP aktiviert ist. Diese Eigenschaft wird [**mit der Methode**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) "" der Methode "*" geändert.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der RD-RAP. Diese Eigenschaft wird mit der [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) -Methode geändert.

</dd> <dt>

**Portnummern**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste von durch Semikolons getrennten Portnummern, die für diese Richtlinie zulässig sind. Um eine beliebige Portnummer zuzulassen, legen Sie " \* " fest.

</dd> <dt>

**Protocolnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste von durch Semikolons getrennten Protokollnamen, die für diese Richtlinie aktiviert sind. Namen müssen mit der Rückgabe der [**getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) -Methode der Win32-Klasse " [**\_ tgatewayserversettings**](win32-tsgatewayserversettings.md) " identisch sein.

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ressourcengruppenname Diese Eigenschaft wird [**mit der Methode**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) "" der Methode "*" geändert.

</dd> <dt>

**Resourcegrouptype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Typ der Ressourcengruppe. Diese Eigenschaft wird [**mit der Methode**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) "" der Methode "*" geändert.

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

</dd> </dl>

</dd> <dt>

**Usergroupnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Durch Semikolons getrennte Liste von Benutzergruppen Namen. Wenn der Benutzer zu einer dieser Benutzergruppen gehört, wird der Zugriff zugelassen. Diese Eigenschaft wird mit den Methoden [**setusergroupnames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**addusergroupnames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)und [**removeusergroupnames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) geändert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.

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

[**Win32-"- \_ gatewayconnection"**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32-"t- \_ gatewayloadbalancer"**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32-"t- \_ gatewayradiusserver"**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32-Datei " \_ zgatewayresourcegroup"**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

