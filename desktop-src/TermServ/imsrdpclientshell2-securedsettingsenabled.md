---
title: IMsRdpClientShell2 SecuredSettingsEnabled-Eigenschaft
description: Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer URL-Sicherheitszone befindet.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- SecuredSettingsEnabled-Eigenschaft Remotedesktopdienste
- SecuredSettingsEnabled-Eigenschaft Remotedesktopdienste , IMsRdpClientShell2-Schnittstelle
- IMsRdpClientShell2-Schnittstelle Remotedesktopdienste , SecuredSettingsEnabled-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d418df76de38313d681f9f01a4dea33ba0803ad67e42d92d90d2ba5a354a8eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870880"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>IMsRdpClientShell2::SecuredSettingsEnabled-Eigenschaft

Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer URL-Sicherheitszone befindet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen booleschen Wert, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer URL-Sicherheitszone befindet.

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

 

 





