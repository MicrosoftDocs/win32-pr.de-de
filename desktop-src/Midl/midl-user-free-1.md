---
title: midl_user_free-Attribut
description: Die Funktion "mittlere \_ Benutzer \_ Kosten" wird von Client-und Server Anwendungen bereitgestellt, um die Zuordnung dynamisch zugeordneten Speichers aufzuheben.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free Attribut-Mittel l
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314901"
---
# <a name="midl_user_free-attribute"></a>\_ \_ Kostenloses Attribut für mittlere Benutzer

Die Funktion " **mittlere \_ Benutzer \_ Kosten** " wird von Client-und Server Anwendungen bereitgestellt, um die Zuordnung dynamisch zugeordneten Speichers aufzuheben.

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*cker* 
</dt> <dd>

Ein Zeiger auf den Speicherblock, der freigegeben werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sowohl die Client Anwendung als auch die Serveranwendung müssen die Free-Funktion der **mittleren \_ \_ Benutzer** implementieren, es sei denn, Sie kompilieren ihn im OSF-Kompatibilitätsmodus ([**/OSF**](-osf.md)). Die **mittlere \_ Benutzer \_ freie** Funktion muss in der Lage sein, den gesamten Speicher freizugeben, der von der [**\_ Benutzer \_ Zuordnung**](/windows/desktop/Rpc/the-midl-user-allocate-function)für den Benutzer zugeordnet wird.

Anwendungen und stufstufs wenden den **\_ Benutzer \_ kostenlos** an, wenn Sie mit Objekten arbeiten, auf die durch Zeiger verwiesen wird

-   Die Serveranwendung sollte den **\_ Benutzer freien Benutzer \_ Free** anrufen, um Speicher freizugeben, der von der application\\z. b. beim Löschen eines bestimmten Knotens zugeordnet wird.
-   Der Serverstub Ruft den **\_ Benutzer \_ kostenlos** auf, um Arbeitsspeicher auf dem Server freizugeben, nachdem alle **\[** [](out-idl.md) **\]** Argumente, **\[** [**in**](in.md), **out \]** -Argumente und der Rückgabewert gemarshallert wurden.

## <a name="examples"></a>Beispiele


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**mittlere Benutzer Zuordnungen \_ \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 