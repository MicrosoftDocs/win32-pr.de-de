---
title: Win32_TSGatewayLoadBalancer-Klasse
description: Beschreibt eine Reihe von Lastenausgleichsservern Remotedesktop Gateways (RD-Gateway). Diese werden zum Lastenausgleich von RD-Gatewayverbindungen über mehrere Server hinweg verwendet.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer-Remotedesktopdienste
- Win32_TSGatewayLoadBalancer klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584077911faf8593e7c26aadd36ca17a0a11d82b18d1d6ade20be1f1444fedf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769870"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>Win32 \_ TSGatewayLoadBalancer-Klasse

Beschreibt eine Reihe von Lastenausgleichsservern Remotedesktop Gateways (RD-Gateway). Diese werden zum Lastenausgleich von RD-Gatewayverbindungen über mehrere Server hinweg verwendet.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSGatewayLoadBalancer-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGatewayLoadBalancer-Klasse** verfügt über diese Methoden.



| Methode                                                                             | Beschreibung                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)                       | Fügt der **Server-Eigenschaft Server** hinzu.<br/>                                                             |
| [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Löscht alle RD-Gateway-Lastenausgleichsserver, die an der Lastenausgleichsfarm teilnehmen.<br/>               |
| [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Löscht Server aus der **Server-Eigenschaft.**<br/>                                                        |
| [**IsLoadBalancingServer**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Bestimmt, ob der Server einen Lastenausgleich durchführen kann.<br/>                                             |
| [**SetServers**](setservers-win32-tsgatewayloadbalancer.md)                       | Legt die **Server-Eigenschaft** mit der durch Semikolons getrennten Liste von RD-Gateway-Lastenausgleichsservern fest.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSGatewayLoadBalancer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Server**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Durch Semikolons getrennte Liste von RD-Gateway-Lastenausgleichsservern. Diese Eigenschaft kann mit den Methoden [**SetServers,**](setservers-win32-tsgatewayloadbalancer.md) [**AddServers,**](addservers-win32-tsgatewayloadbalancer.md) [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)und [**DeleteAllServers geändert**](deleteallservers-win32-tsgatewayloadbalancer.md) werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

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

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

