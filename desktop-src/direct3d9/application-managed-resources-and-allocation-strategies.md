---
description: Verwaltete Vertexpuffer- oder Indexpufferressourcen können nicht als dynamisch deklariert werden, indem D3DUSAGE \_ DYNAMIC zum Zeitpunkt der Erstellung angegeben wird.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed Ressourcen und Zuordnungsstrategien (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86eabccde7fef025c952c869a30fdeff8cf5316ceb0316b513692175d8581a01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119430"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed Ressourcen und Zuordnungsstrategien (Direct3D 9)

Verwaltete Vertexpuffer- oder Indexpufferressourcen können nicht als dynamisch deklariert werden, indem D3DUSAGE \_ DYNAMIC zum Zeitpunkt der Erstellung angegeben wird. Dies erfordert eine zusätzliche Kopie für jede Änderung des Scheitelpunktpufferinhalts. Dynamische Scheitelpunktpuffer sind für das Rendern dynamischer Geometrien und Daten vorgesehen, die aus partitionierten Strukturen im Binärraum oder anderen Sichtbarkeitsdatenstrukturen extrahiert werden. Dies kann durch Vorabzuweisung von Puffern im gewünschten Format erreicht werden. Diese Ressourcen werden dann für die Unterstützung der Anwendungsanforderungen durch einen Ressourcen-Manager innerhalb der Anwendung verwendet. Die Gesamtzahl der dynamischen Scheitelpunktpuffer ist gering, da eine Anwendung nur wenige verschiedene Scheitelpunkt-Strides gleichzeitig verwendet und ein anderer Scheitelpunktpuffer nur für eindeutige Strides erforderlich ist. Wenn Sie dynamische Ressourcen auf diese Weise verwalten, stellen Sie sicher, dass hohe Anforderungen an die Ressourcen die Leistung der Anwendung nicht erheblich beeinträchtigen.

Wenn Sie Ressourcen verwenden, die sowohl von Direct3D als auch von Anwendungen verwaltet werden, ordnen Sie von der Anwendung verwaltete Ressourcen im D3DPOOL DEFAULT-Arbeitsspeicher zu, bevor Sie \_ mit Direct3D verwaltete Ressourcen erstellen. Dadurch kann der Arbeitsspeicher-Manager eine genaue Anzahl des verfügbaren Arbeitsspeichers verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 



