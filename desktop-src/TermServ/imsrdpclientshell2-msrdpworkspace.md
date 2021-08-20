---
title: IMsRdpClientShell2 MsRdpWorkspace-Eigenschaft
description: Ruft einen Zeiger auf die IMsRdpWorkspace-Schnittstelle ab, die zum Verwalten RemoteApp- und Desktopverbindung Anmeldeinformationen und Verbindungen verwendet wird.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- MsRdpWorkspace-Eigenschaft Remotedesktopdienste
- MsRdpWorkspace-Eigenschaft Remotedesktopdienste , IMsRdpClientShell2-Schnittstelle
- IMsRdpClientShell2-Schnittstelle Remotedesktopdienste , MsRdpWorkspace-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6470f51ccae2efb6dc3d44a7b0a2a0310ad4230861d7d86262f34fd312fcfc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854434"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>IMsRdpClientShell2::MsRdpWorkspace-Eigenschaft

Ruft einen Zeiger auf die [**IMsRdpWorkspace-Schnittstelle**](imsrdpworkspace.md) ab, die zum Verwalten RemoteApp- und Desktopverbindung Anmeldeinformationen und Verbindungen verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Adresse eines Zeigers auf die [**IMsRdpWorkspace-Schnittstelle.**](imsrdpworkspace.md)

## <a name="remarks"></a>Hinweise

Die [**IMsRdpWorkspace-Schnittstelle**](imsrdpworkspace.md) wird nicht als benutzerdefinierte Schnittstelle verfügbar gemacht. Der Zugriff ist nur über [IDispatch-Methoden](/windows/desktop/com/exposing-methods-through-idispatch) möglich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

