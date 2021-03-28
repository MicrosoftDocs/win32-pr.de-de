---
description: 'Benachrichtigt das Rückruf Objekt der Container Site. Dieser Wert wird nur verwendet, wenn "IObjectWithSite:: SetSite" nicht unterstützt wird und "shkreateshellfolderviewex" verwendet wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: SFVM_SETISFV Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980880"
---
# <a name="sfvm_setisfv-message"></a>Sfvm- \_ Nachricht "abtisfv"

\[Diese Benachrichtigung wird durch Windows XP Service Pack 2 (SP2) und Windows Server 2003 unterstützt. Sie wird möglicherweise in nachfolgenden Versionen von Windows nicht unterstützt.\]

Benachrichtigt das Rückruf Objekt der Container Site. Dieser Wert wird nur verwendet, wenn " [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) " nicht unterstützt wird und " [**shkreateshellfolderviewex**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) " verwendet wird. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Website* \[ in\]
</dt> <dd>

Ein Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle der Container Site.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
