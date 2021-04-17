---
title: Die "stenabled"-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Aktiviert oder deaktiviert die Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD \ 160; Rap) durch Festlegen der aktivierten Eigenschaft.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode ""
- Remotedesktopdienste der Methode "" der Klasse "Win32_TSGatewayResourceAuthorizationPolicy"
- Win32_TSGatewayResourceAuthorizationPolicy Klasse Remotedesktopdienste, Methode "".
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478861"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Die "stenabled"-Methode der Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"

Aktiviert oder deaktiviert die Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP) durch Festlegen der **aktivierten** Eigenschaft.

## <a name="syntax"></a>Syntax


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktiviert* \[ in\]
</dt> <dd>

**True** gibt an, dass die RD-RAP aktiviert wird. Wenn der Wert **false** ist, wird die RD-RAP deaktiviert.

</dd> </dl>

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

 

