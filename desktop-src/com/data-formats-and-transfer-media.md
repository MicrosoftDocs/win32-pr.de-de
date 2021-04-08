---
title: Datenformate und Übertragungsmedien
description: Datenformate und Übertragungsmedien
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104039829"
---
# <a name="data-formats-and-transfer-media"></a>Datenformate und Übertragungsmedien

Die meisten Plattformen, einschließlich Windows, definieren ein Standardprotokoll für die Übertragung von Daten zwischen Anwendungen, basierend auf einem Satz von Funktionen, die als Zwischenablage bezeichnet werden. Anwendungen, die diese Funktionen verwenden, können Daten freigeben, auch wenn Ihre nativen Datenformate stark voneinander abweichen. Im Allgemeinen haben diese zwischen Ablagen zwei bedeutende Mängel, die com überwunden hat.

Zuerst verwenden Daten Beschreibungen nur einen Format Bezeichner, z. b. den einzelnen 16-Bit-Format Bezeichner für die Zwischenablage unter Windows. Dies bedeutet, dass die Zwischenablage nur die Struktur Ihrer Daten beschreiben kann, d. h. die Reihenfolge der Bits. Es kann berichtet werden: "Ich verfüge über eine Bitmap", oder ich habe Text, aber es kann nicht die Zielgeräte angeben, für die die Daten erstellt werden, welche Sichten oder Aspekte selbst die Daten bereitstellen können oder welche Speichermedien am besten für die Übertragung geeignet sind. Beispielsweise kann nicht berichtet werden: "Ich habe eine Text Zeichenfolge, die im globalen Speicher gespeichert ist und für die Präsentation entweder auf dem Bildschirm oder auf einem Drucker formatiert ist." oder "Ich habe eine Miniaturansicht der Miniaturansicht für einen 100 dpi-Punkt-Matrix-Drucker gerendert und als Datenträger Datei gespeichert."

Zweitens erfolgen alle Datenübertragungen, die die Zwischenablage verwenden, im Allgemeinen durch globalen Speicher. Die Verwendung des globalen Speichers ist für kleine Datenmengen, aber erschreckend ineffizient für große Mengen, z. b. ein Multimediaobjekt von 20 MB, ausreichend effizient. Der globale Arbeitsspeicher ist bei einem großen Datenobjekt langsam, dessen Größe einen beträchtlichen Austausch in den virtuellen Arbeitsspeicher auf dem Datenträger erfordert. In Fällen, in denen sich die ausgetauschten Daten größtenteils auf dem Datenträger befinden, ist das Erzwingen dieses virtuellen Arbeitsspeichers äußerst ineffizient. Eine bessere Möglichkeit würde den globalen Speicher vollständig überspringen und die Daten einfach direkt auf den Datenträger übertragen.

Um diese Probleme zu beheben, stellt com zwei Datenstrukturen bereit: [**formatusw**](/windows/win32/api/objidl/ns-objidl-formatetc) . und [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1). Weitere Informationen finden Sie unter den folgenden Themen:

-   [Die FORMATETC-Struktur](the-formatetc-structure.md)
-   [Die STGMEDIUM-Struktur](the-stgmedium-structure.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

 




