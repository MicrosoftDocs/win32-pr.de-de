---
description: Mergemodule sind im wesentlichen vereinfachte MSI-Dateien, bei denen es sich um die Dateinamenerweiterung für ein Windows Installer Installationspaket handelt. Ein Standard-Mergemodul verfügt über die Dateinamenerweiterung. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Informationen zu Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345169"
---
# <a name="about-merge-modules"></a><span data-ttu-id="b86f6-104">Informationen zu Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="b86f6-104">About Merge Modules</span></span>

<span data-ttu-id="b86f6-105">Mergemodule sind im wesentlichen vereinfachte MSI-Dateien, bei denen es sich um die Dateinamenerweiterung für ein Windows Installer Installationspaket handelt.</span><span class="sxs-lookup"><span data-stu-id="b86f6-105">Merge modules are essentially simplified .msi files, which is the file name extension for a Windows Installer installation package.</span></span> <span data-ttu-id="b86f6-106">Ein Standard-Mergemodul verfügt über die Dateinamenerweiterung. msm.</span><span class="sxs-lookup"><span data-stu-id="b86f6-106">A standard merge module has an .msm file name extension.</span></span>

<span data-ttu-id="b86f6-107">Ein Mergemodul kann nicht allein installiert werden, da es einige wichtige Datenbanktabellen enthält, die in einer Installations Datenbank vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b86f6-107">A merge module cannot be installed alone because its lacks some vital database tables that are present in an installation database.</span></span> <span data-ttu-id="b86f6-108">Mergemodule enthalten auch zusätzliche Tabellen, die für sich selbst eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="b86f6-108">Merge modules also contain additional tables that are unique to themselves.</span></span> <span data-ttu-id="b86f6-109">Um die von einem Mergemodul übermittelten Informationen mit einer Anwendung zu installieren, muss das Modul zuerst in der MSI-Datei der Anwendung zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b86f6-109">To install the information delivered by a merge module with an application, the module must first be merged into the application's .msi file.</span></span>

<span data-ttu-id="b86f6-110">Ein Mergemodul besteht aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="b86f6-110">A merge module consists of the following parts:</span></span>

-   <span data-ttu-id="b86f6-111">Eine [mergemoduldatenbank](merge-module-database.md) mit den Installations Eigenschaften und der Setup Logik, die vom Mergemodul übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="b86f6-111">A [Merge Module Database](merge-module-database.md) containing the installation properties and setup logic being delivered by the merge module.</span></span>
-   <span data-ttu-id="b86f6-112">Ein [Zusammenfassungs Daten-Datenstrom Verweis für Zusammenfassungs Module](merge-module-summary-information-stream-reference.md) , der das Modul</span><span class="sxs-lookup"><span data-stu-id="b86f6-112">A [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md) describing the module.</span></span>
-   <span data-ttu-id="b86f6-113">Eine [MergeModule.CABinet](mergemodule-cabinet.md) -CAB-Datei, die als Stream innerhalb des Mergemoduls gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b86f6-113">A [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file stored as a stream inside the merge module.</span></span> <span data-ttu-id="b86f6-114">Diese CAB-Datei enthält alle Dateien, die von den vom Mergemodul gelieferten Komponenten benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="b86f6-114">This cabinet contains all the files required by the components delivered by the merge module.</span></span>

<span data-ttu-id="b86f6-115">[Mehrere Language Merge-Module](multiple-language-merge-modules.md) können Komponenten an ein Installationspaket in mehreren Sprachen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b86f6-115">[Multiple language merge modules](multiple-language-merge-modules.md) can deliver components to an installation package in multiple languages.</span></span> <span data-ttu-id="b86f6-116">In einem Mergemodul mit mehreren Sprachen enthält die Datenbank die Installations Eigenschaften und die Logik für mehr als eine Sprache. das MergeModule.CABinet-CAB enthält alle Dateien, die zum Installieren von Komponenten mit allen vom Modul unterstützten Sprachen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b86f6-116">In a multiple language merge module the database contains the installation properties and logic for more than one language and the MergeModule.CABinet cabinet includes all the files necessary to install components with all the languages supported by the module.</span></span>

 

 



