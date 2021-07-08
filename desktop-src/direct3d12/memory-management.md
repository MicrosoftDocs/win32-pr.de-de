---
title: Arbeitsspeicherverwaltung in Direct3D 12
description: Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicherresidenz.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481805"
---
# <a name="memory-management-in-direct3d-12"></a>Arbeitsspeicherverwaltung in Direct3D 12

Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicherresidenz. Die Verwaltung der Speicherresidenz bedeutet, dass noch mehr Synchronisierung durchgeführt werden muss. In diesem Abschnitt werden Strategien für die Speicherverwaltung und die Unterzuordnung in Heaps und Puffern behandelt.

-   [In diesem Abschnitt](#in-this-section)
-   [Verwandte Themen](#related-topics)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategien für die Arbeitsspeicherverwaltung](memory-management-strategies.md)<br/> | Ein Speicher-Manager für Direct3D 12 kann sehr schnell mit allen verschiedenen Supportebenen, für UMA- oder diskrete Adapter (nicht UMA) und mit einem erheblichen Bereich von Architekturunterschieden zwischen GPU-Adaptern sehr kompliziert werden.<br/> Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist "Klassifizieren, Budget und Streamen".<br/> |
| [Unterzuweisung innerhalb von Puffern](large-buffers.md)<br/>                | Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier gängige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.<br/>                                                                                                                                     |
| [Unterzuweisung innerhalb von Heaps](suballocation-within-heaps.md)<br/>     | Ressourcenheaps übertragen Daten von der CPU zur GPU (Upload) und von der GPU zur CPU (zurücklesen). <br/>                                                                                                                                                                                                                                                                  |
| [Residenz](residency.md)<br/>                                       | Ein Objekt gilt als *resident,* wenn es von der GPU zugänglich ist.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> </dl>

 

 





