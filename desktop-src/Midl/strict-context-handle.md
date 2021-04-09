---
title: strict_context_handle-Attribut
description: Das Attribut \ Strict \_ context \_ handle \ ACF legt Einschränkungen für Kontext Handles fest.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948615"
---
# <a name="strict_context_handle-attribute"></a>Strict- \_ Kontext \_ handle-Attribut

Das **\[ strikte \_ Kontext \_ handle \]** -ACF-Attribut legt Einschränkungen für Kontext Handles fest.

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

*Interface-Attribute-List* 
</dt> <dd>

Andere ACF-Attribute, die auf die gesamte Schnittstelle angewendet werden. Gültige Attribute sind [**Auto \_ handle**](auto-handle.md), [**implizites \_**](implicit-handle.md)handle, [**explizites \_ handle**](explicit-handle.md)und [**Optimierung**](optimize.md), [**Code**](code.md)oder [**NoCode**](nocode.md). Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Interface-Definition-Anweisungen* 
</dt> <dd>

Eine oder mehrere-Mittell-Anweisungen, die die Elemente der- [**Schnittstelle**](interface.md)definieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Normalerweise wird das Handle, wenn ein-Befehl an eine Schnittstellen Methode ein Kontext Handle generiert, für jede andere Schnittstelle frei verfügbar. Wenn Sie das **\[ strikte \_ Kontext \_ handle \]** -Attribut verwenden, gewährleisten Sie, dass die Methoden in dieser Schnittstelle nur Kontext Handles akzeptieren, die von einer Methode von derselben Schnittstelle erstellt wurden. Schnittstellen, die ohne **\[ Strict- \_ Kontext \_ handle \]** kompiliert werden, können keine Kontext Handles akzeptieren, die für Schnittstellen **\[ \_ \_ \]** erstellt werden

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Ordnung**](code.md)
</dt> <dt>

[Kontext Handles](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**Kontext \_ handle- \_ Serialisierung**](context-handle-serialize.md)
</dt> <dt>

[**Kontext \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**explizites \_ handle**](explicit-handle.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**optimiert**](optimize.md)
</dt> <dt>

[Typ \_ Strict- \_ Kontext \_ handle](type-strict-context-handle.md)
</dt> </dl>

 

 