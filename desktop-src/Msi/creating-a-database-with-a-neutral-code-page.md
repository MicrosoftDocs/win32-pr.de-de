---
description: Der empfohlene Ansatz für die Verarbeitung von Codepages besteht im Erstellen einer neutralen Basisdatenbank, die nur Zeichen enthält, die in eine beliebige Codepage übersetzt werden können.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Erstellen einer Datenbank mit einer neutralen Codepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e9283378d003adf3069e2feb505fab36c9a379de4deb2a767d10559d547e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379415"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Erstellen einer Datenbank mit einer neutralen Codepage

Der empfohlene Ansatz für die Verarbeitung von Codepages besteht im Erstellen einer neutralen Basisdatenbank, die nur Zeichen enthält, die in eine beliebige Codepage übersetzt werden können. Die Datenbank kann dann auf die Codepage der Lokalisierung festgelegt werden, und die Lokalisierungsinformationen können hinzugefügt werden, wie unter Lokalisieren eines Windows [Installer-Pakets beschrieben.](localizing-a-windows-installer-package.md)

Um eine neutrale Datenbank zu erstellen, vermeiden Sie Erweiterte Zeichen, die nicht zum ASCII-Zeichensatz gehören und daher eine spezielle Codepage erfordern. Beispielsweise sind das Copyrightzeichen, © und das registrierte Markenzeichen, , keine ASCII-Zeichen und erfordern eine spezielle ANSI-Codepage für die ordnungsgemäße Anzeige. Verwenden Sie stattdessen (c) und (r), da diese Zeichen übersetzt oder in die Symbole für die englischsprachige Version transformiert werden können. Diese neutrale Datenbank kann dann lokalisiert werden, indem ihre Codepage und Lokalisierungsinformationen durch Tabellenbearbeitung oder durch Importieren von Textarchivdateien hinzugefügt werden.

 

 



