---
description: In der folgenden Liste sind die TAPI-MSP-Entwurfs Ziele enthalten.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Allgemeine Entwurfs Ziele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345154"
---
# <a name="general-design-goals"></a>Allgemeine Entwurfs Ziele

In der folgenden Liste sind die TAPI-MSP-Entwurfs Ziele enthalten.

-   Basisklassen wurden einfach gehalten, wobei Member und Methoden nur bei Bedarf eingeführt wurden.
-   Einfache Vererbung. Keine mehrfache Vererbung zwischen Klassen, obwohl mehrere Vererbung für die Schnittstellen verwendet wird.
-   Das Sperren erfolgt nur in einer Richtung, um einen Deadlock zu verhindern. Methoden für das-Objekt, die die Sperre des Aufrufes erfordern, können Methoden für den Stream aufzurufen, die die Sperre für den Stream erfordern. Methoden im Datenstrom, die die Sperre für den Stream erfordern, werden jedoch nie eine Methode für den-Befehl aufruft, der eine Sperre für den-Befehl erfordert.
-   RefCounts werden verwendet, um den Zugriff zu schützen. Alle Rückrufe, die an den Thread Pool gesendet werden, enthalten refCounts. Der Ref count wird abgebrochen, wenn der Warte Vorgang abgebrochen wird. Das Adress Objekt hat eine Ref-Anzahl an Terminals. Calltobjekte haben refcount für die Adresse und für Datenströme. Stream-Objekte haben rebcounts bei aufrufen und Terminals. Die Terminals haben Ref-Werte für Streams. Die zirkuläre refCounts unterbrechen, wenn die Shutdown-Methode für die Address-und calltobjekte aufgerufen wird.

 

 



