---
description: Beschreibt grundlegende e/a-Konzepte.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: E/a-Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353936"
---
# <a name="io-concepts"></a>E/a-Konzepte

Die folgenden e/a-Konzepte werden in diesem Abschnitt beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                               | BESCHREIBUNG                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateipufferung](file-buffering.md)<br/>                                     | Beschreibt Überlegungen zur Anwendungssteuerung der Datei Pufferung, auch bekannt als nicht gepufferte Dateieingabe/-Ausgabe (e/a).<br/>                                    |
| [Dateizwischenspeicherung](file-caching.md)<br/>                                         | Windows speichert Datei Daten, die von Datenträgern gelesen und auf Datenträger geschrieben werden.<br/>                                                                                   |
| [Synchrone und asynchrone e/a](synchronous-and-asynchronous-i-o.md)<br/> | Es gibt zwei Arten der Eingabe-/ausgabesynchronisierung (e/a): Synchrone e/a-Vorgänge und asynchrone e/a-Vorgänge. Asynchrone e/a-Vorgänge werden auch als überlappende e/a-Vorgänge bezeichnet.<br/> |
| [Abbrechen von ausstehenden e/a-Vorgängen](canceling-pending-i-o-operations.md)<br/> | Benutzern das Abbrechen von e/a-Anforderungen, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden.<br/>                             |
| [Warn Bare e/a](alertable-i-o.md)<br/>                                       | Warn Bare e/a ist die Methode, mit der Anwendungsthreads asynchrone e/a-Anforderungen verarbeiten, wenn Sie sich in einem wartungstabellenzustand befinden.<br/>                     |
| [E/a-Abschlussports](i-o-completion-ports.md)<br/>                         | E/a-Abschlussports stellen ein effizientes Threading Modell für die Verarbeitung mehrerer asynchroner e/a-Anforderungen auf einem Multiprozessorsystem dar.<br/>                  |



 

 

 




