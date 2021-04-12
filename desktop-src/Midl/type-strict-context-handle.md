---
title: type_strict_context_handle-Attribut
description: Verwenden Sie den "\ Type \_ Strict \_ context \_ handle \" in einer ACF-Datei, um Einschränkungen für Kontext Handles festzulegen.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472789"
---
# <a name="type_strict_context_handle-attribute"></a>Typ \_ Strict- \_ Kontext \_ handle-Attribut

Verwenden Sie den **\[ Typ \_ Strict- \_ Kontext \_ handle \]** in einer ACF-Datei, um Einschränkungen für Kontext Handles festzulegen.

``` syntax
[ 
    type_strict_context_handle 
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

Um dieses Attribut zu verwenden, muss das-Target-Flag beim Ausführen von midl.exe auf nt60 (oder höher) festgelegt werden.

\[\_der Typ Strict- \_ Kontext \_ handle \] ist eine Funktions Übermenge eines \[ strengen \_ Kontext \_ Handles \] . Im \[ Strict- \_ Kontext \_ handle \] ist die Typ-ID des Handles immer 0. im \[ Typ \_ Strict- \_ Kontext Handle wird \_ \] eine eindeutige Typ-ID vom Mittelwert Compiler zugewiesen.

Es wird empfohlen, das \[ \_ typstrikte \_ Kontext \_ handle \] anstelle eines \[ strengen \_ Kontext \_ Handles \] zu verwenden. Kontext Handles sind nicht standardmäßig mit einem bestimmten Typ verknüpft. Wenn im gleichen Prozess mehrere Typen von Kontext Handles verwendet werden, ist es möglich, dass ein böswilliger Client ein Kontext Handle anstelle eines anderen übergibt, um unerwünschte Ergebnisse zu erzielen. Durch die Verwendung \[ des \_ Typs \_ Strict \_ -Kontext Handle \] können Anwendungen die Konsistenz des Kontext Handles erzwingen und jede nicht übereinstimmende Kontext Handle-Typverwendung verhindern.

Ein mit dem Typ Strict-Kontext Handle attributiertes Kontext Handle \[ \_ \_ \_ \] kann nicht auch mit einem \[ Strict-Kontext Handle attributiert werden \_ \_ \] .

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

[Strict- \_ Kontext \_ handle](strict-context-handle.md)
</dt> </dl>

 

 