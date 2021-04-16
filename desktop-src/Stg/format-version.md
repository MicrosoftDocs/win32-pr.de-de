---
title: Format Version
description: Der Format Versions Wert ist ein Word-Datentyp, der verwendet wird, um die Format Version dieses Streams anzugeben.
ms.assetid: 38362a45-4f49-4a85-aabe-452ff32c2812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503019a3bfe3224e4137ac3bfd43fadbe1e15a3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516892"
---
# <a name="format-version"></a>Format Version

Der Format Versions Wert ist ein **Word** -Datentyp, der verwendet wird, um die Format Version dieses Streams anzugeben. Der Wert kann 0 oder 1 sein. Der Format-Version-Indikator muss beim Lesen des Eigenschaften Satzes geprüft werden. Wenn Sie nicht 0 (null) oder eins ist, wurde der Stream in eine andere Spezifikation geschrieben und kann nicht von Code gelesen werden, der gemäß dieser Spezifikation entwickelt wurde.

Eigenschaften Sätze mit Format Version 1 entsprechen Version 0, mit den folgenden Ergänzungen:

-   Die **Groß-/Kleinschreibung** beachten Eigenschaftsnamen werden in der reservierten Dictionary-Eigenschaft, der Eigen [schafts-ID 0](/windows/desktop/Stg/reserved-property-identifiers), gespeichert. In Eigenschaften Sätzen der Version 1 kann bei diesen Namen die Groß-/Kleinschreibung beachtet werden. Die Unterscheidung nach Groß-/Kleinschreibung wird durch die Eigenschaft reserviertes Verhalten, [Eigenschaften-ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers)
-   **Lange Eigenschaftsnamen**. Eigenschaften Sätze der Version 1, im Gegensatz zu Eigenschaften Sätzen der Version 0, sind in der Länge von Eigenschaftsnamen nicht beschränkt. Weitere Informationen zu Eigenschaftsnamen finden Sie unter [Property ID 0](/windows/desktop/Stg/reserved-property-identifiers) .
-   **Eigenschafts Typen**. Die Eigenschaften Sätze der Version 1 können alle Eigenschafts Typen enthalten, die in einem Eigenschaften Satz der Version 0 und einigen zusätzlichen Typen enthalten sein können. Weitere Informationen zu diesen Typen finden Sie in der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur.

 

 