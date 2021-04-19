---
description: Die \_ forcecodepage-Tabelle ist eine spezielle Tabelle zum Ändern der Codepage eines Installationspakets. Sie können die Codepage bestimmen oder festlegen, indem Sie eine Textarchiv Datei mit dem Namen \_ forcecodepage. IDT exportieren oder importieren.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367889"
---
# <a name="_forcecodepage"></a><span data-ttu-id="cdb07-104">\_Forcecodepage</span><span class="sxs-lookup"><span data-stu-id="cdb07-104">\_ForceCodepage</span></span>

<span data-ttu-id="cdb07-105">Die \_ forcecodepage-Tabelle ist eine spezielle Tabelle zum Ändern der Codepage eines Installationspakets.</span><span class="sxs-lookup"><span data-stu-id="cdb07-105">The \_ForceCodepage table is a special table used for changing the code page of an installation package.</span></span> <span data-ttu-id="cdb07-106">Sie können die Codepage bestimmen oder festlegen, indem Sie eine [Textarchiv Datei](text-archive-files.md) mit dem Namen \_ forcecodepage. IDT exportieren oder importieren.</span><span class="sxs-lookup"><span data-stu-id="cdb07-106">You can determine or set the code page by exporting or importing a [text archive file](text-archive-files.md) named \_ForceCodepage.idt.</span></span>

<span data-ttu-id="cdb07-107">Das Format der \_ forcecodepage-Tabelle ist 2 leere Zeilen, gefolgt von einer dritten Zeile, die die numerische Codepage angibt.</span><span class="sxs-lookup"><span data-stu-id="cdb07-107">The format of the \_ForceCodepage table is 2 blank lines followed by a third line that indicates the numeric code page.</span></span> <span data-ttu-id="cdb07-108">Beispielsweise würde eine \_ forcecodepage Table. IDT-Datei für eine japanische Datenbank wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-108">For example, a \_ForceCodepage table .idt file for a Japanese database would look as follows.</span></span> <span data-ttu-id="cdb07-109">Die numerische Codepage ist in diesem Fall 932.</span><span class="sxs-lookup"><span data-stu-id="cdb07-109">The numeric code page in this case is 932.</span></span>

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

<span data-ttu-id="cdb07-110">Weitere Informationen zur Verwendung \_ von forcecodepage zum Anzeigen oder Festlegen der Codepage einer Datenbank finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-110">For more information on how to use \_ForceCodepage to get or set the code page of a database see the following topics.</span></span>

-   [<span data-ttu-id="cdb07-111">Code Page Behandlung (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="cdb07-111">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
-   [<span data-ttu-id="cdb07-112">Festlegen der Codepage einer Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="cdb07-112">Determining an Installation Database's Code Page</span></span>](determining-an-installation-database-s-code-page.md)
-   [<span data-ttu-id="cdb07-113">Festlegen der Codepage einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="cdb07-113">Setting the Code Page of a Database</span></span>](setting-the-code-page-of-a-database.md)

<span data-ttu-id="cdb07-114">Die \_ forcecodepage-Tabelle ist eine spezielle Pseudo Tabelle, die zum Ändern der Codepage eines Installationspakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cdb07-114">The \_ForceCodepage table is a special pseudo table used for changing the code page of an installation package.</span></span> <span data-ttu-id="cdb07-115">Durch die Verwendung der \_ forcecodepage-Tabelle wird die-Datenbank auf die Codepage festgelegt, ohne dass eine Validierung durchgeführt wird, um zu überprüfen, ob die aktuell in der Datenbank vorhandenen Daten in die neue Codepage übersetzt werden</span><span class="sxs-lookup"><span data-stu-id="cdb07-115">Using the \_ForceCodepage table unconditionally sets the database to the code page without performing any validation as to whether the data currently in the database can be translated to the new code page.</span></span> <span data-ttu-id="cdb07-116">Es wird immer empfohlen, die Codepage einer Datenbank mit einer sprach neutralen Datenbank zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cdb07-116">It is always recommended that changing the code page of a database start with a language neutral database.</span></span>

 

 



