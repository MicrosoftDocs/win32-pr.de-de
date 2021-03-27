---
title: Einheitliche Speicherarchitektur
description: Die Abfrage, ob eine einheitliche Speicherarchitektur (UMA) unterstützt wird, kann Ihnen dabei helfen zu bestimmen, wie einige Ressourcen behandelt werden.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947467"
---
# <a name="unified-memory-architecture"></a>Einheitliche Speicherarchitektur

Die Abfrage, ob eine einheitliche Speicherarchitektur (UMA) unterstützt wird, kann Ihnen dabei helfen zu bestimmen, wie einige Ressourcen behandelt werden.

Ein boolescher Wert, der vom Treiber festgelegt wird, kann aus der [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) -Struktur gelesen werden, um zu bestimmen, ob die Hardware "Uma" unterstützt.

Anwendungen, die in einer anderen Sprache ausgeführt werden, benötigen möglicherweise mehr Ressourcen mit aktiviertem CPU-Zugriff, als wenn Sie nicht verfügbar sind. Mit Uma können Anwendungen nicht mehr Ressourcen Daten kopieren, sondern nur für nicht-Uma-Grafikadapter. [Direct3D 11,3-Features](direct3d-11-3-features.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11,3-Features](direct3d-11-3-features.md)
</dt> </dl>

 

 




