---
title: ITsSbSession Username-Eigenschaft
description: Ruft den Benutzernamen für diese Sitzung ab.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Username-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste , ITsSbSession-Schnittstelle
- ITsSbSession-Schnittstelle Remotedesktopdienste , Username-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d42c06d700cb95df5635f902876c242b164a6fd12415848cc11539cb30edd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351200"
---
# <a name="itssbsessionusername-property"></a>ITsSbSession::Username-Eigenschaft

Ruft den Benutzernamen für diese Sitzung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR-Variable,** die den Benutzernamen für diese Sitzung empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





