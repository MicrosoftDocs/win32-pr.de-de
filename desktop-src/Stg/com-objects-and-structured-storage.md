---
title: COM-Objekte und strukturierte Storage
description: Eine der häufigsten aktuellen Verwendungsmöglichkeiten persistenter Eigenschaften ist die Verwendung dieser Eigenschaften zum Speichern von Daten zu einem Systemobjekt, z. B. einem Dokument, mit diesem Objekt.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- COM-Objekte und strukturierte Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4c1405ddfaa060aa249090fc58b25b294a8c9aecc5f7b885d21b55bc162198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663590"
---
# <a name="com-objects-and-structured-storage"></a>COM-Objekte und strukturierte Storage

Eine der häufigsten aktuellen Verwendungsmöglichkeiten persistenter Eigenschaften ist die Verwendung dieser Eigenschaften zum Speichern von Daten zu einem Systemobjekt, z. B. einem Dokument, mit diesem Objekt. Es besteht natürlich das Potenzial, Eigenschaften mit jedem Objekt zu speichern, z. B. einem Drucker, sodass es nur erforderlich wäre, die Eigenschaften zu überprüfen, um den Speicherort, den Typ und so weiter zu bestimmen. Ein Benutzerobjekt kann über einen Eigenschaftensatz verfügen, der Daten wie Vorname, Nachname, Office und Telefon. Anwendungen können geschrieben werden, um eine systemweite Gruppe von Objekten basierend auf ihren Eigenschaften abfragt, z. B. zum Anzeigen aller Drucker, die sich in einem bestimmten Gebäude befinden. Aktuelle Systeme verwenden jedoch am häufigsten Eigenschaften für Dokumente.

Der von COM definierte primäre Eigenschaftensatzstandard ist [Der Zusammenfassungsinformations-Eigenschaftensatz.](the-summary-information-property-set.md) Dieser Eigenschaftensatz ist einfach und wird häufig verwendet. Die meisten Dokumente, die von Anwendungen erstellt werden, verfügen über einen gemeinsamen Satz von Attributen, die für Benutzer dieser Dokumente nützlich sind. Zu diesen Attributen gehören der Name des Dokumentautors, der Betreff des Dokuments, die Erstellung des Dokuments und so weiter. Zwei weitere Eigenschaftensätze werden für Microsoft Office 95 definiert, Office 97 und höher. Dies sind der COM-Dokumentzusammenfassungs-Eigenschaftensatz und User-Defined Eigenschaftensatz. Weitere Informationen finden Sie unter [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md).

In Windows 3.1 hatte jede Anwendung eine andere Möglichkeit, diese Daten in ihren Dokumenten zu speichern. Um die Zusammenfassungsinformationen für ein bestimmtes Dokument zu untersuchen, musste der Benutzer die Anwendung ausführen, die das Dokument erstellt hat, es öffnen und das Dialogfeld Zusammenfassungsinformationen der Anwendung aufrufen, damit nur die Anwendung ihre Zusammenfassungsinformationen anzeigen konnte.

COM-Eigenschaftensätze und die Eigenschaftensatzschnittstellen ermöglichen das Anzeigen der Dokumenteigenschaften, ohne die erstellende Anwendung ausführen zu müssen. Beispielsweise speichern alle Versionen von Microsoft Word 6.0 oder höher und viele andere COM-fähige Anwendungen jetzt ihre Dokumente mithilfe von strukturiertem COM-Speicher und dem hier beschriebenen Eigenschaftensatzstandard. Daher können andere Office Suite-Anwendungen den [](the-summary-information-property-set.md) Eigenschaftssatz für Zusammenfassungsinformationen für eine solche Datei anzeigen, solange diese Datei eine COM-strukturierte Speicherdatei ist und die erstellende Anwendung die Informationen im COM-Eigenschaftensatzformat gespeichert hat. Die Windows 95- oder Windows 98-Shell verwendet dies beispielsweise und ermöglicht dem Endbenutzer, die Eigenschaften eines beliebigen Word 6.0- oder höher-Dokuments direkt in der Shell anzeigen zu können.

Um Eigenschaftensätze aus anderen Anwendungen zu verwenden, müssen die anderen Anwendungen erkennen, wie die Eigenschaften innerhalb eines Eigenschaftensets interpretiert werden, was einen Standard impliziert. COM hat diesen Ansatz durch die Definition eines Standardeigenschaftssets, des COM Summary Information Property Set, zum Ziel gesetzt. Jede Anwendung, die über die Definition dieses Eigenschaftensatz verfügt, kann problemlos auf die Zusammenfassungsinformationen zugreifen, die in jedem Dokument enthalten sind, das von einer COM-Anwendung erstellt wurde, die diese Eigenschaftensatzspezifikation verwendet.

 

 




