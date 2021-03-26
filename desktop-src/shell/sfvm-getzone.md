---
description: 'Ermöglicht dem Rückruf Objekt, Internet Zonen Informationen bereitzustellen. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: SFVM_GETZONE Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530182"
---
# <a name="sfvm_getzone-message"></a>Sfvm- \_ getzone-Nachricht

\[Diese Benachrichtigung wird durch Windows XP Service Pack 2 (SP2) und Windows Server 2003 unterstützt. Sie wird möglicherweise in nachfolgenden Versionen von Windows nicht unterstützt.\]

Ermöglicht dem Rückruf Objekt, Internet Zonen Informationen bereitzustellen. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zone* \[ vorgenommen\]
</dt> <dd>

Einer der folgenden Werte, der die Internet Zone angibt. Diese Werte bilden die [**urlzone**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) -Enumeration, die in Urlmon. h definiert ist.

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**lokaler urlzone- \_ \_ Computer**


</dt> <dd>

Die für den Inhalt verwendete Zone, die sich bereits auf dem lokalen Computer des Benutzers befindet. Diese Zone wird nicht von der Benutzeroberfläche verfügbar gemacht.

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**urlzone- \_ Intranet**


</dt> <dd>

Zone für Inhalte, die in einem Intranet gefunden werden.

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**urlzone \_ vertrauenswürdig**


</dt> <dd>

Zone, die für vertrauenswürdige Websites im Internet verwendet wird.

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**urlzone- \_ Internet**


</dt> <dd>

Zone, die für die meisten Inhalte im Internet verwendet wird.

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**urlzone \_ nicht vertrauenswürdig**


</dt> <dd>

Zone, die für nicht vertrauenswürdige Websites verwendet wird.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
