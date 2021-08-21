---
title: SetResourceGroup-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt den Ressourcengruppentyp und -namen fest.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- SetResourceGroup-Methode Remotedesktopdienste
- SetResourceGroup-Methode Remotedesktopdienste , Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste , SetResourceGroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29c4ca301a26fb3199891f3d25141f69402ecfe55bc46a2f3581c31e99b9445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058448"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>SetResourceGroup-Methode der Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse

Legt den Ressourcengruppentyp und -namen fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ResourceGroupName* \[ In\]
</dt> <dd>

Ressourcengruppenname Dieser Wert ersetzt die vorhandene **ResourceGroupName-Eigenschaft.**

</dd> <dt>

*ResourceGroupType* \[ In\]
</dt> <dd>

Gibt den Typ der Ressourcengruppe an. Dieser Wert ersetzt die vorhandene **ResourceGroupType-Eigenschaft.**

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

</dd> </dl> </dd> </dl>

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

 

