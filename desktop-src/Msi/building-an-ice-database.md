---
description: Nachdem Sie die entsprechenden ICES für die Validierung ausgewählt haben, muss ein Entwickler die benutzerdefinierten Aktionen in einer Ice-Datenbank zusammenfassen.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Aufbauen einer Ice-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864427"
---
# <a name="building-an-ice-database"></a><span data-ttu-id="79e17-103">Aufbauen einer Ice-Datenbank</span><span class="sxs-lookup"><span data-stu-id="79e17-103">Building an ICE Database</span></span>

<span data-ttu-id="79e17-104">Nachdem Sie die entsprechenden [ICES](internal-consistency-evaluators-ices.md) für die Validierung ausgewählt haben, muss ein Entwickler die benutzerdefinierten Aktionen in einer Ice-Datenbank zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="79e17-104">After selecting the appropriate [ICEs](internal-consistency-evaluators-ices.md) for validation, a developer must collect the custom actions together into an ICE database.</span></span> <span data-ttu-id="79e17-105">Eine CUB-Datei ist eine MSI-Standarddatenbank, die nur die ICES und die erforderlichen Tabellen enthält.</span><span class="sxs-lookup"><span data-stu-id="79e17-105">A .cub file is a standard .msi database that contains only ICEs and their required tables.</span></span> <span data-ttu-id="79e17-106">Eine CUB-Datei kann nicht installiert werden und wird nur zum Speichern und Bereitstellen des Zugriffs auf benutzerdefinierte Ice-Aktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="79e17-106">A .cub file cannot be installed and is used only to store and provide access to ICE custom actions.</span></span>

<span data-ttu-id="79e17-107">Eine CUB-Datei enthält die folgenden Datenbanktabellen.</span><span class="sxs-lookup"><span data-stu-id="79e17-107">A .cub file contains the following database tables.</span></span>



| <span data-ttu-id="79e17-108">Tabelle</span><span class="sxs-lookup"><span data-stu-id="79e17-108">Table</span></span>                                  | <span data-ttu-id="79e17-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e17-109">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79e17-110">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="79e17-110">Binary</span></span>](binary-table.md)             | <span data-ttu-id="79e17-111">Die Skriptdateien, DLLs und EXEs der ICE-Zoll-Aktionen, auf die in der Tabelle "CustomAction" verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="79e17-111">The script files, DLLs, and EXEs of the ICE customs actions that are referenced in the CustomAction table.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="79e17-112">CustomAction</span><span class="sxs-lookup"><span data-stu-id="79e17-112">CustomAction</span></span>](customaction-table.md) | <span data-ttu-id="79e17-113">Jeder Datensatz in dieser Tabelle entspricht einer benutzerdefinierten Ice-Aktion, die in der CUB-Datei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="79e17-113">Each record in this table corresponds to an ICE custom action included in the .cub file.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="79e17-114">\_Icesequence</span><span class="sxs-lookup"><span data-stu-id="79e17-114">\_ICESequence</span></span>                          | <span data-ttu-id="79e17-115">In dieser Tabelle sind die Ice-Zoll-Aktionen aufgeführt, die in der CUB-Datei in ihrer Ausführungssequenz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="79e17-115">This table lists the ICE customs actions included in the .cub file in their execution sequence.</span></span> <span data-ttu-id="79e17-116">Die in dieser Tabelle aufgeführten benutzerdefinierten Eis Aktionen werden durch Aufrufen von " [**msisequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)" oder einzeln mithilfe von " [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79e17-116">The ICE custom actions listed in this table are executed by calling [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), or individually executed using [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> |
| [<span data-ttu-id="79e17-117">\_Überprüfen</span><span class="sxs-lookup"><span data-stu-id="79e17-117">\_Validation</span></span>](-validation-table.md)  | <span data-ttu-id="79e17-118">Diese Tabelle enthält die CUB-Datei Einträge, die in der Validierungs Tabelle zusammengeführt werden sollen \_ .</span><span class="sxs-lookup"><span data-stu-id="79e17-118">This table contains the .cub file entries that are to be merged into the \_Validation table.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="79e17-119">\_Sonderfunktionen</span><span class="sxs-lookup"><span data-stu-id="79e17-119">\_Special</span></span>                              | <span data-ttu-id="79e17-120">Alle speziellen Verarbeitungs Tabellen, die für bestimmte benutzerdefinierte Ice-Aktionen erforderlich sind, müssen in der CUB-Datei enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="79e17-120">Any special processing tables required by particular ICE custom actions must be included in the .cub file.</span></span> <span data-ttu-id="79e17-121">Der Name dieser Tabellen muss einen führenden Unterstrich aufweisen.</span><span class="sxs-lookup"><span data-stu-id="79e17-121">The name of these tables must have a leading underscore.</span></span>                                                                                                        |



 

<span data-ttu-id="79e17-122">Weitere Informationen finden Sie unter [Sample. CUB-Datei](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="79e17-122">See [Sample .cub File](sample--cub-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79e17-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79e17-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79e17-124">Aufbauen eines Eis</span><span class="sxs-lookup"><span data-stu-id="79e17-124">Building An ICE</span></span>](building-an-ice.md)
</dt> </dl>

 

 



