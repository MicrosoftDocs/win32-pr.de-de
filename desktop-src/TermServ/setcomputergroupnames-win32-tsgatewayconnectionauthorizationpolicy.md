---
title: Setcomputergroupnames-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die computergroupnames-Eigenschaft fest.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- Setcomputergroupnames-Methode Remotedesktopdienste
- Setcomputergroupnames-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, setcomputergroupnames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391865"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Setcomputergroupnames-Methode der Win32- \_ Klasse "sgatewayconnectionauthorizationpolicy"

Legt die **computergroupnames** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computer groupnames* \[ in\]
</dt> <dd>

Liste von durch Semikolons getrennten Computer Gruppennamen. Dieser Wert kann leer sein. Die Namen weisen das Format *Domäne \\ computergroupname* auf. Wenn ein Wert angegeben wird, muss der Client Computer zu einer dieser Computer Gruppen gehören, damit der Benutzer auf den RD-Gateway Server zugreifen kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Wenn sich mehrere Computer Gruppennamen im *computergroupnames* -Parameter befinden und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.

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

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

