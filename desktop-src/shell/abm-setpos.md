---
description: Legt die Größe und Bildschirmposition einer appbar fest.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: ABM_SETPOS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525427"
---
# <a name="abm_setpos-message"></a>ABM- \_ SetPos-Nachricht

Legt die Größe und Bildschirmposition einer appbar fest. Die Meldung gibt eine Bildschirm Kante und das umgebende Rechteck für die appbar an. Das System kann das umgebende Rechteck so anpassen, dass die APP-Leiste die Windows-Taskleiste oder andere appbars nicht beeinträchtigt.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur. Der **uedge** -Member gibt einen Bildschirmrand an, und das **RC** -Element enthält das umgebende Rechteck. Wenn die [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) -Funktion zurückgegeben wird, enthält **RC** das genehmigte umschließende Rechteck. Sie müssen die Member **CBSIZE**, **HWND**, **uedge** und **RC** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung bewirkt, dass das System die [**ABN \_**](abn-poschanged.md) -Benachrichtigungs Meldung an alle appbars sendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




