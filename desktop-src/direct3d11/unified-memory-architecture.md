---
title: Einheitliche Speicherarchitektur
description: Die Abfrage, ob Unified Memory Architecture (UMA) unterstützt wird, kann dabei helfen, zu bestimmen, wie einige Ressourcen behandelt werden.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09648c69f312f16d1301b6c9b5cad21d544bd456f244950486cf9d6871079c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119375670"
---
# <a name="unified-memory-architecture"></a>Einheitliche Speicherarchitektur

Die Abfrage, ob Unified Memory Architecture (UMA) unterstützt wird, kann dabei helfen, zu bestimmen, wie einige Ressourcen behandelt werden.

Ein vom Treiber festgelegter boolescher Wert kann aus der [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) gelesen werden, um zu bestimmen, ob die Hardware UMA unterstützt.

Anwendungen, die unter UMA ausgeführt werden, möchten möglicherweise mehr Ressourcen mit aktivierten CPU-Zugriff haben, als wenn er nicht verfügbar ist. UMA ermöglicht es Anwendungen, das Kopieren von Ressourcendaten zu vermeiden, anstatt nur für Nicht-UMA-Grafikkarten effizient zu bleiben. [Direct3D 11.3-Features](direct3d-11-3-features.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11.3-Features](direct3d-11-3-features.md)
</dt> </dl>

 

 




