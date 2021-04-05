---
title: Die Methode "* tresourcegroup" der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt den Typ und den Namen der Ressourcengruppe fest.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "* tresourcegroup"
- Methode Remotedesktopdienste der Methode "Win32_TSGatewayResourceAuthorizationPolicy"
- Win32_TSGatewayResourceAuthorizationPolicy Klasse Remotedesktopdienste, Methode "*"
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
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859062"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Die Methode "* tresourcegroup" der Win32- \_ Klasse "zgatewayresourceauthorizationpolicy"

Legt den Typ und den Namen der Ressourcengruppe fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Resourcegroupname* \[ in\]
</dt> <dd>

Ressourcengruppenname Dieser Wert ersetzt die vorhandene **resourcegroupname** -Eigenschaft.

</dd> <dt>

*Resourcegrouptype* \[ in\]
</dt> <dd>

Identifiziert den Typ der Ressourcengruppe. Dieser Wert ersetzt die vorhandene **resourcegrouptype** -Eigenschaft.

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

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

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

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

