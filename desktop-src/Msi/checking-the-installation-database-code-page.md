---
description: Eine Codepage ist eine interne Tabelle, die vom Betriebssystem zum Zuordnen von Symbolen (Buchstaben, Ziffern und Interpunktions Zeichen) zu einer Zeichen Nummer verwendet wird.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Die Codepage der Installations Datenbank wird überprüft.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357515"
---
# <a name="checking-the-installation-database-code-page"></a>Die Codepage der Installations Datenbank wird überprüft.

Eine *Codepage* ist eine interne Tabelle, die vom Betriebssystem zum Zuordnen von Symbolen (Buchstaben, Ziffern und Interpunktions Zeichen) zu einer Zeichen Nummer verwendet wird. Unterschiedliche Codepages bieten Unterstützung für die in verschiedenen Ländern oder Regionen verwendeten Zeichensätze. Auf Codepages wird durch Number verwiesen. die Codepage 932 stellt z. b. den japanischen Zeichensatz dar, und die Codepage 950 stellt einen der chinesischen Zeichensätze dar. Eine Liste von ASCII-Codepages finden Sie [unter Lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) .

Die gleiche ASCII-Codepage, 1252, kann für Englisch und Französisch verwendet werden. Daher muss die Codepage für die Datenbank MNP2000.msi (Englisch) nicht zurückgesetzt werden, um die Installation auf Französisch zu ändern.

Weitere Informationen zum Festlegen der Codepage finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).

[Fortsetzen](importing-localized-error-and-actiontext-tables.md)

 

 



