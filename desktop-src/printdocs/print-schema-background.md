---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Hintergrund des Druck Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93280b6c8de62c76acdd59e2e596a0f600702451
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761565"
---
# <a name="print-schema-background"></a>Hintergrund des Druck Schemas

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Das Druck Schema dient dazu, die Probleme der opaqueness und der Mehrdeutigkeit in Bezug auf die interne Kommunikation zwischen den Komponenten des Druck Subsystems und die externe Kommunikation zwischen dem Druck Subsystem und den Anwendungen zu behandeln.

Die aktuelle Interaktion des Druck Subsystems mit den Plug-Ins für Anwendungen und Hardware Anbieter verwendet die binäre, indexbasierte DEVMODE-Struktur und binäre devcaps. Die Einstellungen, die von den einzelnen Komponenten vorgenommen werden, sind für andere Komponenten größtenteils nicht transparent, was die Portabilität von Einstellungen zwischen Geräten oder sogar zwischen verschiedenen Treiberversionen auf demselben Gerät verhindert. Darüber hinaus können printfunktionen nicht einfach von Client Anwendungen genutzt werden, ohne dass entweder proprietäre Kenntnisse des Geräts oder die Benutzeroberfläche des Treibers verwendet werden. Zusätzlich zu diesen Einschränkungen gibt es in größerem Sinn keine klar definierte Sprache, um allgemeine Geräte Attribute, Druckfunktionen, Geräte Konfigurationen oder die Auftrags Formatierung zu beschreiben. Das Druck Schema und seine zugehörigen Technologien sind so konzipiert, dass diese Einschränkungen behandelt werden, indem eine konsistente, eindeutige und erweiterbare Methode für die Kommunikation von Einstellungen und Funktionen auf konsolidierte und logische Weise bereitgestellt wird.

Die konzeptionellen Grundlagen der Druck Schema Schlüsselwörter und des Druck Schema-Frameworks sind Konsistenz, fehlende Mehrdeutigkeit und Erweiterbarkeit. Konsistenz wird durch die Verwendung der Druck Schema Schlüsselwörter und des Druck Schema-Frameworks als Bausteine für die Kommunikation zwischen den Druckkomponenten der nächsten Generation erreicht. Anwendungen, das Microsoft Windows-Druck Subsystem und IHV-Plug-ins und-Treiber interagieren mithilfe dieses allgemeinen Mechanismus. Diese Schlüsselwörter, ihre Struktur und ihre Bedeutung werden vom öffentlichen Schema wohl definiert. Dies verhindert Mehrdeutigkeiten in der Bedeutung eines bestimmten Schlüssel Worts und verhindert redundante oder doppelte Schlüsselwörter. Alle Komponenten können sich darauf verlassen, dass ein bestimmtes Schlüsselwort verwendet wird, um eine bestimmte Absicht zu vermitteln, und dass diese Absicht vom Empfänger gut verstanden werden kann. Die Erweiterbarkeit ist wichtig, um die Lebensdauer der Druck Schema Schlüsselwörter zu gewährleisten und sicherzustellen, dass das öffentliche Schema eine dynamische Entität ist. Die Struktur lässt auch private Erweiterungen zu, die IHVs die Flexibilität bei der Entwicklung der gewünschten Innovation gewährt. die zukünftige Einbindung eines privaten Schlüssel Worts in das öffentliche Schema ist für die Beibehaltung der Konsistenz und die Vermeidung von Mehrdeutigkeit von entscheidender Bedeutung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



