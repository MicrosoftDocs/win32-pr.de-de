---
description: Synchronisierungs Werte können automatisch durch die Konfiguration anderer Eigenschaften, z. b. Transaktions Anforderungen und JIT-Aktivierung (Just-in-Time), festgelegt oder eingeschränkt werden.
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Synchronisierungs Abhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860968"
---
# <a name="synchronization-dependencies"></a>Synchronisierungs Abhängigkeiten

Synchronisierungs Werte können automatisch durch die Konfiguration anderer Eigenschaften, z. b. Transaktions Anforderungen und JIT-Aktivierung (Just-in-Time), festgelegt oder eingeschränkt werden. Beispielsweise erzwingt com+ die Synchronisierung sowohl für transaktionale als auch für JIT-aktivierte Komponenten.

Diese Abhängigkeiten sind vorhanden, da Komponenten, die JIT-aktiviert sind oder an Transaktionen teilnehmen, ordnungsgemäß Isolation und Parallelitäts Verhalten aufweisen müssen. Daher erfordert com+, dass der Zugriff auf diese Komponenten durch erzwingen der Synchronisierung serialisiert wird. (Ausführliche Informationen zu diesen Abhängigkeiten finden Sie unter [com+ Just-in-Time-Aktivierung](com--just-in-time-activation.md).)

In den folgenden Tabellen werden die Merkmale der com+-Synchronisierungs Attributwerte angezeigt.

### <a name="transactional-requirement"></a>Transaktionale Anforderung



| Wenn Transaktionen auf festgelegt sind | Die Synchronisierung kann auf festgelegt werden                    |
|------------------------------|--------------------------------------------------|
| Disabled<br/>          | Alles, abhängig von der JIT-Aktivierung<br/> |
| Nicht unterstützt<br/>     | Alles, abhängig von der JIT-Aktivierung<br/> |
| Unterstützt<br/>         | Erforderlich<br/>                              |
| Erforderlich<br/>          | Erforderlich<br/>                              |
| Requires New<br/>      | Erforderlich oder erfordert neu<br/>              |



 

### <a name="jit-activation"></a>JIT-Aktivierung



| Wenn die JIT-Aktivierung auf festgelegt ist | Die Synchronisierung kann auf festgelegt werden       |
|-------------------------------|-------------------------------------|
| Aktiviert<br/>            | Erforderlich oder erfordert neu<br/> |
| Disabled<br/>           | Dagegen<br/>                 |



 

Weitere Details dazu, wie sich die Transaktions-, JIT-Aktivierungs-und Synchronisierungs Attribute einander Verhalten, finden Sie unter [Konfigurieren von Transaktionen](configuring-transactions.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen des Synchronisierungs Attributs](setting-the-synchronization-attribute.md)
</dt> <dt>

[Werte der Synchronisierungs Attribute](synchronization-attribute-values.md)
</dt> </dl>

 

 




