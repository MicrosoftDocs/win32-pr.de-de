---
title: Win32_TSGatewayResourceGroup-Klasse
description: Beschreibt eine Ressourcengruppe, die eine Gruppe von Ressourcen (Computernamen) einer einzelnen Entität zulistet.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup-Klassen-Remotedesktopdienste
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ba4ec4545502d82a3449cee39954deb9b5b2e68bf7c657423e673c582d1c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603884"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>Win32 \_ TSGatewayResourceGroup-Klasse

Beschreibt eine Ressourcengruppe, die eine Gruppe von Ressourcen (Computernamen) einer einzelnen Entität zulistet.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSGatewayResourceGroup-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGatewayResourceGroup-Klasse** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | Fügt der **Resources-Eigenschaft** für diese Ressourcengruppe Ressourcen hinzu.<br/>      |
| [**Erstellen**](create-win32-tsgatewayresourcegroup.md)                   | Erstellt eine Ressourcengruppe.<br/>                                                  |
| [**Löschen**](delete-win32-tsgatewayresourcegroup.md)                   | Löscht diese Ressourcengruppe.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Löscht Ressourcen aus der **Resources-Eigenschaft** für diese Ressourcengruppe.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Legt die **Description-Eigenschaft** für diese Ressourcengruppe fest.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Legt die **Name-Eigenschaft** für diese Ressourcengruppe fest.<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | Legt die **Resources-Eigenschaft** für diese Ressourcengruppe fest.<br/>                   |
| [**Aktualisieren**](update-win32-tsgatewayresourcegroup.md)                   | Aktualisiert diese Ressourcengruppe.<br/>                                               |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSGatewayResourceGroup-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Durch Semikolons getrennte Liste der Remotedesktopdienste Ressourcenautorisierungsrichtlinien (RD RAPs), die dieser Ressourcengruppe zugeordnet sind.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibung der Ressourcengruppe. Diese Eigenschaft kann mit der [**SetDescription-Methode**](setdescription-win32-tsgatewayresourcegroup.md) geändert werden.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der Ressourcengruppe Diese Eigenschaft kann mit der [**SetName-Methode**](setname-win32-tsgatewayresourcegroup.md) geändert werden.

</dd> <dt>

**Ressourcen**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Durch Semikolons getrennte Liste von Ressourcen in dieser Ressourcengruppe. Ein \* "" bedeutet alle Ressourcen. Diese Eigenschaft kann mit den Methoden [**SetResources,**](setresources-win32-tsgatewayresourcegroup.md) [**AddResources,**](addresources-win32-tsgatewayresourcegroup.md) [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)und [**Update**](update-win32-tsgatewayresourcegroup.md) geändert werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

