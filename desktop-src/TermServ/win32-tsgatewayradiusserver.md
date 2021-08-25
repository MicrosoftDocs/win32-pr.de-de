---
title: Win32_TSGatewayRADIUSServer-Klasse
description: Beschreibt einen Remote Authentication Dial-In User Service -Server (RADIUS), der über eine Reihe von Remotedesktopdienste Verbindungsautorisierungsrichtlinien verfügt (RD \ 160; CAPs).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer klasse Remotedesktopdienste
- Win32_TSGatewayRADIUSServer klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9997494f9e93980ac4d6e4b1dcb9c95b0d7665a70226f77d1cd4c7ca3ad751d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769840"
---
# <a name="win32_tsgatewayradiusserver-class"></a>Win32 \_ TSGatewayRADIUSServer-Klasse

Beschreibt einen Remote Authentication Dial-In User Service -Server (RADIUS), der über eine Reihe von Remotedesktopdienste Verbindungsautorisierungsrichtlinien (CONNECTION Authorization Policies, RD-CAPs) verfügt.

RADIUS ist ein Branchenstandardprotokoll, das zum Übertragen von Authentifizierungs-, Autorisierungs- und Konfigurationsinformationen zwischen einem Servercomputer und einem Authentifizierungsserver verwendet wird, der als RADIUS-Server bezeichnet wird, mit einer Datenbank, die Benutzerinformationen speichert. Weitere Informationen finden Sie unter [RADIUS-Protokoll](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSGatewayRADIUSServer-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGatewayRADIUSServer-Klasse** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Hinzufügen**](win32-tsgatewayradiusserver-add.md)                         | Fügt einen neuen RADIUS-Server hinzu.<br/>                                         |
| [**Movedown**](movedown-win32-tsgatewayradiusserver.md)               | Verschiebt diesen RADIUS-Server in der Reihenfolge der Priorität um eine Position nach unten.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Verschiebt diesen RADIUS-Server in der Prioritäts reihenfolge um eine Position nach oben.<br/>   |
| [**Entfernen**](win32-tsgatewayradiusserver-remove.md)                   | Entfernt den aktuellen RADIUS-Server.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Legt die **Name-Eigenschaft** für diesen RADIUS-Server fest.<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Legt die **SharedSecret-Eigenschaft** für diesen RADIUS-Server fest.<br/>        |
| [**Aktualisieren**](update-win32-tsgatewayradiusserver.md)                   | Aktualisiert den aktuellen RADIUS-Server.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSGatewayRADIUSServer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name des RADIUS-Servers. Diese Eigenschaft kann mit der [**SetName-Methode geändert**](setname-win32-tsgatewayradiusserver.md) werden.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Priorität des RADIUS-Servers. Der RD-Gatewayserver sucht basierend auf der Priorität nach RD-CAPs auf RADIUS-Servern. Diese Eigenschaft kann mit den Methoden [**MoveUp,**](moveup-win32-tsgatewayradiusserver.md) [**MoveDown,**](movedown-win32-tsgatewayradiusserver.md) [**Add und**](win32-tsgatewayradiusserver-add.md) [**Remove geändert**](win32-tsgatewayradiusserver-remove.md) werden.

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gemeinsames Geheimnis für den RADIUS-Server. Diese Eigenschaft kann mit der [**SetSharedSecret-Methode geändert**](setsharedsecret-win32-tsgatewayradiusserver.md) werden.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

