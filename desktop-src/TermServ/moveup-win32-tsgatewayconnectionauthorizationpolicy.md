---
title: MoveUp-Methode der Win32_TSGatewayConnectionAuthorizationPolicy Klasse
description: Verschiebt die aktuelle Remotedesktop-Verbindungsautorisierungsrichtlinie (RD \ 160; CAP) eine Position nach oben in der Reihenfolge rd \ 160; CAPs werden ausgewertet.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- MoveUp-Remotedesktopdienste
- MoveUp-Methode Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy klasse Remotedesktopdienste , MoveUp-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc5be4f15cee03097abcb52c50e3206d51872c8886970a49dbd20628f4b7beae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866370"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>MoveUp-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Verschiebt die aktuelle Remotedesktop-Verbindungsautorisierungsrichtlinie (RD CAP) in der Reihenfolge nach oben, in der RD-CAPs ausgewertet werden. Diese Methode dekrementiert die **Order-Eigenschaft** der aktuellen RD-CAP und erhöht die **Order-Eigenschaft** der RD-CAP, die der aktuellen RD-CAP vorausgegangen ist.

## <a name="syntax"></a>Syntax


```mof
uint32 MoveUp();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Movedown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

