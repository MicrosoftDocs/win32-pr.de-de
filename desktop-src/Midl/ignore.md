---
title: ignore-Attribut
description: Das Attribut \ignore\ gibt an, dass ein zeiger, der in einer Struktur oder Union enthalten ist, und das vom Zeiger angegebene Objekt nicht übertragen wird. Das Attribut \ignore\ ist auf Zeigermitglieder von Strukturen oder Unions beschränkt.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- IGNORE-Attribut MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6b7a1e70804bc3c9c277f3d46ac6a8ad20fc0f98b370f93fe9fd09b0b1bb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013858"
---
# <a name="ignore-attribute"></a>ignore-Attribut

Das **\[ \] ignore-Attribut** gibt an, dass ein zeiger, der in einer Struktur oder Union enthalten ist, und das durch den Zeiger angegebene Objekt nicht übertragen wird. Das **\[ ignore-Attribut \]** ist auf Zeigermitglieder von Strukturen oder Unions beschränkt.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pointer-member-type* 
</dt> <dd>

Gibt den Typ des Zeiger-Members der Struktur oder Union an.

</dd> <dt>

*Zeigername* 
</dt> <dd>

Gibt den Namen des Zeigermitglieds an, das während des Marshallings ignoriert werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Wert eines Strukturmitglieds mit dem **\[ \] ignore-Attribut** ist am Ziel nicht definiert. Ein **\[** [](in.md) **\]** in-Parameter ist auf dem Remotecomputer nicht definiert. Ein **\[** [](out-idl.md) **\]** out-Parameter ist auf dem lokalen Computer nicht definiert.

Mit **\[ dem \] Ignore-Attribut** können Sie die Übertragung von Daten verhindern. Dies ist in Situationen nützlich, z. B. in einer doppelt verknüpften Liste. Das folgende Beispiel enthält eine doppelt verknüpfte Liste, die das Datenaliasing einfing:

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

Aliasing tritt im vorherigen Beispiel auf, da der gleiche Speicherbereich über zwei verschiedene Zeiger in der Funktion **p** und **p->** der nächsten >verfügbar ist.

Beachten Sie, **\[ dass ignore \]** nicht als Typattribut verwendet werden kann.

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

[Array- Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**In**](in.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> </dl>

 

 