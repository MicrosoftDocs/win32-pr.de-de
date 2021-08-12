---
title: SetName-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt einen neuen Namen für diese Remotedesktop Verbindungsautorisierungsrichtlinie fest (RD \ 160; CAP).
ms.assetid: 4a3b71d4-9b1c-46ea-b14a-fcbe32af37b5
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste , SetName-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbcfe0e56c4896ba3798766dc99cb439c72552d9122cfb749d1374d92dcde63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604649"
---
# <a name="setname-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>SetName-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Legt einen neuen Namen für diese Remotedesktop Verbindungsautorisierungsrichtlinie (RD CAP) fest.

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

Name der RD-CAP. Der Name darf maximal 64 Zeichen lang sein, eindeutig sein (die Anfrage wird ignoriert) und darf nicht die folgenden reservierten Zeichen enthalten:

<> : ; " / \\ \| ? \*\[TAB\]

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

