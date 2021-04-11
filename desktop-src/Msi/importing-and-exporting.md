---
description: Mit dem Installationsprogramm können Sie ein Textarchiv in eine aktive Datenbank importieren und eine Datenbankdatei in ein Textarchiv exportieren. Dies kann für textbasierte Quell Code Verwaltungssysteme nützlich sein.
ms.assetid: 1025da16-9e1f-4fb4-9ce1-f992970eb903
title: Importieren und Exportieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb778f4a0fe415686c80f2609f63958ae042d920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130445"
---
# <a name="importing-and-exporting"></a><span data-ttu-id="e6c89-104">Importieren und Exportieren</span><span class="sxs-lookup"><span data-stu-id="e6c89-104">Importing and Exporting</span></span>

<span data-ttu-id="e6c89-105">Mit dem Installationsprogramm können Sie ein Textarchiv in eine aktive Datenbank importieren und eine Datenbankdatei in ein Textarchiv exportieren.</span><span class="sxs-lookup"><span data-stu-id="e6c89-105">You can use the installer to import a text archive into an active database as well as to export a database file to a text archive.</span></span> <span data-ttu-id="e6c89-106">Dies kann für textbasierte Quell Code Verwaltungssysteme nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="e6c89-106">This can be useful for text-based source control systems.</span></span>

<span data-ttu-id="e6c89-107">Um ein Textarchiv in eine aktive Datenbank zu importieren, müssen Sie die Funktion [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) abrufen.</span><span class="sxs-lookup"><span data-stu-id="e6c89-107">To import a text archive into an active database, call the [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) function.</span></span>

<span data-ttu-id="e6c89-108">Wenn Sie eine Datenbankdatei in ein Textarchiv exportieren möchten, müssen Sie die Funktion [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) anrufen.</span><span class="sxs-lookup"><span data-stu-id="e6c89-108">To export a database file to a text archive, call the [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) function.</span></span>

 

 



