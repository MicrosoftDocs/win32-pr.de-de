---
description: Fordert eine Größe und Bildschirmposition für eine appbar an.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: ABM_QUERYPOS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342868"
---
# <a name="abm_querypos-message"></a>ABM- \_ querypos-Nachricht

Fordert eine Größe und Bildschirmposition für eine appbar an. Wenn die Anforderung erfolgt, schlägt die Meldung einen Bildschirmrand und ein Begrenzungs Rechteck für die appbar vor. Das System passt das umgebende Rechteck so an, dass die APP-Leiste die Windows-Taskleiste oder andere appbars nicht beeinträchtigt.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur. Der **uedge** -Member gibt einen Bildschirmrand an, und das **RC** -Element enthält das vorgeschlagene umgebende Rechteck. Wenn die [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) -Funktion zurückgegeben wird, enthält **RC** das genehmigte umschließende Rechteck. Sie müssen die Member **CBSIZE**, **HWND**, **uedge** und **RC** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Eine appbar sollte diese Nachricht vor dem Senden der [**ABM- \_ SetPos**](abm-setpos.md) -Nachricht senden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




