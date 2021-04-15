---
description: Standardmäßig verwendet die Erkennung ein System Wörterbuch, das alle häufig geschriebenen Wörter in einer Sprache enthält.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Anwendungs Wörterbücher verwenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484787"
---
# <a name="using-application-dictionaries"></a>Anwendungs Wörterbücher verwenden

Standardmäßig verwendet die Erkennung ein System Wörterbuch, das alle häufig geschriebenen Wörter in einer Sprache enthält. Außerdem verfügt die Erkennung über ein Benutzerwörterbuch, das Wörter enthält, die der Benutzer dem Wörterbuch hinzugefügt hat. Benutzer fügen dem Benutzerwörterbuch über den Tablet PC-Eingabebereich ein Wort hinzu, indem Sie Folgendes auswählen:

-   Die Alternative Liste (beim Schreiben).
-   Das Sprach Tools-Menü (bei der Sprache).

Wenn Sie eine Anwendung entwerfen, in die Sie erwarten, dass der Benutzer Wörter schreibt, die nicht im System Wörterbuch oder im Benutzerwörterbuch gefunden werden, erstellen Sie ein Anwendungs Wörterbuch. Ein Anwendungs Wörterbuch verbessert die Erkennungsgenauigkeit weiter, indem dem Erkennungs Modul eine zusätzliche angepasste Liste von Wörtern bereitgestellt wird, die wahrscheinlich als Handschrift in eine Anwendung eingegeben werden.

Sie erstellen ein Anwendungs Wörterbuch mit dem [**WordList**](inkwordlist-class.md) -Objekt. Das resultierende Anwendungs Wörterbuch erhöht die Erkennungsgenauigkeit, indem der Erkennungs Modul eine Liste erwarteter Wörter bereitgestellt wird. Beispielsweise erhöht ein Anwendungs Wörterbuch, das die medizinische Terminologie enthält, die Erkennungsgenauigkeit innerhalb einer Anwendung, die für die medizinische Branche entwickelt wurde, in die die Begriffe wahrscheinlich geschrieben werden.

Ein weiteres Beispiel: Wenn Sie ein Formular für jemanden zum Sortieren von Musikinstrumenten entwerfen, erstellen Sie ein [**WordList**](inkwordlist-class.md) -Objekt, das die Namen der am häufigsten erstellten Instrumentations Hersteller enthält. Legen Sie die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts auf das von Ihnen erstellte **WordList** -Objekt fest. Diese Liste von Wörtern wird dann vom **erkenzercontext** -Objekt an die Erkennung weitergegeben. Das Anwendungs Wörterbuch erhöht die Erkennungsgenauigkeit, wenn diese Namen in einem Feld in der Anwendung geschrieben werden.

In den folgenden Themen wird die Verwendung von Anwendungs Wörterbüchern beschrieben.

-   [Grundlegendes zu Wortlisten, Erkennungs Kontext und Faktoiden](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Verwenden von Anwendungs Wörterbüchern mit den Tablet PC Platform-APIs](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Erstellen benutzerdefinierter Wörterbücher für die Handschrifterkennung](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



