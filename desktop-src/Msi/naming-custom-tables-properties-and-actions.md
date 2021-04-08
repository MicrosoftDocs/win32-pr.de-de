---
description: Paket Ersteller sollten sicherstellen, dass die Namen von benutzerdefinierten Tabellen, Eigenschaften oder Aktionen, die in Ihrem Paket definiert sind, nicht mit den Namen von Standard Tabellen,-Eigenschaften oder-Aktionen in Konflikt stehen, die für die Windows Installer System eigen sind.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864083"
---
# <a name="naming-custom-tables-properties-and-actions"></a><span data-ttu-id="71f60-103">Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen</span><span class="sxs-lookup"><span data-stu-id="71f60-103">Naming Custom Tables, Properties, and Actions</span></span>

<span data-ttu-id="71f60-104">Paket Ersteller sollten sicherstellen, dass die Namen von benutzerdefinierten Tabellen, Eigenschaften oder Aktionen, die in Ihrem Paket definiert sind, nicht mit den Namen von Standard Tabellen,-Eigenschaften oder-Aktionen in Konflikt stehen, die für die Windows Installer System eigen sind.</span><span class="sxs-lookup"><span data-stu-id="71f60-104">Package authors should ensure that the names of any custom tables, properties, or actions defined in their package will not conflict with the names of standard tables, properties, or actions that are native to the Windows Installer.</span></span>

<span data-ttu-id="71f60-105">Paket Autoren sollten die folgenden Richtlinien für benutzerdefinierte Tabellen-, Eigenschafts-oder Aktions Namen einhalten.</span><span class="sxs-lookup"><span data-stu-id="71f60-105">Package authors should adhere to the following guidelines for custom table, property, or action names.</span></span>

-   <span data-ttu-id="71f60-106">Geben Sie Namen für benutzerdefinierte Tabellen, Eigenschaften oder Aktionen mit einem Präfix an, das Ihre Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="71f60-106">Make names for custom tables, properties, or actions that have a prefix that identifies your application.</span></span>
-   <span data-ttu-id="71f60-107">Verwenden Sie niemals einen Namen mit MSI als Präfix.</span><span class="sxs-lookup"><span data-stu-id="71f60-107">Never use a name with Msi as the prefix.</span></span> <span data-ttu-id="71f60-108">Ab Windows Installer 2,0 werden allen neuen systemeigenen Windows Installer Eigenschaften, Aktionen und Tabellennamen mit dem Präfix MSI zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="71f60-108">Starting with Windows Installer 2.0, all new native Windows Installer properties, actions, and tables are given names prefixed by Msi.</span></span> <span data-ttu-id="71f60-109">Bei diesem Präfix wird die Groß-/Kleinschreibung nicht beachtet, z.b. msinewinternaltable.</span><span class="sxs-lookup"><span data-stu-id="71f60-109">This prefix is not case sensitive, for example MsiNewInternalTable.</span></span> <span data-ttu-id="71f60-110">Da die Groß-/Kleinschreibung nicht beachtet wird, sollten Autoren alle Fälle des MSI-Präfixes vermeiden.</span><span class="sxs-lookup"><span data-stu-id="71f60-110">Because the prefix is not case sensitive, authors should avoid all cases of the Msi prefix.</span></span>

<span data-ttu-id="71f60-111">Weitere Informationen finden Sie unter [Tabellennamen](table-names.md).</span><span class="sxs-lookup"><span data-stu-id="71f60-111">For more information, see [Table Names](table-names.md).</span></span>

 

 



