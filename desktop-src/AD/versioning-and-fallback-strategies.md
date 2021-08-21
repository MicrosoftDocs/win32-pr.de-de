---
title: Versions- und Fallbackstrategien
description: Wenn eine Anwendung eine Teilaktualisierung mit einer der oben genannten Techniken erkennt oder einen Satz von Objekten liest, deren Gültigkeitsdatum noch nicht erreicht wurde, muss die Anwendung die Situation ordnungsgemäß behandeln.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Versions- und Fallbackstrategien AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55226efcd72cec4f6dbe65447a945733dac88a56b976661bcf24564c9b366ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024413"
---
# <a name="versioning-and-fallback-strategies"></a>Versions- und Fallbackstrategien

Wenn eine Anwendung eine Teilaktualisierung mit einer der oben genannten Techniken erkennt oder einen Satz von Objekten liest, deren Gültigkeitsdatum noch nicht erreicht wurde, muss die Anwendung die Situation ordnungsgemäß behandeln. Bei einigen Anwendungen ist die ordnungsgemäß reagierende Antwort ein "Fallback" auf eine frühere Version der betreffenden Objekte. Active Directory Domain Services bieten keine Versionsfunktion– Anwendungen, die diese Funktion wünschen, müssen sie selbst bereitstellen. Zu den Ansätzen für die Versionsverwaltung gehören das lokale Zwischenspeichern der "letzten bekannten guten" Werte und das Speichern mehrerer Objektsätze im Verzeichnis, z. B. in "alten", "aktuellen" und "neuen" Containern. Viele andere Schemas sind möglich.

Implementierungen müssen darauf achten, unbeabsichtigte Folgen zu vermeiden. Eine frühere Version von -Objekten sollte nur verwendet werden, wenn ein Teilupdate erkannt wird oder die neuen Objekte noch nicht "effektiv" sind. Ein Fallback, da etwas in der Anwendung "nicht funktioniert", könnte die Absicht eines Administrators umgehen. Beispielsweise könnten zwei Computer, die früher kommunizieren konnten, aufgrund einer Änderung der IPsec-Richtlinie (Internet Protocol Security) dazu nicht in der Lage sein. Wenn dies vom Administrator beabsichtigt ist, sollten die betroffenen Systeme nicht auf die Richtlinie zurückgreifen, die die Kommunikation ermöglicht hat, da dies eine Sicherheitsverletzung wäre.

 

 




