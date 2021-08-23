---
title: Eingebettete Objekte (COM)
description: Eingebettete Objekte
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df671850dc167a0751f69cbc57f8c19698db06a0454dd6283553c4d8ffa1609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048358"
---
# <a name="embedded-objects-com"></a>Eingebettete Objekte (COM)

Ein eingebettetes Objekt wird zusammen mit allen Informationen, die zum Verwalten des Objekts erforderlich sind, physisch im Verbunddokument gespeichert. Das heißt, das eingebettete Objekt ist tatsächlich ein Teil des Verbunddokuments, in dem es sich befindet. Diese Anordnung hat einige Nachteile. Erstens ist ein zusammengesetztes Dokument, das eingebettete Objekte enthält, größer als ein Dokument, das die gleichen Objekte wie Links enthält. Zweitens werden Änderungen, die an der Quelle eines eingebetteten Objekts vorgenommen wurden, nicht automatisch in der eingebetteten Kopie repliziert, und Änderungen in der eingebetteten Kopie werden nicht in der Quelle widergespiegelt, da sie sich über einen Link befinden.

Für bestimmte Zwecke bietet das Einbetten jedoch mehrere Vorteile gegenüber Links. Erstens können Benutzer Verbunddokumente mit eingebetteten Objekten auf andere Computer oder andere Speicherorte auf demselben Computer übertragen, ohne einen Link zu unterbricht. Zweitens können Benutzer eingebettete Objekte bearbeiten, ohne den Inhalt des Originals zu ändern. Manchmal ist diese Trennung genau das, was erforderlich ist. Drittens können eingebettete Objekte an Ort und Stelle aktiviert werden, was bedeutet, dass der Benutzer das Objekt bearbeiten oder anderweitig bearbeiten kann, ohne in einem anderen Fenster als dem des Objekts arbeiten zu müssen. Wenn das Objekt aktiviert wird, ändert sich stattdessen die Benutzeroberfläche der Containeranwendung, um die Tools verfügbar zu machen, die zum Verwalten oder Ändern des Objekts erforderlich sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen verknüpfter und eingebetteter Objekte aus vorhandenen Daten](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




