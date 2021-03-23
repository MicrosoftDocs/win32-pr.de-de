---
title: Speicherverwaltung in Direct3D 12
description: Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicher Residenz.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103400"
---
# <a name="memory-management-in-direct3d-12"></a>Speicherverwaltung in Direct3D 12

Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicher Residenz. Das Verwalten der Speicher Residenz bedeutet, dass noch mehr Synchronisierungen ausgeführt werden müssen. In diesem Abschnitt werden die Strategien für die Speicherverwaltung und die unter Zuordnung von Heaps und Puffern behandelt.

-   [In diesem Abschnitt](#in-this-section)
-   [Verwandte Themen](#related-topics)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategien für die Speicherverwaltung](memory-management-strategies.md)<br/> | Ein Speicher-Manager für Direct3D 12 kann mit allen unterstützten Unterstützungs Ebenen, für UMA-oder diskrete (nicht-UMA-) Adapter und mit einer beträchtlichen Bandbreite an Architektur Unterschiede zwischen GPU-Adaptern sehr kompliziert werden.<br/> Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist "klassifizieren, Budget und Stream".<br/> |
| [Untergeordnete Zuordnung innerhalb von Puffern](large-buffers.md)<br/>                | Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier häufige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.<br/>                                                                                                                                     |
| [Untergeordnete Zuordnung innerhalb von Heaps](suballocation-within-heaps.md)<br/>     | Ressourcen Heaps übertragen Daten von der CPU auf die GPU (Upload) und von der GPU zur CPU (Read Back). <br/>                                                                                                                                                                                                                                                                  |
| [Aufenthaltes](residency.md)<br/>                                       | Ein Objekt gilt als *residente* , wenn es von der GPU zugänglich ist.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> </dl>

 

 





