---
title: IMsRdpClientShell IsRemoteProgramClientInstalled (Eigenschaft)
description: Ruft ab, ob der Remotedesktopverbindung -Client (RDC) Windows Server 2008 R2 RemoteApp-Funktionalität unterstützt.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- IsRemoteProgramClientInstalled-Remotedesktopdienste
- IsRemoteProgramClientInstalled-Eigenschaft Remotedesktopdienste , IMsRdpClientShell-Schnittstelle
- IMsRdpClientShell-Schnittstelle Remotedesktopdienste , IsRemoteProgramClientInstalled (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3073bb9a9e5890ff7a6a46bb9ea0c03964bf54f1c91550dbb2746385a11fa809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129763"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>IMsRdpClientShell::IsRemoteProgramClientInstalled (Eigenschaft)

Ruft ab, ob der Remotedesktopverbindung -Client (RDC) Windows Server 2008 R2 RemoteApp-Funktionalität unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Eigenschaftswert

Ruft ab, ob der Remotedesktopverbindung -Client (RDC) remoteApp-Funktionen unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell ist als d012ae6d-c19a-4bfe-b367-201f8911f134 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





