---
title: Imsrdpclientshell isremoteprogramclientinstallierte (Eigenschaft)
description: Ruft ab, ob der Remotedesktopverbindung-Client (RDC) Windows Server 2008 R2 RemoteApp-Funktionalität unterstützt.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Isremoteprogramclientinstallierte-Eigenschaft Remotedesktopdienste
- Isremoteprogramclientinstallierte-Eigenschaft Remotedesktopdienste, imsrdpclientshell-Schnittstelle
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, isremoteprogramclientinstallierte-Eigenschaft
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
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103270"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>Imsrdpclientshell:: isremoteprogramclientinstallierte-Eigenschaft

Ruft ab, ob der Remotedesktopverbindung-Client (RDC) Windows Server 2008 R2 RemoteApp-Funktionalität unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Eigenschaftswert

Ruft ab, ob der Remotedesktopverbindung-Client (RDC) die RemoteApp-Funktionalität unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientshell**](imsrdpclientshell.md)
</dt> </dl>

 

 





