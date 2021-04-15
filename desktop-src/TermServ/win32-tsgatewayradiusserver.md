---
title: Win32_TSGatewayRADIUSServer-Klasse
description: Beschreibt einen Remote Authentication Dial-in User Service Server (RADIUS), der über eine Reihe von Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD \ 160; Caps).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste
- Win32_TSGatewayRADIUSServer Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476386"
---
# <a name="win32_tsgatewayradiusserver-class"></a>Win32-Klasse "t- \_ gatewayradiusserver"

Beschreibt einen Remote Authentication Dial-in User Service Server (RADIUS), der über eine Reihe von Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) verfügt.

RADIUS ist ein Industriestandard Protokoll, das zum Übertragen von Authentifizierung, Autorisierung und Konfigurationsinformationen zwischen einem Server Computer und einem authentifizier enden Server, der als RADIUS-Server bezeichnet wird, mit einer Datenbank verwendet wird, in der Benutzerinformationen gespeichert werden. Weitere Informationen finden Sie unter [RADIUS-Protokoll](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).

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

Die Win32-Klasse " **\_ zgatewayradiusserver** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zgatewayradiusserver** " verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Eren**](win32-tsgatewayradiusserver-add.md)                         | Fügt einen neuen RADIUS-Server hinzu.<br/>                                         |
| [**Nach unten**](movedown-win32-tsgatewayradiusserver.md)               | Verschiebt diesen RADIUS-Server in der Prioritäts Reihenfolge um eine Position nach unten.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Verschiebt diesen RADIUS-Server in der Prioritäts Reihenfolge um eine Position nach oben.<br/>   |
| [**Aufgeh**](win32-tsgatewayradiusserver-remove.md)                   | Entfernt den aktuellen RADIUS-Server.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Legt die **Name** -Eigenschaft für diesen RADIUS-Server fest.<br/>                |
| [**Setsharedsecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Legt die **sharedsecret** -Eigenschaft für diesen RADIUS-Server fest.<br/>        |
| [**Aktualisieren**](update-win32-tsgatewayradiusserver.md)                   | Aktualisiert den aktuellen RADIUS-Server.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "t- **\_ gatewayradiusserver** " verfügt über diese Eigenschaften.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des RADIUS-Servers. Diese Eigenschaft kann mit der [**SetName**](setname-win32-tsgatewayradiusserver.md) -Methode geändert werden.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Priorität des RADIUS-Servers. Der RD-Gateway Server sucht nach RD-CAPs auf RADIUS-Servern basierend auf der Priorität. Diese Eigenschaft kann mit den Methoden [**moveUp**](moveup-win32-tsgatewayradiusserver.md), [**muvedown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)und [**Remove**](win32-tsgatewayradiusserver-remove.md) geändert werden.

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gemeinsamer geheimer Schlüssel für den RADIUS-Server. Diese Eigenschaft kann mit der [**setsharedsecret**](setsharedsecret-win32-tsgatewayradiusserver.md) -Methode geändert werden.

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

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32-Datei " \_ zgatewayresourcegroup"**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

