---
description: Zum Ermitteln der Codepage einer Datenbank müssen Sie msidatabaseexport mit hDataBase auf das Handle der Datenbank und sztablename auf \_ forcecodepage festgelegt haben.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Festlegen der Codepage einer Installations Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866348"
---
# <a name="determining-an-installation-databases-code-page"></a><span data-ttu-id="8e58d-103">Festlegen der Codepage einer Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="8e58d-103">Determining an Installation Database's Code Page</span></span>

<span data-ttu-id="8e58d-104">Zum Ermitteln der Codepage einer Datenbank müssen Sie [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) mit *hDataBase* auf das Handle der Datenbank und *sztablename* auf \_ forcecodepage festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="8e58d-104">To determine the code page of a database, call [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) with *hDatabase* set to the handle of the database and *szTableName* set to \_ForceCodepage.</span></span> <span data-ttu-id="8e58d-105">Dadurch wird eine Textdatei mit der Erweiterung IDT exportiert.</span><span class="sxs-lookup"><span data-stu-id="8e58d-105">This exports a text file with an .idt extension.</span></span> <span data-ttu-id="8e58d-106">Die ersten beiden Zeilen dieser Datei sind leer.</span><span class="sxs-lookup"><span data-stu-id="8e58d-106">The first two lines of this file are blank.</span></span> <span data-ttu-id="8e58d-107">Die dritte Zeile ist die ANSI-Code Page Nummer, gefolgt von einer Registerkarte, gefolgt von dem Namen \_ forcecodepage.</span><span class="sxs-lookup"><span data-stu-id="8e58d-107">The third line is the ANSI code page number, followed by a tab, followed by the name \_ForceCodepage.</span></span> <span data-ttu-id="8e58d-108">Siehe auch [Code Page Behandlung importierter und exportierter Tabellen](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8e58d-108">See also [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="8e58d-109">Ein Beispiel für die Bestimmung der Codepage mithilfe der [**Export Methode**](database-export.md) wird im Windows Installer SDK als Teil des Hilfsprogramms WiLangId.vbs bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8e58d-109">An example of determining the code page by using the [**Export method**](database-export.md) is provided in the Windows Installer SDK as a part of the utility WiLangId.vbs.</span></span> <span data-ttu-id="8e58d-110">Weitere Informationen zum Verwenden von WiLangId.vbs finden Sie im Thema zum [Verwalten von Sprache und Codepage](manage-language-and-codepage.md).</span><span class="sxs-lookup"><span data-stu-id="8e58d-110">For more information about using WiLangId.vbs see the topic: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

 

 



