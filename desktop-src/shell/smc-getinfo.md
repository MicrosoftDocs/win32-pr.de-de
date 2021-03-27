---
description: Fordert Informationen über ein reguläres Menü Element an.
title: SMC_GETINFO Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f60c1581ae7c4585de48eea943cc23b4d87fa4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994839"
---
# <a name="smc_getinfo-message"></a>SMC- \_ GetInfo-Nachricht

Fordert Informationen über ein reguläres Menü Element an.


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psminfo* 
</dt> <dd>

Ein Zeiger auf eine [**sminfo**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) -Struktur. Füllen Sie die Struktur mit den entsprechenden Informationen aus, und geben Sie \_ OK zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "S OK" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




