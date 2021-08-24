---
title: Arbeitsspeicherverwaltung in Direct3D 12
description: Der Wechsel zu D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicherresidenz.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42547b85836711efc4e9aa5b621d90c672617aacff779567f118d4af5041512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123793"
---
# <a name="memory-management-in-direct3d-12"></a>Arbeitsspeicherverwaltung in Direct3D 12

Der Wechsel zu D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicherresidenz. Das Verwalten der Speicherresidenz bedeutet, dass noch mehr Synchronisierung durchgeführt werden muss. In diesem Abschnitt werden Strategien für die Speicherverwaltung und die Unterzuordnung innerhalb von Heaps und Puffern behandelt.

-   [In diesem Abschnitt](#in-this-section)
-   [Zugehörige Themen](#related-topics)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategien für die Arbeitsspeicherverwaltung](memory-management-strategies.md)<br/> | Ein Speicher-Manager für Direct3D 12 kann sehr schnell mit allen verschiedenen Unterstützungsebenen, für UMA- oder diskrete Adapter (nicht UMA) und mit einer beträchtlichen Bandbreite von Architekturunterschieden zwischen GPU-Adaptern sehr kompliziert werden.<br/> Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung , die in diesem Abschnitt beschrieben wird, ist "klassifizieren, budgetieren und streamen".<br/> |
| [Unterzuweisung innerhalb von Puffern](large-buffers.md)<br/>                | Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen eine große Anzahl vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier gängige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.<br/>                                                                                                                                     |
| [Unterzuweisung innerhalb von Heaps](suballocation-within-heaps.md)<br/>     | Ressourcenhaps übertragen Daten von der CPU an die GPU (Upload) und von der GPU an die CPU (Zurücklesen). <br/>                                                                                                                                                                                                                                                                  |
| [Residenz](residency.md)<br/>                                       | Ein Objekt wird als *"resident" betrachtet,* wenn es von der GPU zugänglich ist.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> </dl>

 

 





