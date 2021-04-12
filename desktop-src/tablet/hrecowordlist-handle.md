---
description: Ein hrecowordlist-Handle wird verwendet, um eine Wort Liste zu verwalten, die Sie an einen Erkennungs Kontext anfügen. Sie verwenden eine Wort Liste, um die Erkennungsergebnisse zu verbessern.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Hrecowordlist-handle ("recapis. h")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526573"
---
# <a name="hrecowordlist-handle"></a>Hrecowordlist-handle

Ein **hrecowordlist** -Handle wird verwendet, um eine Wort Liste zu verwalten, die Sie an einen Erkennungs Kontext anfügen. Sie verwenden eine Wort Liste, um die Erkennungsergebnisse zu verbessern.


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>Bemerkungen

Die folgende Funktion verwendet eine **hrecowordlist**.



| Funktion                                         | BESCHREIBUNG                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**Addwordstowordlist**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | Fügt der Word-Liste mindestens ein Wort hinzu.<br/> |
| [**Destroywordlist**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | Zerstört die aktuelle Wort Liste.<br/>          |
| [**Makewordlist**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | Erstellt eine Wort Liste.<br/>                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>"Recapis. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Setwordlist-Funktion**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




