---
title: MENUHELPID-Struktur
description: Enthält die endgültigen Daten, die in die RT MENU-Ressource für ein Menü oder Untermenü geschrieben werden, wenn das resInfo-Element der \_ POPUPMENUITEM-Struktur auf POPUP \_ POPUP festgelegt ist.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- MENUHELPID-Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4831074d5e7b663210f880bf6684cbc6484ad3487a0c6c9e5be308aebc66291a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825950"
---
# <a name="menuhelpid-structure"></a>MENUHELPID-Struktur

Enthält die endgültigen Daten, die in die [**RT \_ MENU-Ressource**](/windows/desktop/menurc/resource-types) für ein Menü oder Untermenü geschrieben werden, wenn das **resInfo-Element** der [**POPUPMENUITEM-Struktur**](popupmenuitem.md) auf **POPUP POPUP festgelegt \_ ist.** Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>Member

<dl> <dt>

**helpID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Bezeichner, der verwendet wird, um das Menü während der [**WM \_ HELP-Verarbeitung zu**](/windows/desktop/shell/wm-help) identifizieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

