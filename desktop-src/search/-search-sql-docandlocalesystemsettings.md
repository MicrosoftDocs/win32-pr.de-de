---
description: Wenn das Betriebssystem oder sogar eine Anwendung auf die Verwendung einer bestimmten Sprache und eines bestimmten Locale festgelegt ist, sind viele Einstellungen betroffen.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Dokument- und System-Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed43ae52d7626b759563069b05fe4ae03649feb63fd1af8dab1b80cfd4d558a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594780"
---
# <a name="document-and-system-locale-settings"></a>Dokument- und System-Einstellungen

Wenn das Betriebssystem oder sogar eine Anwendung auf die Verwendung einer bestimmten Sprache und eines bestimmten Locale festgelegt ist, sind viele Einstellungen betroffen. Diese Einstellungen umfassen numerisches Format, Datumsformat, Währungsformat, Groß- und Kleinbuchstabenzuordnung, Wörterbuchsortierreihenfolge, Tokenisierung und andere. Obwohl diese Einstellungen dazu beitragen Windows die Suche eine hervorragende lokalisierte Unterstützung zu bieten, können unerwartete Ergebnisse auftreten, wenn Dokumente aus einem Bestimmten mithilfe eines Systems durchsucht werden, das auf ein anderes Locale festgelegt ist.

Wenn das [**IFilter-Objekt**](/windows/win32/api/filter/nn-filter-ifilter) die Texteigenschaften und den Inhalt eines Dokuments verarbeitet, meldet es die Sprache dieses Dokuments an den Inhaltsindexer. Mithilfe dieser Informationen Windows Die Suche kann die entsprechende Wörter wörterbrechend anwenden.

 

 
