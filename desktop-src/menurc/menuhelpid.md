---
title: Menuhelpid-Struktur
description: Enthält die abschließenden Daten, die in die RT- \_ Menü Ressource für ein Menü oder ein Untermenü geschrieben werden, wenn der ResInfo-Member der popupmenuitem-Struktur auf MFR-Popup festgelegt ist \_ .
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menuhelpid-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344268"
---
# <a name="menuhelpid-structure"></a>Menuhelpid-Struktur

Enthält die abschließenden Daten, die in die [**RT- \_ Menü**](/windows/desktop/menurc/resource-types) Ressource für ein Menü oder ein Untermenü geschrieben werden, wenn der **ResInfo** -Member der [**popupmenuitem**](popupmenuitem.md) -Struktur auf **MFR- \_ Popup** festgelegt ist. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>Member

<dl> <dt>

**HelpID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Bezeichner, der zum Identifizieren des Menüs während der [**WM- \_ Hilfe**](/windows/desktop/shell/wm-help) Verarbeitung verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Menuheader**](menuheader.md)
</dt> <dt>

[**Popupmenuitem**](popupmenuitem.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

