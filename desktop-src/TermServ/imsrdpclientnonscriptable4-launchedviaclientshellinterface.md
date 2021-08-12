---
title: IMsRdpClientNonScriptable4 LaunchViaClientShellInterface-Eigenschaft
description: Gibt an, ob der Benutzer das Clientsteuerelement mithilfe der Remotedesktop Webzugriff -Schnittstelle (RD-Webzugriff) gestartet hat.
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Eigenschaft "LaunchedViaClientShellInterface" Remotedesktopdienste
- LaunchViaClientShellInterface-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , LaunchViaClientShellInterface-Eigenschaft
- LaunchViaClientShellInterface-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , LaunchViaClientShellInterface-Eigenschaft
- LaunchViaClientShellInterface-Eigenschaft Remotedesktopdienste , MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste , LaunchViaClientShellInterface-Eigenschaft
- LaunchViaClientShellInterface-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , LaunchViaClientShellInterface-Eigenschaft
- LaunchViaClientShellInterface-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , LaunchViaClientShellInterface-Eigenschaft
- LaunchViaClientShellInterface-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , LaunchViaClientShellInterface-Eigenschaft
- LaunchViaClientShellInterface-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , LaunchViaClientShellInterface-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf4b3af34d274ae2ebfc34aed2a4256272daca2365966795de14d6b156562d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607588"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a>IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface-Eigenschaft

Gibt an, ob der Benutzer das Clientsteuerelement mithilfe der Remotedesktop Webzugriff -Schnittstelle (RD-Webzugriff) gestartet hat.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die **LaunchViaClientShellInterface-Eigenschaft** fest.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





