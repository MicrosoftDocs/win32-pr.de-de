---
title: Itssbsession username (Eigenschaft)
description: Ruft den Benutzernamen für diese Sitzung ab.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Username-Eigenschaft Remotedesktopdienste
- Username-Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, UserName-Eigenschaft
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
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344104"
---
# <a name="itssbsessionusername-property"></a>Itssbsession:: username (Eigenschaft)

Ruft den Benutzernamen für diese Sitzung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR** -Variable, die den Benutzernamen für diese Sitzung empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbsession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





