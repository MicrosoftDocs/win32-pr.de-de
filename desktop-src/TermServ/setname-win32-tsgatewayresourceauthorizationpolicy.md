---
title: SetName-Methode der Win32_TSGatewayResourceAuthorizationPolicy Klasse
description: Legt die Name-Eigenschaft für die Remotedesktop Ressourcenautorisierungsrichtlinie fest (RD \ 160; RAP).
ms.assetid: 3a652ece-11fe-4aa7-913d-39ef96ab1633
ms.tgt_platform: multiple
keywords:
- SetName-Remotedesktopdienste
- SetName-Methode Remotedesktopdienste , Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy der Remotedesktopdienste , SetName-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df296ec4fc9dbb1b28a6cc5382f8197241c7e8557192dcf2ffe30af19cf9bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350011"
---
# <a name="setname-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>SetName-Methode der Win32 \_ TSGatewayResourceAuthorizationPolicy-Klasse

Legt die **Name-Eigenschaft** für die Remotedesktop Resource Authorization Policy (RD RD RD) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Name des RD-RD-3D- Der Name muss mindestens 64 Zeichen lang sein, muss eindeutig sein (case wird ignoriert) und darf nicht die folgenden reservierten Zeichen enthalten:

<> : ; " / \\ \| ? \*\[REGISTERKARTE\]

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

