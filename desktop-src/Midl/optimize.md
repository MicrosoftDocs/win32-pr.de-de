---
title: Attribut optimieren
description: Das Attribut "\ optimieren \ ACF" wird verwendet, um den Grad der Verlauf für das Marshalling von Daten zu optimieren.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- Attribut-Mittel l optimieren
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341272"
---
# <a name="optimize-attribute"></a>Attribut optimieren

Das ACF-Attribut "optimieren" wird verwendet, um den Grad der Verlauf für das Marshalling von Daten zu **\[ optimieren \]** .

> [!Note]  
> Dieses Schlüsselwort ist nicht mehr verwendende und sollte nicht verwendet werden. Die aktuellen Mittell-Kompilierungen sollten stattdessen [**/Oicf**](-oi.md)[**/robust**](-robust.md) verwenden.

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Optimierung: Optionen* 
</dt> <dd>

Gibt die Methode für das Mars Hallen von Daten an. Verwenden Sie entweder "s" für das Marshalling in gemischtem Modus oder "i" für interpretiertes Marshalling.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese RPC-Version bietet zwei Methoden zum Marshalling von Daten: gemischter Modus ("s") und interpretiertes ("i"). Diese Methoden entsprechen den Befehls zeilenschaltern [**/OS**](-os.md) und [**/Oi**](-oi.md) . Die interpretierte-Methode Marshalls Daten vollständig offline. Obwohl dies die Größe des Stubs erheblich verringern kann, kann die Leistung beeinträchtigt werden.

Wenn die Leistung von Bedeutung ist, kann die Methode mit gemischtem Modus die beste Vorgehensweise sein. Der gemischte Modus ermöglicht es dem Mittelwert Compiler, die Bestimmung zwischen den Daten, die Inline gemarshallt werden, und die durch einen Rückruf einer Offline-Dynamic Link Library gemarshallt werden. Wenn viele Prozeduren dieselben Datentypen verwenden, kann eine einzelne Prozedur wiederholt aufgerufen werden, um die Daten zu Mars Hallen. Auf diese Weise werden Daten, die am besten für das Inline Marshalling geeignet sind, Inline verarbeitet, während andere Daten effizienter im Offline Modus gemarshallt werden können.

Beachten Sie, dass das Attribut " **\[ optimieren \]** " als Schnittstellen Attribut oder als Vorgangs Attribut verwendet werden kann. Wenn Sie als Schnittstellen Attribut verwendet wird, wird der Standardwert für die gesamte Schnittstelle festgelegt und Befehls Zeilenschalter überschrieben. Wenn Sie jedoch als Vorgangs Attribut verwendet wird, wirkt sich dies nur auf diesen Vorgang aus, wobei Befehls Zeilenschalter und der Standard der-Schnittstelle überschrieben werden.

## <a name="examples"></a>Beispiele

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**/OS**](-os.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




