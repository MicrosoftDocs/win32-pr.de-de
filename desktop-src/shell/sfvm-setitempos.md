---
description: Legt die Position eines Elements in der shellansicht fest. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_SETITEMPOS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218382"
---
# <a name="sfvm_setitempos-message"></a>Sfvm- \_ Nachricht

Legt die Position eines Elements in der shellansicht fest. Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SIP* \[ in\]
</dt> <dd>

Ein Zeiger auf eine SFV-Struktur von "- [**\_ titempos**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) ".

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




