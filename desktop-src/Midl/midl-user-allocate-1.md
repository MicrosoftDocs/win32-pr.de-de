---
title: midl_user_allocate-Attribut
description: Die \_ \_ Midl-Benutzer-Zuordnungsfunktion ist eine Funktion, die Client- und Serveranwendungen bereitstellen, um Arbeitsspeicher zu reservieren.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate MIDL-Attribut
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16729e0a0a422c8ed2d8a8f323b563cb6a268fcb041e6a9d2ba13a9c9b847d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806658"
---
# <a name="midl_user_allocate-attribute"></a>midl \_ user \_ allocate-Attribut

Die **\_ Midl-Benutzer-Zuordnungsfunktion \_** ist eine Funktion, die Client- und Serveranwendungen bereitstellen, um Arbeitsspeicher zu reservieren.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*cBytes* 
</dt> <dd>

Gibt die Anzahl der zu reservierenden Bytes an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sowohl Clientanwendungen als auch Serveranwendungen müssen die Midl-Benutzer-Zuordnungsfunktion implementieren, es sei denn, Sie kompilieren im OSF-Kompatibilitätsmodus [**(/osf).**](-osf.md) **\_ \_** Anwendungen und generierte Stubs rufen **midl \_ user allocate \_ auf,** wenn es um Objekte geht, auf die von Zeigern verwiesen wird:

-   Die Serveranwendung sollte **midl \_ user \_ allocate** aufrufen, um Arbeitsspeicher für die Anwendung zu reservieren, z.B. beim Erstellen eines neuen Knotens.
-   Der Serverstub ruft **midl \_ user allocate \_ auf,** wenn die Zuordnung von point-at-Daten in den Serveradressenbereich entmardt wird.
-   Der Clientstub ruft **midl \_ user allocate \_ auf,** wenn daten vom Server, auf den von einem Out-Zeiger verwiesen wird, nicht imShaling [**gespeichert**](out-idl.md) werden. Beachten Sie, dass der Clientstub für **\[** [**in**](in.md), out **\]** **\[ \]** und eindeutige Zeiger nur dann midl user allocate **\[** [](unique.md) **\]** **\[ \]** aufruft, **\_ \_**  wenn der eindeutige Zeigerwert bei der Eingabe NULL war und sich während des Aufrufs in einen **Nicht-NULL-Wert** ändert. Wenn der **\[ \] eindeutige** Zeiger bei der Eingabe nicht **NULL** war, schreibt der Clientstub die zugeordneten Daten in den vorhandenen Arbeitsspeicher.

Wenn **bei der \_ Midl-Benutzerbeteilung \_** kein Speicher reserviert werden kann, muss ein **NULL-Zeiger** zurückgegeben werden.

Es wird empfohlen, dass **midl \_ user \_ allocate** einen Zeiger zurückgibt, der 8 Bytes ausgerichtet ist.

## <a name="examples"></a>Beispiele


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Array- Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**In**](in.md)
</dt> <dt>

[**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> </dl>

 

 