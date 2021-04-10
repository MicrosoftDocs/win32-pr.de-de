---
title: Eingebettete Objekte (com)
description: Eingebettete Objekte
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102691"
---
# <a name="embedded-objects-com"></a>Eingebettete Objekte (com)

Ein eingebettetes Objekt wird physisch im Verbund Dokument gespeichert, zusammen mit allen Informationen, die für die Verwaltung des Objekts benötigt werden. Das heißt, dass das eingebettete Objekt tatsächlich Teil des Verbund Dokuments ist, in dem es sich befindet. Diese Anordnung hat einige Nachteile. Zuerst ist ein zusammengesetztes Dokument mit eingebetteten Objekten größer als eins, das die gleichen Objekte wie Verknüpfungen enthält. Zweitens werden Änderungen, die an der Quelle eines eingebetteten Objekts vorgenommen werden, nicht automatisch in der eingebetteten Kopie repliziert, und Änderungen in der eingebetteten Kopie werden nicht in der Quelle übernommen, wie Sie es bei einem Link gibt.

Für bestimmte Zwecke bietet Einbettungen aber mehrere Vorteile gegenüber Links. Zunächst können die Benutzer zusammengesetzte Dokumente mit eingebetteten Objekten auf andere Computer oder an andere Speicherorte auf demselben Computer übertragen, ohne einen Link zu unterbrechen. Zweitens können Benutzer eingebettete Objekte bearbeiten, ohne den Inhalt des Originals zu ändern. Manchmal ist diese Trennung genau das, was erforderlich ist. Drittens können eingebettete Objekte direkt aktiviert werden. Dies bedeutet, dass der Benutzer das Objekt bearbeiten oder anderweitig bearbeiten kann, ohne in einem separaten Fenster von dem Container des Objekts arbeiten zu müssen. Wenn das Objekt aktiviert ist, wird stattdessen die Benutzeroberfläche der Containeranwendung geändert, um die Tools verfügbar zu machen, die zum Verwalten oder Ändern des Objekts erforderlich sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




