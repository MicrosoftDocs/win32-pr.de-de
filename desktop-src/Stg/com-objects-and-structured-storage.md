---
title: COM-Objekte und strukturierter Speicher
description: Eine der gängigsten aktuellen Verwendungsmöglichkeiten von permanenten Eigenschaften besteht darin, Sie zum Speichern von Daten über ein Systemobjekt (z. b. ein Dokument) mit diesem Objekt zu verwenden.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- COM-Objekte und strukturierter Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a3d2fb9c145538bbd6b5e87dfcc9523feff78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388041"
---
# <a name="com-objects-and-structured-storage"></a>COM-Objekte und strukturierter Speicher

Eine der gängigsten aktuellen Verwendungsmöglichkeiten von permanenten Eigenschaften besteht darin, Sie zum Speichern von Daten über ein Systemobjekt (z. b. ein Dokument) mit diesem Objekt zu verwenden. Es gibt natürlich das Potenzial, Eigenschaften mit einem beliebigen Objekt, z. b. einem Drucker, zu speichern. Daher ist es nur notwendig, die Eigenschaften zu überprüfen, um den Speicherort, den Typ usw. zu ermitteln. Ein Benutzerobjekt kann einen Eigenschaften Satz aufweisen, der Daten wie Vorname, Nachname, Office und Telefon enthält. Anwendungen können so geschrieben werden, dass eine systemweite Gruppe von Objekten basierend auf ihren Eigenschaften abgefragt wird, z. b. wenn alle Drucker in einem bestimmten Gebäude angezeigt werden. Aktuelle Systeme verwenden jedoch häufig Eigenschaften für Dokumente.

Der von com definierte primäre Eigenschaften Satz Standard ist [der Eigenschaften Satz für Zusammenfassungs Informationen](the-summary-information-property-set.md). Dieser Eigenschaften Satz ist sowohl einfach als auch häufig verwendet. Die meisten von Anwendungen erstellten Dokumente verfügen über einen gemeinsamen Satz von Attributen, die für Benutzer dieser Dokumente nützlich sind. Diese Attribute enthalten den Namen des Dokument Autors, den Betreff des Dokuments, den Zeitpunkt der Erstellung usw. Zwei weitere Eigenschaften Sätze sind für Microsoft Office 95, Office 97 und höher definiert. Dabei handelt es sich um den Eigenschaften Satz com-Dokument Zusammenfassung und den User-Defined Eigenschaften Satz. Weitere Informationen finden Sie unter [serialisiertes Eigenschaften Satz Format für strukturierte Speicherung](structured-storage-serialized-property-set-format.md).

In Windows 3,1 hatte jede Anwendung eine andere Möglichkeit, diese Daten in Ihren Dokumenten zu speichern. Zum Überprüfen der Zusammenfassungs Informationen für ein bestimmtes Dokument musste der Benutzer die Anwendung ausführen, die das Dokument erstellt hat, ihn öffnen und das Dialogfeld "Informationen zur Anwendungs Zusammenfassung" aufrufen, sodass nur die Anwendung seine Zusammenfassungs Informationen anzeigen kann.

Mit com-Eigenschaften Sätzen und den Eigenschaften Satz Schnittstellen können die Dokumenteigenschaften angezeigt werden, ohne dass die erstellenden Anwendungen ausgeführt werden. Beispielsweise speichern alle Versionen von Microsoft Word 6,0 oder höher und viele andere com-aktivierte Anwendungen Ihre Dokumente jetzt mithilfe von com-strukturiertem Speicher und dem hier beschriebenen Eigenschaften Satz Standard. Daher können von anderen Office Suite-Anwendungen [die Eigenschaften für Zusammenfassungs Informationen](the-summary-information-property-set.md) für eine solche Datei angezeigt werden, solange die Datei eine strukturierte com-Speicherdatei ist und die Erstellungs Anwendung die Informationen im com-Eigenschaften Satz Format gespeichert hat. Die Shell Windows 95 oder Windows 98 verwendet diese z. b., und ermöglicht dem Endbenutzer, die Eigenschaften eines beliebigen Word 6,0-Dokuments oder eines späteren Dokuments direkt aus der Shell anzuzeigen.

Um Eigenschaften Sätze aus anderen Anwendungen verwenden zu können, müssen die anderen Anwendungen erkennen, wie die Eigenschaften innerhalb eines Eigenschaften Satzes interpretiert werden, was einen Standard impliziert. Com hat diesen Ansatz vorangetrieben, indem ein Standardeigenschaften Satz definiert wurde, der Eigenschaften Satz für com-Zusammenfassungs Informationen. Jede Anwendung, die über die Definition dieses Eigenschaften Satzes verfügt, kann problemlos auf die Zusammenfassungs Informationen zugreifen, die in einem von einer COM-Anwendung erstellten Dokument enthalten sind, das diese Eigenschaften Satz Spezifikation verwendet.

 

 




