---
title: MENUEX_TEMPLATE_ITEM Struktur
description: Definiert ein Menü Element in einer erweiterten Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518698"
---
# <a name="menuex_template_item-structure"></a>Menuex- \_ Vorlagen \_ Elementstruktur

Definiert ein Menü Element in einer erweiterten Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

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

Der Typ des Menü Elements. Dieser Member kann eine Kombination der Werte vom Typ (beginnend mit MFT) sein, die mit der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelistet sind.

</dd> <dt>

**dwstate**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Zustand des Menü Elements. Dieser Member kann eine Kombination aus den in der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelisteten Status Werten (beginnend mit MFS) sein.

</dd> <dt>

**uId**
</dt> <dd>

Typ: **uint**

</dd> <dd>

Der Bezeichner des Menü Elements. Dies ist ein von der Anwendung definierter Wert, der das Menü Element bezeichnet. In einer erweiterten Menü Ressource können Elemente, die Dropdown Menüs oder Untermenüs sowie Befehls Elemente öffnen, über Bezeichner verfügen.

</dd> <dt>

**wFlags**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Gibt an, ob es sich beim Menü Element um das letzte Element in der Menüleiste, im Dropdown Menü, im Untermenü oder im Kontextmenü handelt und ob es sich um ein Element handelt, das ein Dropdown Menü oder ein Untermenü öffnet. Dieser Member kann NULL oder mehr dieser Werte sein. Bei 32-Bit-Anwendungen ist dieser Member ein Wort. bei 16-Bit-Anwendungen ist es ein Byte.

<dt>

0x80
</dt> <dd>

Die Struktur definiert das letzte Menü Element in der Menüleiste, dem Dropdown Menü, dem Untermenü oder dem Kontextmenü.

</dd> <dt>

0x01
</dt> <dd>

Die-Struktur definiert ein Element, das ein Dropdown Menü oder ein Untermenü öffnet. Nachfolgende Strukturen definieren Menü Elemente im entsprechenden Dropdown Menü oder Untermenü.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Der Text des Menü Elements. Dieser Member ist eine auf NULL endenden Unicode-Zeichenfolge, die an einer Wort Grenze ausgerichtet ist. Die Größe der Menü Element Definition variiert abhängig von der Länge dieser Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine erweiterte Menüvorlage besteht aus einer [**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md) Struktur, gefolgt von einer oder mehreren zusammenhängenden **menuex- \_ Vorlagen \_ Element** Strukturen. Die **menuex- \_ Vorlagen \_ Element** Strukturen, die eine Variable Länge haben, werden an den **DWORD** -Grenzen ausgerichtet. Verwenden Sie die [**loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) -Funktion, um ein Menü aus einer erweiterten Menüvorlage im Arbeitsspeicher zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md)
</dt> <dt>

[**Menuiteminfo zuordnet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

 





