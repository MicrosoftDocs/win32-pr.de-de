---
title: Menuheader-Struktur
description: Enthält Versionsinformationen für die Menü Ressource. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menuheader-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338321"
---
# <a name="menuheader-structure"></a>Menuheader-Struktur

Enthält Versionsinformationen für die Menü Ressource. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**wversion**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Versionsnummer der Menüvorlage. Dieser Member muss gleich NULL sein, um anzugeben, dass es sich um ein [**RT- \_ Menü**](/windows/desktop/menurc/resource-types) handelt, das mit einer Standardmenü Vorlage erstellt wurde.

</dd> <dt>

**cbheadersize**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Größe des Menü Vorlagen Headers. Dieser Wert ist 0 (null) für Menüs, die Sie mit einer Standardmenü Vorlage erstellen.

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

[**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md)
</dt> <dt>

[**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md)
</dt> <dt>

[**Menuitemtemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[**Menuitemtemplateheader**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[**Normalmenuitem**](normalmenuitem.md)
</dt> <dt>

[**Popupmenuitem**](popupmenuitem.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

