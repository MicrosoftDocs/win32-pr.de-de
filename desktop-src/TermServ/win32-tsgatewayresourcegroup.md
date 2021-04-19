---
title: Win32_TSGatewayResourceGroup-Klasse
description: Beschreibt eine Ressourcengruppe, die eine Gruppe von Ressourcen (Computernamen) einer einzelnen Entität zuordnet.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste
- Win32_TSGatewayResourceGroup Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339964"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>Win32- \_ Klasse "zgatewayresourcegroup"

Beschreibt eine Ressourcengruppe, die eine Gruppe von Ressourcen (Computernamen) einer einzelnen Entität zuordnet.

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

Die Win32-Klasse "t- **\_ gatewayresourcegroup** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse "t- **\_ gatewayresourcegroup** " verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResource**](addresources-win32-tsgatewayresourcegroup.md)       | Fügt der **Ressourcen** Eigenschaft für diese Ressourcengruppe Ressourcen hinzu.<br/>      |
| [**Stelle**](create-win32-tsgatewayresourcegroup.md)                   | Erstellt eine Ressourcengruppe.<br/>                                                  |
| [**Lösch**](delete-win32-tsgatewayresourcegroup.md)                   | Löscht diese Ressourcengruppe.<br/>                                               |
| [**Removeresources**](removeresources-win32-tsgatewayresourcegroup.md) | Löscht Ressourcen aus der **Ressourcen** Eigenschaft für diese Ressourcengruppe.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Legt die **Beschreibungs** Eigenschaft für diese Ressourcengruppe fest.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Legt die **Name** -Eigenschaft für diese Ressourcengruppe fest.<br/>                        |
| [**Abtresources**](setresources-win32-tsgatewayresourcegroup.md)       | Legt die **Ressourcen** Eigenschaft für diese Ressourcengruppe fest.<br/>                   |
| [**Aktualisieren**](update-win32-tsgatewayresourcegroup.md)                   | Aktualisiert diese Ressourcengruppe.<br/>                                               |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ zgatewayresourcegroup** " verfügt über diese Eigenschaften.

<dl> <dt>

**Associatedraps**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Durch Semikolons getrennte Liste von Remotedesktopdienste-Ressourcen Autorisierungs Richtlinien (RD-RAPs), die dieser Ressourcengruppe zugeordnet sind.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibung der Ressourcengruppe. Diese Eigenschaft kann mit der [**setDescription**](setdescription-win32-tsgatewayresourcegroup.md) -Methode geändert werden.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der Ressourcengruppe Diese Eigenschaft kann mit der [**SetName**](setname-win32-tsgatewayresourcegroup.md) -Methode geändert werden.

</dd> <dt>

**Ressourcen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Durch Semikolons getrennte Liste von Ressourcen in dieser Ressourcengruppe. Ein " \* " bedeutet alle Ressourcen. Diese Eigenschaft kann mit den Methoden "Settings", " [**adresssources**](addresources-win32-tsgatewayresourcegroup.md) [**", "**](setresources-win32-tsgatewayresourcegroup.md) [**removeresources**](removeresources-win32-tsgatewayresourcegroup.md)" und " [**Update**](update-win32-tsgatewayresourcegroup.md) " geändert werden.

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

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

