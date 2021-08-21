---
title: optimize-Attribut
description: Das Attribut \optimize\ ACF wird verwendet, um den Grad der Gradierung für das Marshalling von Daten zu optimieren.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- OPTIMIZE-Attribut MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7703a3539ff16c7f2dc78d51c62cfe05612dcb6e935bb5c5701f9a7b59a9f1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869570"
---
# <a name="optimize-attribute"></a>optimize-Attribut

Das **\[ Optimize \]** ACF-Attribut wird verwendet, um den Grad der Gradierung für das Marshallen von Daten zu optimieren.

> [!Note]  
> Dieses Schlüsselwort wird ersetzt und sollte nicht verwendet werden. Aktuelle MIDL-Kompilierungen sollten [**stattdessen /Oicf**](-oi.md)[**/robust**](-robust.md) verwenden.

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Optimierungsoptionen* 
</dt> <dd>

Gibt die Methode zum Marshallen von Daten an. Verwenden Sie entweder "s" für Marshalling im gemischten Modus oder "i" für interpretiertes Marshalling.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Version von RPC bietet zwei Methoden zum Marshallen von Daten: gemischter Modus ("s") und interpretierter ("i"). Diese Methoden entsprechen den [**Befehlszeilenschaltern /Os**](-os.md) und [**/Oi.**](-oi.md) Die interpretierte Methode marshallt Daten vollständig offline. Dies kann zwar die Größe des Stubs erheblich reduzieren, aber die Leistung kann beeinträchtigt werden.

Wenn die Leistung ein Problem ist, kann die Methode im gemischten Modus der beste Ansatz sein. Im gemischten Modus kann der MIDL-Compiler bestimmen, zwischen welchen Daten inline gemarshallt und welche durch einen Aufruf einer Offlinebibliothek für dynamische Links gemarshallt werden. Wenn viele Prozeduren dieselben Datentypen verwenden, kann eine einzelne Prozedur wiederholt aufgerufen werden, um die Daten zu marshallen. Auf diese Weise werden Daten, die am besten für das Inline-Marshalling geeignet sind, inline verarbeitet, während andere Daten effizienter offline gemarshallt werden können.

Beachten Sie, **\[ dass das \] Optimize-Attribut** als Schnittstellenattribut oder als Vorgangsattribut verwendet werden kann. Wenn es als Schnittstellenattribut verwendet wird, wird der Standardwert für die gesamte Schnittstelle festgelegt, und Befehlszeilenschalter werden überschrieben. Wenn es jedoch als Vorgangsattribut verwendet wird, wirkt sich dies nur auf diesen Vorgang aus, das Überschreiben von Befehlszeilenschaltern und die Standardeinstellung der Schnittstelle.

## <a name="examples"></a>Beispiele

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




