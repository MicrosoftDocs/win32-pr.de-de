---
title: RemoveComputerGroupNames-Methode der Win32_TSGatewayConnectionAuthorizationPolicy Klasse
description: Entfernt angegebene Computergruppennamen aus der ComputerGroupNames-Eigenschaft.
ms.assetid: 5f4e566a-1a2e-459d-ab6c-53ffd42271d8
ms.tgt_platform: multiple
keywords:
- RemoveComputerGroupNames-Remotedesktopdienste
- RemoveComputerGroupNames-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy klasse Remotedesktopdienste , RemoveComputerGroupNames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df87623ff9a6fe4ee7596b21db3fc03957473c1be8b0bff421aa342864edfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127620"
---
# <a name="removecomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>RemoveComputerGroupNames-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Entfernt angegebene Computergruppennamen aus der **ComputerGroupNames-Eigenschaft.**

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerGroupNames* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste der Computergruppennamen, die aus der **ComputerGroupNames-Eigenschaft entfernt werden.** Computergruppennamen müssen das Format *Domäne \\ ComputerGroupName haben.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Wenn mehrere Computergruppennamen im *Parameter ComputerGroupNames* enthalten sind und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

