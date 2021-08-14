---
title: MENUEX_TEMPLATE_ITEM-Struktur
description: Definiert ein Menüelement in einer erweiterten Menüvorlage. Diese Strukturdefinition wird nur zur Erklärung verwendet. sie ist in einer Standardheaderdatei nicht vorhanden.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6352c7ce596a59d69b21f1ba424ac50b471e13cd97320f0df184bce2e1abd295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733905"
---
# <a name="menuex_template_item-structure"></a>MENUEX \_ TEMPLATE \_ ITEM-Struktur

Definiert ein Menüelement in einer erweiterten Menüvorlage. Diese Strukturdefinition wird nur zur Erklärung verwendet. sie ist in einer Standardheaderdatei nicht vorhanden.

## <a name="syntax"></a>Syntax

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a>Member

<dl> <dt>

**dwType**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Menüelementtyp. Dieser Member kann eine Kombination der Typwerte (beginnend mit MFT) sein, die mit der [**MENUITEMINFO-Struktur aufgelistet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) sind.

</dd> <dt>

**dwState**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Menüelementzustand. Dieser Member kann eine Kombination der Statuswerte (beginnend mit MFS) sein, die mit der [**MENUITEMINFO-Struktur aufgelistet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) sind.

</dd> <dt>

**Uid**
</dt> <dd>

Typ: **UINT**

</dd> <dd>

Der Menüelementbezeichner. Dies ist ein anwendungsdefinierter Wert, der das Menüelement identifiziert. In einer erweiterten Menüressource können Elemente, die Dropdownmenüs oder Untermenüs öffnen, sowie Befehlselemente Bezeichner enthalten.

</dd> <dt>

**wFlags**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Gibt an, ob das Menüelement das letzte Element in der Menüleiste, im Dropdownmenü, im Untermenü oder im Kontextmenü ist und ob es sich um ein Element handelt, das ein Dropdownmenü oder Untermenü öffnet. Dieser Member kann null oder mehr dieser Werte sein. Bei 32-Bit-Anwendungen ist dieser Member ein Wort. Für 16-Bit-Anwendungen ist es ein Byte.

<dt>

0x80
</dt> <dd>

Die -Struktur definiert das letzte Menüelement in der Menüleiste, im Dropdownmenü, im Untermenü oder im Kontextmenü.

</dd> <dt>

0x01
</dt> <dd>

Die -Struktur definiert ein Element, das ein Dropdownmenü oder Untermenü öffnet. Nachfolgende Strukturen definieren Menüelemente im entsprechenden Dropdownmenü oder Untermenü.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Der Text des Menüelements. Dieser Member ist eine auf NULL terminte Unicode-Zeichenfolge, die an einer Wortgrenze ausgerichtet ist. Die Größe der Menüelementdefinition variiert je nach Länge dieser Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine erweiterte Menüvorlage besteht aus einer [**MENUEX \_ TEMPLATE \_ HEADER-Struktur,**](menuex-template-header.md) gefolgt von einer oder mehreren zusammenhängenden **MENUEX TEMPLATE \_ \_ ITEM-Strukturen.** Die **MENUEX \_ TEMPLATE \_ ITEM-Strukturen,** die eine variable Länge haben, werden an **DWORD-Grenzen** ausgerichtet. Um ein Menü aus einer erweiterten Menüvorlage im Arbeitsspeicher zu erstellen, verwenden Sie die [**LoadMenuIndirect-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

 





