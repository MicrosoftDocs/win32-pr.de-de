---
title: IMsRdpClientShell2 securedsettingsenabled (Eigenschaft)
description: Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClientShell2-Schnittstelle
- IMsRdpClientShell2 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
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
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340370"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>IMsRdpClientShell2:: securedsettingsenabled (Eigenschaft)

Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen booleschen Wert, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.

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

 

 





