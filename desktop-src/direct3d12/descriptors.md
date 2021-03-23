---
title: Deskriptoren
description: Deskriptoren sind die primäre Bindungs Einheit für eine einzelne Ressource in D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104144"
---
# <a name="descriptors"></a>Deskriptoren

Deskriptoren sind die primäre Bindungs Einheit für eine einzelne Ressource in D3D12.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über Deskriptoren](descriptors-overview.md)<br/> | Deskriptoren werden von API-aufrufen erstellt und identifizieren Ressourcen.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Erstellen von Deskriptoren](creating-descriptors.md)<br/> | Beschreibt und zeigt Beispiele für das Erstellen von Index-, Vertex-und konstantenpuffersichten. Shader-Ressource, Renderziel, unsortierter Zugriff, Streamausgabe-und tiefen Schablonen Ansichten; und Samplers. Alle Methoden zum Erstellen von Deskriptoren sind frei Thread.<br/>                                                                                                                             |
| [Kopieren von Deskriptoren](copying-descriptors.md)<br/>   | Die [**ID3D12Device:: copydescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) -Methode und die [**ID3D12Device:: copydescriptorssimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) -Methode auf der Geräteschnittstelle verwenden die CPU zum sofortigen Kopieren von Deskriptoren. Sie können als frei Thread bezeichnet werden, solange mehrere Threads auf der CPU oder GPU keine potenziell in Konflikt stehenden Schreibvorgänge durchführen.<br/> |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> </dl>

 

 





