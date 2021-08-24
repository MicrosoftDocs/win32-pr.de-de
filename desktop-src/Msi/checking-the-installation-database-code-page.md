---
description: Eine Codepage ist eine interne Tabelle, die das Betriebssystem zum Zuordnen von Symbolen (Buchstaben, Ziffern und Interpunktionszeichen) zu einer Zeichennummer verwendet.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Überprüfen der Codepage der Installationsdatenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedb63128d4a3b18878eba16af5e55da92403953ddf2a2c9a29c788a524ad41f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581770"
---
# <a name="checking-the-installation-database-code-page"></a>Überprüfen der Codepage der Installationsdatenbank

Eine *Codepage* ist eine interne Tabelle, die das Betriebssystem zum Zuordnen von Symbolen (Buchstaben, Ziffern und Interpunktionszeichen) zu einer Zeichennummer verwendet. Verschiedene Codepages bieten Unterstützung für die Zeichensätze, die in verschiedenen Ländern oder Regionen verwendet werden. Auf Codepages wird anhand der Zahl verwiesen. Die Codepage 932 stellt beispielsweise den japanischen Zeichensatz und die Codepage 950 einen der chinesischen Zeichensätze dar. Eine Liste der ASCII-Codepages finden Sie unter Lokalisieren der [Fehler- und ActionText-Tabellen.](localizing-the-error-and-actiontext-tables.md)

Die gleiche ASCII-Codepage 1252 kann für Englisch und Französisch verwendet werden. Daher muss die Codepage für die Datenbank MNP2000.msi (Englisch) nicht zurückgesetzt werden, um die Installation in Französisch zu ändern.

Weitere Informationen zum Festlegen der Codepage finden Sie unter [Codepagebehandlung (Windows Installer).](code-page-handling-windows-installer-.md)

[Fortsetzen](importing-localized-error-and-actiontext-tables.md)

 

 



