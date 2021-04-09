---
description: Die Connect-Methode des Merge-Objekts kann verwendet werden, um ein Modul mit einer zusätzlichen Funktion zu verbinden, die in der Datenbank zusammengeführt oder in der Datenbank zusammengeführt wird. Die Funktion muss vorhanden sein, bevor diese Methode aufgerufen wird.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Verbinden eines Mergemoduls mit mehreren Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867044"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a><span data-ttu-id="ff283-104">Verbinden eines Mergemoduls mit mehreren Features</span><span class="sxs-lookup"><span data-stu-id="ff283-104">Connecting a Merge Module to Multiple Features</span></span>

<span data-ttu-id="ff283-105">Die [**Connect**](merge-connect.md) -Methode des [Merge-Objekts](merge-object.md) kann verwendet werden, um ein Modul mit einer zusätzlichen Funktion zu verbinden, die in der Datenbank zusammengeführt oder in der Datenbank zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff283-105">The [**Connect**](merge-connect.md) method of the [Merge Object](merge-object.md) can be used to connect a module to an additional feature that has been merged into the database or that will be merged into the database.</span></span> <span data-ttu-id="ff283-106">Die Funktion muss vorhanden sein, bevor diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ff283-106">The feature must exist before calling this method.</span></span>

<span data-ttu-id="ff283-107">Ein Mergemodul sollte nie eine Komponente, die Systemdateien enthält, an das Haupt Feature einer Anwendung übermitteln, da dies dazu führen kann, dass das Installationsprogramm die Anwendung bei jeder Verwendung der Systemdatei überprüft und repariert.</span><span class="sxs-lookup"><span data-stu-id="ff283-107">A merge module should never deliver a component containing system files to the main feature of an application, because this may cause the Installer to validate and repair the application each time the system file is used.</span></span> <span data-ttu-id="ff283-108">Eine MSI-Datei, die Komponenten eines Mergemoduls akzeptieren soll, sollte so erstellt werden, dass alle Komponenten, die Systemdateien enthalten, nur zu Features gehören, die von der Hauptfunktion der Anwendung getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="ff283-108">A .msi file that is intended to accept components from a merge module should be authored so that any components that contain system files only belong to features that are separate from the main feature of the application.</span></span>

<span data-ttu-id="ff283-109">Wenn das Paket ein Mergemodul verwendet, das Systemdateien enthält, die alle Komponenten aus dem Mergemodul mit dem Haupt Feature der Anwendung verknüpfen, kann der Versuch, die Systemdatei zu verwenden, das Installationsprogramm veranlassen, das Haupt Feature der Anwendung zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="ff283-109">If your package uses a merge module containing system files that link all the components from the merge module to the main feature of the application, an attempt to use the system file may trigger the Installer to try and repair the main feature of the application.</span></span> <span data-ttu-id="ff283-110">Wenn die Hauptfunktion nicht repariert werden kann, tritt bei der Installation möglicherweise ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ff283-110">If the main feature cannot be repaired, the installation may fail.</span></span>

 

 



