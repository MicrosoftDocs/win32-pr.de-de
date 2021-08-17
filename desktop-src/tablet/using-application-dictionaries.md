---
description: Standardmäßig verwendet die Recognizer ein Systemwörterbuch, das alle häufig geschriebenen Wörter in einer Sprache enthält.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Verwenden von Anwendungswörterbüchern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c83013f704fe28b5754ab89fd95ed730e16d1cda5ab257d4fb411d0e7293347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449232"
---
# <a name="using-application-dictionaries"></a>Verwenden von Anwendungswörterbüchern

Standardmäßig verwendet die Recognizer ein Systemwörterbuch, das alle häufig geschriebenen Wörter in einer Sprache enthält. Darüber hinaus verfügt die -Erkannt über ein Benutzerwörterbuch, das Wörter enthält, die der Benutzer dem Wörterbuch hinzugefügt hat. Benutzer fügen dem Benutzerwörterbuch über den Eingabebereich des Tablet-PCs ein Wort hinzu, und klicken dabei auf die folgenden Auswahlen:

-   Die alternative Liste (beim Schreiben).
-   Das Menü "Sprachtools" (beim Sprechen).

Wenn Sie eine Anwendung entwerfen, in die Sie erwarten, dass der Benutzer Wörter schreibt, die weder im Systemverzeichnis noch im Benutzerwörterbuch gefunden werden, erstellen Sie ein Anwendungswörterbuch. Ein Anwendungswörterbuch verbessert die Erkennungsgenauigkeit weiter, indem es der Erkennung eine zusätzliche benutzerdefinierte Liste von Wörtern zur Verfügung stellt, die wahrscheinlich als Handschrift in eine Anwendung eingegeben werden.

Sie erstellen ein Anwendungswörterbuch mithilfe des [**WordList-Objekts.**](inkwordlist-class.md) Das nachfolgende Anwendungswörterbuch erhöht die Erkennungsgenauigkeit, indem es der Erkennung eine Liste der erwarteten Wörter zur Verfügung stellt. Beispielsweise erhöht ein Anwendungswörterbuch, das medizinische Terminologie enthält, die Erkennungsgenauigkeit innerhalb einer Anwendung, die für die medizinische Branche entwickelt wurde, in die die Begriffe wahrscheinlich geschrieben werden.

Ein weiteres Beispiel: Wenn Sie ein Formular entwerfen, in dem jemand Musikinstrument bestellen kann, erstellen Sie ein [**WordList-Objekt,**](inkwordlist-class.md) das die Namen der gängigsten Instrumenthersteller enthält. Legen Sie [**die WordList-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) des [**RecognizerContext-Objekts**](inkrecognizercontext-class.md) auf das **wordList-Objekt** fest, das Sie erstellt haben. Diese Liste von Wörtern wird dann vom RecognizerContext-Objekt an die **Recognizer-Klasse** übergeben. Das Anwendungswörterbuch erhöht die Erkennungsgenauigkeit, wenn diese Namen in ein Feld in der Anwendung geschrieben werden.

In den folgenden Themen wird die Verwendung von Anwendungswörterbüchern beschrieben.

-   [Grundlegendes zu Wortlisten, Kontext der Wiedererkennung und Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Verwenden von Anwendungswörterbüchern mit den Plattform-APIs für Tablet-PCs](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Erstellen benutzerdefinierter Wörterbücher für die Handschrifterkennung](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



