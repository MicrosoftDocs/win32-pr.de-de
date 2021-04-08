---
description: Alle Ressourcen haben die folgenden Eigenschaften gemeinsam.
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: Ressourcen Eigenschaften (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747168"
---
# <a name="resource-properties-direct3d-9"></a>Ressourcen Eigenschaften (Direct3D 9)

Alle Ressourcen haben die folgenden Eigenschaften gemeinsam.

-   Verwendung. Die Art und Weise, wie eine Ressource verwendet wird, z. b. als Textur oder Renderziel.
-   Formatieren. Das Format der Daten, z. b. das Pixel Format einer 2D-Oberfläche.
-   Spool. Der Typ des Arbeitsspeichers, dem die Ressource zugeordnet ist.
-   Type (Typ). Der Ressourcentyp, z. b. ein Vertex-Puffer oder Renderziel.

Ressourcen Verwendungen werden erzwungen. Eine Anwendung, die in einem bestimmten Vorgang eine Ressource verwendet, muss diesen Vorgang zum Zeitpunkt der Ressourcen Erstellung angeben. Eine Liste der für Ressourcen definierten Verwendungs Konstanten finden Sie unter [**D3DUSAGE**](d3dusage.md).

Die \_ Konstanten D3DUSAGE rtpatches, D3DUSAGE \_ npatches und D3DUSAGE \_ Points geben dem Treiber an, dass die Daten in diesen Puffern wahrscheinlich für dreieckige oder Raster-Patches, N-Patches oder Punkt Sprites verwendet werden. Diese Flags werden bereitgestellt, wenn die Hardware diese Vorgänge ohne Host Verarbeitung nicht ausführen kann. Daher soll der Treiber diese Oberflächen im Systemspeicher zuordnen, damit die CPU darauf zugreifen kann. Wenn der Treiber diese Vorgänge vollständig in der Hardware ausführen kann, kann er diese Oberflächen im Video-oder AGP-Arbeitsspeicher zuordnen, um eine Host Kopie zu vermeiden und die Leistung mindestens doppelt zu verbessern. Beachten Sie, dass die von diesen Flags bereitgestellten Informationen nicht unbedingt erforderlich sind. Ein Treiber kann erkennen, dass solche Vorgänge für die Daten ausgeführt werden, und der Puffer wird für nachfolgende Frames wieder in den Systemspeicher verschoben.

Ausführliche Informationen zu den nutzungsflags und deren Beziehung zu bestimmten Ressourcen finden Sie auf den Referenzseiten zu den einzelnen Methoden zum Erstellen von Ressourcen.

Weitere Informationen zum Oberflächen Format von Ressourcen finden Sie unter dem enumerierten [D3DFORMAT](d3dformat.md) -Typ.

Die Klasse des Arbeitsspeichers, die die Puffer einer Ressource enthält, wird als Pool bezeichnet. Poolwerte werden durch den [**D3DPOOL**](./d3dpool.md) -enumerierten Typ definiert. Ein Pool kann nicht für verschiedene Objekte gemischt werden, die in einer einzelnen Ressource enthalten sind, d. h. MIP-Ebenen in einer MipMap, und wenn ein Pool für eine Ressource ausgewählt wird, kann der Pool nicht geändert werden.

Die Ressourcentypen werden implizit zur Laufzeit festgelegt, wenn die Anwendung eine Ressourcen Erstellungs Methode wie [**IDirect3DDevice9:: createcubetexture**](/windows/desktop/api)aufruft. Ressourcentypen werden durch den [**D3DRESOURCETYPE**](./d3dresourcetype.md) -enumerierten Typ definiert. Anwendungen können diese Typen zur Laufzeit Abfragen. Es wird jedoch erwartet, dass für die meisten Szenarien keine Lauf Zeittyp Überprüfung erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 
