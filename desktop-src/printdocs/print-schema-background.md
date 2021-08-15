---
description: Das Druckschema behandelt Nichtdurchsichtigkeit und Mehrdeutigkeit in der Kommunikation zwischen Komponenten des Drucksubsystems und zwischen dem Drucksubsystem und Anwendungen.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Drucken des Schemahintergrunds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab366429623f2bb1f187294705d1a83e93acd1e5fb500d4b1e9d224496ac39e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731760"
---
# <a name="print-schema-background"></a>Drucken des Schemahintergrunds

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das Druckschema soll die Probleme der Nichtdurchsichtigkeit und Mehrdeutigkeit im Zusammenhang mit der internen Kommunikation zwischen den Komponenten des Drucksubsystems und der externen Kommunikation zwischen dem Drucksubsystem und Anwendungen behandeln.

Die aktuelle Interaktion des Drucksubsystems mit Anwendungen und Hardwareanbieter-Plug-Ins verwendet die binäre, indexbasierte DEVMODE-Struktur und binäre DevCaps. Einstellungen, die von den einzelnen Komponenten vorgenommen werden, sind für andere Komponenten größtenteils nicht transparent, sodass die Portabilität von Einstellungen zwischen Geräten oder sogar zwischen verschiedenen Treiberversionen auf demselben Gerät verhindert wird. Darüber hinaus können PrintCapabilities von Clientanwendungen nicht ohne proprietäre Kenntnisse des Geräts oder mithilfe der Benutzeroberfläche des Treibers genutzt werden. Zusätzlich zu diesen Einschränkungen gibt es im weiteren Sinne keine klar definierte Sprache, um allgemeine Geräteattribute, PrintCapabilities, Gerätekonfigurationen oder Auftragsformatierungen zu beschreiben. Das Druckschema und die zugehörigen Technologien sind darauf ausgelegt, diese Einschränkungen zu beheben, und bieten eine konsistente, eindeutige und erweiterbare Methode zur Konsolidierten und logischen Kommunikation von Einstellungen und Funktionen.

Die konzeptionellen Grundlagen der Druckschemaschlüsselwörter und des Druckschemaframeworks sind Konsistenz, fehlende Mehrdeutigkeit und Erweiterbarkeit. Konsistenz wird durch die Verwendung der Druckschemaschlüsselwörter und des Druckschemaframeworks als Bausteine für die Kommunikation zwischen Druckkomponenten der nächsten Generation erreicht. Anwendungen, das Drucksubsystem microsoft Windows sowie IHV-Plug-Ins und -Treiber interagieren mit diesem gängigen Mechanismus. Diese Schlüsselwörter, ihre Struktur und ihre Bedeutung werden durch das öffentliche Schema klar definiert. Dies verhindert Mehrdeutigkeiten in der Bedeutung eines bestimmten Schlüsselworts und redundante oder doppelte Schlüsselwörter. Alle Komponenten können sich auf die Verwendung eines bestimmten Schlüsselworts verlassen, um eine bestimmte Absicht zu vermitteln und diese Absicht vom Empfänger gut verstehen zu lassen. Erweiterbarkeit ist wichtig, um die Beständigkeit der Schlüsselwörter für Druckschemas zu gewährleisten, um sicherzustellen, dass das öffentliche Schema eine dynamische Entität ist. Die Struktur ermöglicht auch private Erweiterungen, die IHVs die Flexibilität bieten, innovationen nach Bedarf zu entwickeln. Beachten Sie dabei, dass die zukünftige Einbeziehung eines privaten Schlüsselworts in das öffentliche Schema entscheidend ist, um Konsistenz zu gewährleisten und Mehrdeutigkeit zu verhindern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



