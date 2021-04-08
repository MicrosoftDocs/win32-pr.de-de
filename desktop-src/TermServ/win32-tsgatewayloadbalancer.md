---
title: Win32_TSGatewayLoadBalancer-Klasse
description: Beschreibt eine Gruppe von Remotedesktop Gateway-Lasten Ausgleichs Servern (RD-Gateway). Diese werden verwendet, um einen Lastenausgleich RD-Gateway Verbindungen über mehrere Server hinweg durchzusetzen.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer-Klasse Remotedesktopdienste
- Win32_TSGatewayLoadBalancer Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741249"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>Win32-Klasse "t- \_ gatewayloadbalancer"

Beschreibt eine Gruppe von Remotedesktop Gateway-Lasten Ausgleichs Servern (RD-Gateway). Diese werden verwendet, um einen Lastenausgleich RD-Gateway Verbindungen über mehrere Server hinweg durchzusetzen.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ zgatewayloadbalancer** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zgatewayloadbalancer** " verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**Addservers**](addservers-win32-tsgatewayloadbalancer.md)                       | Fügt der **Server** Eigenschaft Server hinzu.<br/>                                                             |
| [**Deleteallservers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Löscht alle RD-Gateway Lasten Ausgleichs Server, die Teil der Lasten Ausgleichs Farm sind.<br/>               |
| [**Delta Server**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Löscht Server aus der **Server** -Eigenschaft.<br/>                                                        |
| [**Isloadbalancingserver**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Bestimmt, ob der Server einen Lastenausgleich durchführen kann.<br/>                                             |
| [**Setservers**](setservers-win32-tsgatewayloadbalancer.md)                       | Legt die **Server** -Eigenschaft mit der durch Semikolons getrennten Liste von RD-Gateway Lasten Ausgleichs Servern fest.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "t- **\_ gatewayloadbalancer** " verfügt über diese Eigenschaften.

<dl> <dt>

**Server**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Durch Semikolons getrennte Liste der RD-Gateway Lasten Ausgleichs Server. Diese Eigenschaft kann mit den Methoden [**setservers**](setservers-win32-tsgatewayloadbalancer.md), [**addservers**](addservers-win32-tsgatewayloadbalancer.md), [**deleteservers**](deleteservers-win32-tsgatewayloadbalancer.md)und [**deleteallservers**](deleteallservers-win32-tsgatewayloadbalancer.md) geändert werden.

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

[**Win32-"t- \_ gatewayradiusserver"**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32-Datei " \_ zgatewayresourcegroup"**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

