---
title: Datenformate und Übertragungsmedien
description: Datenformate und Übertragungsmedien
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccbab96fbaca83330737521f253b3c625e67ea9a024d87d35276da2826a3964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501430"
---
# <a name="data-formats-and-transfer-media"></a>Datenformate und Übertragungsmedien

Die meisten Plattformen, einschließlich Windows, definieren ein Standardprotokoll für die Übertragung von Daten zwischen Anwendungen, basierend auf einer Reihe von Funktionen, die als Zwischenablage bezeichnet werden. Anwendungen, die diese Funktionen verwenden, können Daten auch dann freigeben, wenn sich ihre nativen Datenformate stark unterscheiden. Im Allgemeinen weisen diese Zwischenablage zwei wesentliche Nachteile auf, die COM behoben hat.

Zunächst verwenden Datenbeschreibungen nur einen Formatbezeichner, z. B. den einzelnen 16-Bit-Zwischenablageformatbezeichner für Windows. Dies bedeutet, dass die Zwischenablage nur die Struktur ihrer Daten beschreiben kann, d. h. die Reihenfolge der Bits. Sie kann "I have a bitmap" (Ich habe eine Bitmap) "or I have some text" (Ich habe eine Bitmap) melden, aber es können nicht die Zielgeräte angegeben werden, für die die Daten zusammengesetzt sind, welche Ansichten oder Aspekte von sich selbst die Daten bereitstellen können oder welche Speichermedien für die Übertragung am besten geeignet sind. Beispielsweise kann nicht angezeigt werden: "Ich habe eine Textzeichenfolge, die im globalen Speicher gespeichert und zur Darstellung entweder auf dem Bildschirm oder auf einem Drucker formatiert ist" oder "Ich habe eine Bitmap für Miniaturansichtszeichnungen, die für einen 100-dpi-Punktmatrixdrucker gerendert und als Datenträgerdatei gespeichert ist".

Zweitens erfolgen alle Datenübertragungen, die die Zwischenablage verwenden, in der Regel über globalen Arbeitsspeicher. Die Verwendung des globalen Arbeitsspeichers ist für kleine Datenmengen relativ effizient, aber für große Mengen, z. B. ein 20 MB großes Multimediaobjekt, grauenhaft ineffizient. Der globale Arbeitsspeicher ist für ein großes Datenobjekt langsam, dessen Größe einen erheblichen Austausch des virtuellen Speichers auf dem Datenträger erfordert. In Fällen, in denen sich die ausgetauschten Daten ohnehin größtenteils auf dem Datenträger befinden, ist das Erzwingen dieses Engpasses im virtuellen Speicher äußerst ineffizient. Eine bessere Möglichkeit wäre, den globalen Arbeitsspeicher vollständig zu überspringen und die Daten einfach direkt auf den Datenträger zu übertragen.

Um diese Probleme zu beheben, stellt COM zwei Datenstrukturen bereit: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) und [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1). Weitere Informationen finden Sie in den folgenden Themen:

-   [Die FORMATETC-Struktur](the-formatetc-structure.md)
-   [Die STGMEDIUM-Struktur](the-stgmedium-structure.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

 




