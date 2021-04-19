---
title: Die muvedown-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse.
description: Verschiebt die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap) eine Position unten in der Reihenfolge, in der RD \ 160; Caps werden ausgewertet.
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der
- Remotedesktopdienste-Methode, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste,-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e5b2e2b56a60d78f827f8989c0317cb003e511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342480"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Die Methode "Pfad" der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"

Verschiebt den aktuellen Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP) eine Position nach unten in der Reihenfolge, in der die RD-CAPs ausgewertet werden. Mit dieser Methode wird die **Order** -Eigenschaft der aktuellen RD-Obergrenze erhöht und die **Order** -Eigenschaft der RD-Obergrenze verringert, die der aktuellen RD-Obergrenze folgt.

## <a name="syntax"></a>Syntax


```mof
uint32 MoveDown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

