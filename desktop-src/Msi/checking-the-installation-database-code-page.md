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
# <a name="checking-the-installation-database-code-page"></a><span data-ttu-id="29523-103">Die Codepage der Installations Datenbank wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="29523-103">Checking the Installation Database Code Page</span></span>

<span data-ttu-id="29523-104">Eine *Codepage* ist eine interne Tabelle, die vom Betriebssystem zum Zuordnen von Symbolen (Buchstaben, Ziffern und Interpunktions Zeichen) zu einer Zeichen Nummer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29523-104">A *code page* is an internal table that the operating system uses to map symbols (letters, numerals, and punctuation characters) to a character number.</span></span> <span data-ttu-id="29523-105">Unterschiedliche Codepages bieten Unterstützung für die in verschiedenen Ländern oder Regionen verwendeten Zeichensätze.</span><span class="sxs-lookup"><span data-stu-id="29523-105">Different code pages provide support for the character sets used in different countries or regions.</span></span> <span data-ttu-id="29523-106">Auf Codepages wird durch Number verwiesen. die Codepage 932 stellt z. b. den japanischen Zeichensatz dar, und die Codepage 950 stellt einen der chinesischen Zeichensätze dar.</span><span class="sxs-lookup"><span data-stu-id="29523-106">Code pages are referred to by number; for example, code page 932 represents the Japanese character set, and code page 950 represents one of the Chinese character sets.</span></span> <span data-ttu-id="29523-107">Eine Liste von ASCII-Codepages finden Sie [unter Lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) .</span><span class="sxs-lookup"><span data-stu-id="29523-107">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of ASCII code pages.</span></span>

<span data-ttu-id="29523-108">Die gleiche ASCII-Codepage, 1252, kann für Englisch und Französisch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29523-108">The same ASCII code page, 1252, may be used for English and French.</span></span> <span data-ttu-id="29523-109">Daher muss die Codepage für die Datenbank MNP2000.msi (Englisch) nicht zurückgesetzt werden, um die Installation auf Französisch zu ändern.</span><span class="sxs-lookup"><span data-stu-id="29523-109">Therefore the code page for the database MNP2000.msi (English) does not need to be reset to change the installation to French.</span></span>

<span data-ttu-id="29523-110">Weitere Informationen zum Festlegen der Codepage finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="29523-110">For more information about setting the code page see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

[<span data-ttu-id="29523-111">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="29523-111">Continue</span></span>](importing-localized-error-and-actiontext-tables.md)

 

 



