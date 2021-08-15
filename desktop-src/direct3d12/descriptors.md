---
title: Deskriptoren
description: Deskriptoren sind die primäre Bindungseinheit für eine einzelne Ressource in D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2b501a79eddf942e92a3296f2b23af58b08a69ebbb0cded2570752f96263b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530398"
---
# <a name="descriptors"></a>Deskriptoren

Deskriptoren sind die primäre Bindungseinheit für eine einzelne Ressource in D3D12.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über Deskriptoren](descriptors-overview.md)<br/> | Deskriptoren werden durch API-Aufrufe erstellt und identifizieren Ressourcen.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Erstellen von Deskriptoren](creating-descriptors.md)<br/> | Beschreibt und zeigt Beispiele für das Erstellen von Index-, Scheitelpunkt- und Konstantenpufferansichten. Shaderressource, Renderziel, ungeordneter Zugriff, Streamausgabe und Tiefenschablonenansichten; und Sampler. Alle Methoden zum Erstellen von Deskriptoren sind frei gethreadt.<br/>                                                                                                                             |
| [Kopieren von Deskriptoren](copying-descriptors.md)<br/>   | Die [**Methoden ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) und [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) auf der Geräteschnittstelle verwenden die CPU, um Deskriptoren sofort zu kopieren. Sie können als free threaded bezeichnet werden, solange mehrere Threads auf der CPU oder GPU keine potenziell in Konflikt stehenden Schreibvorgänge ausführen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> <dt>

[Stammsignaturen](root-signatures.md)
</dt> </dl>

 

 





