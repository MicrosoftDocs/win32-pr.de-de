---
title: Untergeordnete Zuordnung innerhalb von Heaps
description: Ressourcen Heaps übertragen Daten von der CPU auf die GPU (Upload) und von der GPU zur CPU (Read Back).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103485"
---
# <a name="suballocation-within-heaps"></a>Untergeordnete Zuordnung innerhalb von Heaps

Ressourcen Heaps übertragen Daten von der CPU auf die GPU (Upload) und von der GPU zur CPU (Read Back).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | Beschreibung                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Speicher Aliasing und Datenvererbung](memory-aliasing-and-data-inheritance.md)<br/> | Die platzierte und die reservierte Ressource können den physischen Speicher innerhalb eines Heaps als Alias. Platzierte Ressourcen ermöglichen mehr Daten Vererbungs Szenarien als reservierte Ressourcen, wenn für den Heap das Shared-Flag festgelegt wurde oder wenn die Aliasing-Ressourcen vollständig definierte Speicher Layouts aufweisen. <br/> |
| [Freigegebene Heaps](shared-heaps.md)<br/>                                                 | Die Freigabe eignet sich für Multiprozess-und multiadapterarchitekturen.<br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[**ID3D12Device:: kreateheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Speicherverwaltung](memory-management.md)
</dt> </dl>

 

 





