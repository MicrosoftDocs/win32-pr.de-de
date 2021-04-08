---
title: Attribut ignorieren
description: Das Attribut \ Ignore \ gibt an, dass ein in einer Struktur oder Union enthaltener Zeiger und das vom Zeiger festgestellte Objekt nicht übertragen werden. Das Attribut \ Ignore \ ist auf Zeiger Elemente von Strukturen oder Unions beschränkt.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- Attribut-Mittel l ignorieren
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858189"
---
# <a name="ignore-attribute"></a>Attribut ignorieren

Das **\[ Ignore \]** -Attribut gibt an, dass ein in einer Struktur oder Union enthaltener Zeiger und das vom Zeiger festgestellte Objekt nicht übertragen werden. Das **\[ Ignore \]** -Attribut ist auf Zeiger Elemente von Strukturen oder Unions beschränkt.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Pointer-Member-Type* 
</dt> <dd>

Gibt den Typ des Zeiger Elements der Struktur oder Union an.

</dd> <dt>

*Zeiger Name* 
</dt> <dd>

Gibt den Namen des Zeiger Elements an, das beim Marshalling ignoriert werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Wert eines Strukturmembers mit dem **\[ Ignore \]** -Attribut ist am Ziel nicht definiert. Ein **\[** [**in**](in.md) - **\]** Parameter ist nicht auf dem Remote Computer definiert. Ein **\[** [**out**](out-idl.md) - **\]** Parameter ist nicht auf dem lokalen Computer definiert.

Mit dem Attribut " **\[ Ignore \]** " können Sie die Übertragung von Daten verhindern. Dies ist in Situationen hilfreich, z. b. in einer doppelt verknüpften Liste. Das folgende Beispiel enthält eine doppelt verknüpfte Liste, die das datenaliasing einführt:

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

Aliasing tritt im vorangehenden Beispiel auf, weil derselbe Speicherbereich von zwei verschiedenen Zeigern in der Funktion **p** und **p->Next->Previous** verfügbar ist.

Beachten Sie, dass **\[ Ignore \]** nicht als Type-Attribut verwendet werden kann.

## <a name="examples"></a>Beispiele

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 