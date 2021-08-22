---
title: strict_context_handle-Attribut
description: Das \strict \_ context \_ handle\ACF-Attribut legt Einschränkungen für Kontexthandles fest.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle-Attribut MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db19c74efa323fa7e3abc4bfd17c14a471cbb9c81414ae78064f84bfc19fa7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013578"
---
# <a name="strict_context_handle-attribute"></a>\_ \_ Strict-Kontexthandleat

Das **\[ \_ Strict-Kontexthandle \_ \]** ACF-Attribut legt Einschränkungen für Kontexthandles fest.

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Andere ACF-Attribute, die für die gesamte Schnittstelle gelten. Zu den gültigen Attributen gehören [**das automatische \_ Handle,**](auto-handle.md) [**das implizite \_ Handle,**](implicit-handle.md)das [**explizite \_ Handle**](explicit-handle.md)und [**das Optimieren**](optimize.md)von , [**Code**](code.md)oder [**Nocode**](nocode.md). Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*interface-definition-statements* 
</dt> <dd>

Eine oder mehrere MIDL-Anweisungen, die die Elemente der [**Schnittstelle**](interface.md)definieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ein Aufruf einer Schnittstellenmethode ein Kontexthandle generiert, ist dieses Handle normalerweise für jede andere Schnittstelle frei verfügbar. Wenn Sie das **\[ \_ strict-Kontexthandleattribut \_ \]** verwenden, garantieren Sie, dass die Methoden in dieser Schnittstelle nur Kontexthandles akzeptieren, die von einer Methode aus derselben Schnittstelle erstellt wurden. Schnittstellen, die ohne **\[ striktes \_ \_ \] Kontexthandle** kompiliert wurden, können keine Kontexthandles akzeptieren, die auf Schnittstellen erstellt wurden, die mit **\[ einem \_ strict-Kontexthandle \_ \]** kompiliert wurden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Code**](code.md)
</dt> <dt>

[Kontexthandles](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**\_Kontexthandle \_ serialisieren**](context-handle-serialize.md)
</dt> <dt>

[**context \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**Explizites \_ Handle**](explicit-handle.md)
</dt> <dt>

[**Implizites \_ Handle**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Optimieren**](optimize.md)
</dt> <dt>

[Type \_ \_ Strict-Kontexthandle \_](type-strict-context-handle.md)
</dt> </dl>

 

 