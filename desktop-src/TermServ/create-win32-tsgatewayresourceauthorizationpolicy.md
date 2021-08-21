---
title: Create-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Erstellt eine Remotedesktop Ressourcenautorisierungsrichtlinie (RD \ 160; HIER WIRD DER 16.
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Erstellen einer Methode Remotedesktopdienste
- Erstellen einer Methode Remotedesktopdienste , Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste , Create-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a85055ed9c8930a47e9a9949693457456fd8f261e1cb458e1092eb570532231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131184"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Create-Methode der Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse

Erstellt eine Remotedesktop-Ressourcenautorisierungsrichtlinie (RDRAP).

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Name des RD-CSV.

</dd> <dt>

*Beschreibung* \[ In\]
</dt> <dd>

Beschreibung des RD-CSV.

</dd> <dt>

*Aktiviert* \[ In\]
</dt> <dd>

Gibt an, ob rd- UND RD-ENTEaktiviert werden soll.

</dd> <dt>

*ResourceGroupType* \[ In\]
</dt> <dd>

Ressourcengruppentyp.

<dt>

"RG"
</dt> <dd>

Ressourcengruppe

</dd> <dt>

"CG"
</dt> <dd>

Computergruppe, wie in Active Directory Domain Services gespeichert.

</dd> <dt>

"ALL"
</dt> <dd>

Alle Ressourcen.

</dd> </dl> </dd> <dt>

*ResourceGroupName* \[ In\]
</dt> <dd>

Ressourcengruppenname

</dd> <dt>

*UserGroupNames* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste von Benutzergruppennamen. Wenn der Benutzer einer dieser Benutzergruppen angehört, ist der Zugriff zulässig. Benutzergruppennamen sollten das Format *Domäne \\ UserGroupName aufweisen.*

</dd> <dt>

*ProtocolNames* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste von Protokollnamen, die für diese Richtlinie aktiviert sind. Namen müssen mit der Rückgabe der [**GetProtocolName-Methode**](getprotocolname-win32-tsgatewayserversettings.md) der [**Win32 \_ TSGatewayServerSettings-Klasse**](win32-tsgatewayserversettings.md) übereinstimmen.

</dd> <dt>

*PortNumbers* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste von Portnummern, die für diese Richtlinie aktiviert sind. Um eine beliebige Portnummer zuzulassen, legen Sie \* "" fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

