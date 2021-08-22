---
description: Beschreibt grundlegende E/A-Konzepte.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: E/A-Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08c8b95df0f5319f9acb62c677b5448ff3f962c8a49eb43c444c391bf139ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533680"
---
# <a name="io-concepts"></a>E/A-Konzepte

Die folgenden E/A-Konzepte werden in diesem Abschnitt beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                               | Beschreibung                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateipufferung](file-buffering.md)<br/>                                     | Beschreibt Überlegungen zur Anwendungssteuerung der Dateipufferung, die auch als nicht gepufferte Dateieingabe/-ausgabe (E/A) bezeichnet wird.<br/>                                    |
| [Dateizwischenspeicherung](file-caching.md)<br/>                                         | Windows zwischengespeicherte Dateidaten, die von Datenträgern gelesen und auf Datenträger geschrieben werden.<br/>                                                                                   |
| [Synchrone und asynchrone E/A](synchronous-and-asynchronous-i-o.md)<br/> | Es gibt zwei Arten der Eingabe-/Ausgabesynchronisierung (E/A): synchrone E/A und asynchrone E/A. Asynchrone E/A wird auch als überlappende E/A bezeichnet.<br/> |
| [Abbrechen ausstehender E/A-Vorgänge](canceling-pending-i-o-operations.md)<br/> | Wenn Benutzer E/A-Anforderungen abbrechen können, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden.<br/>                             |
| [Warnungsfähige E/A](alertable-i-o.md)<br/>                                       | Warnungsfähige E/A ist die Methode, mit der Anwendungsthreads asynchrone E/A-Anforderungen nur verarbeiten, wenn sie sich in einem warnbaren Zustand befinden.<br/>                     |
| [E/A-Abschlussports](i-o-completion-ports.md)<br/>                         | E/A-Abschlussports bieten ein effizientes Threadingmodell für die Verarbeitung mehrerer asynchroner E/A-Anforderungen auf einem Multiprozessorsystem.<br/>                  |



 

 

 




