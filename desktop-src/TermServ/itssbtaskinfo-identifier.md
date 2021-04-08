---
title: Itssbtaskinfo-Bezeichnereigenschaft
description: Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Bezeichnereigenschaft Remotedesktopdienste
- Bezeichnereigenschaft Remotedesktopdienste, itssbtaskinfo-Schnittstelle
- Itssbtaskinfo-Schnittstelle Remotedesktopdienste, Bezeichnereigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743640"
---
# <a name="itssbtaskinfoidentifier-property"></a>Itssbtaskinfo:: Identifier-Eigenschaft

Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **BSTR** -Wert, der die GUID empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbtaskinfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





