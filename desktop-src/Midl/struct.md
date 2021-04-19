---
title: struct-Attribut
description: Das struct-Schlüsselwort wird in einem strukturtypspezifizierer verwendet.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- Struktur Attribut-Mittel l
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106342128"
---
# <a name="struct-attribute"></a>struct-Attribut

Das **struct** -Schlüsselwort wird in einem strukturtypspezifizierer verwendet.

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*struct-Tag* 
</dt> <dd>

Gibt ein optionales Tag für die Struktur an.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Feld Attribute an, die für den Strukturmember gelten. Gültige Feld Attribute sind " **\[** [**First \_ is**](first-is.md)" **\]** , " **\[** [**Last \_ is**](last-is.md)" **\]** , " **\[** [**length \_ is**](length-is.md)", " **\]** **\[** [**Max \_ is**](max-is.md)" und "size", " **\]** **\[** [**\_**](size-is.md) **\]** Usage Attribute **\[** [**String**](string.md) " **\]** und " **\[** [**Ignore**](ignore.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](switch-type.md) **\]** " Trennen Sie mehrere Feld Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), eine **Struktur**, eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren. (Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der IDL-strukturtypspezifizierer ( **struct**) unterscheidet sich in folgenden Punkten vom standardmäßigen C-Typspezifizierer:

-   Jeder Strukturmember kann optionalen Feld Attributen zugeordnet werden, die die Merkmale dieses Strukturmembers für den Zweck eines Remote Prozedur Aufrufes beschreiben.
-   Bitfelder und Funktionsdeklaratoren sind in Strukturen, die in Remote Prozedur aufrufen verwendet werden, nicht zulässig. Diese standardmäßigen C-deklaratorkonstrukte können nur verwendet werden, wenn die Struktur nicht im Netzwerk übertragen wird.

Die Form von Strukturen muss plattformübergreifend identisch sein, um die Konnektivität zu gewährleisten.

## <a name="examples"></a>Beispiele

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**/c \_ ext**](-c-ext.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[**der erste \_ ist**](first-is.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**Letzter \_ ist**](last-is.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**\_Switchtyp**](switch-type.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 