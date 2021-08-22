---
description: Synchronisierungswerte können automatisch durch die Konfiguration anderer Eigenschaften bestimmt oder eingeschränkt werden, z. B. transaktionale Anforderungen und JIT-Aktivierung (Just-In-Time).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Synchronisierungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2976426d652ca50c4e7399f39e98ba13ef337d15ef8c15a2271d4a562d1790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499730"
---
# <a name="synchronization-dependencies"></a>Synchronisierungsabhängigkeiten

Synchronisierungswerte können automatisch durch die Konfiguration anderer Eigenschaften bestimmt oder eingeschränkt werden, z. B. transaktionale Anforderungen und JIT-Aktivierung (Just-In-Time). COM+ erzwingt beispielsweise die Synchronisierung sowohl für transaktionsbasierte als auch für JIT-aktivierte Komponenten.

Diese Abhängigkeiten sind vorhanden, da Komponenten, die JIT-aktiviert sind oder an Transaktionen teilnehmen, ein ordnungsgemäßes Isolations- und Parallelitätsverhalten aufweisen müssen. Aus diesem Grund erfordert COM+, dass der Zugriff auf diese Komponenten serialisiert wird, indem die Synchronisierung erzwungen wird. (Ausführliche Informationen zu diesen Abhängigkeiten finden Sie unter [COM+ Just-in-Time-Aktivierung](com--just-in-time-activation.md).)

Die folgenden Tabellen zeigen die Merkmale der COM+-Synchronisierungsattributwerte.

### <a name="transactional-requirement"></a>Transaktionsanforderung



| Wenn Transaktionen auf festgelegt sind | Die Synchronisierung kann auf festgelegt werden.                    |
|------------------------------|--------------------------------------------------|
| Disabled<br/>          | Alles, abhängig von der JIT-Aktivierung<br/> |
| Nicht unterstützt<br/>     | Alles, abhängig von der JIT-Aktivierung<br/> |
| Unterstützt<br/>         | Erforderlich<br/>                              |
| Erforderlich<br/>          | Erforderlich<br/>                              |
| Requires New<br/>      | Erforderlich oder erfordert Neue<br/>              |



 

### <a name="jit-activation"></a>JIT-Aktivierung



| Wenn jit activation (JIT-Aktivierung) auf festgelegt ist | Die Synchronisierung kann auf festgelegt werden.       |
|-------------------------------|-------------------------------------|
| Aktiviert<br/>            | Erforderlich oder erfordert Neue<br/> |
| Disabled<br/>           | Etwas<br/>                 |



 

Weitere Informationen dazu, wie sich Transaktions-, JIT-Aktivierungs- und Synchronisierungsattribute verhalten, finden Sie unter [Konfigurieren von Transaktionen.](configuring-transactions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen des Synchronisierungsattributs](setting-the-synchronization-attribute.md)
</dt> <dt>

[Synchronisierungsattributwerte](synchronization-attribute-values.md)
</dt> </dl>

 

 




