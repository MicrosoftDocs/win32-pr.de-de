---
description: Windows Installer Entwickler können Tools erstellen, die es Endbenutzern ermöglichen, konfigurierbare Mergemodule zu verwenden.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Hinzufügen von Modul Konfigurationsfunktionen zu einem Mergetool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756253"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a><span data-ttu-id="3492c-103">Hinzufügen von Modul Konfigurationsfunktionen zu einem Mergetool</span><span class="sxs-lookup"><span data-stu-id="3492c-103">Adding Module Configuration Capability to a Merge Tool</span></span>

<span data-ttu-id="3492c-104">Damit Endbenutzer konfigurierbare Mergemodule verwenden können, können Sie Merge-und Konfigurationstools erstellen, um folgende Aufgaben durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="3492c-104">To enable end users to use configurable merge modules, you can author merge and configuration tools to do the following:</span></span>

-   <span data-ttu-id="3492c-105">Merge-Tools sollten die Funktionen in Mergemod.dll Version 2,0 zum Zusammenführen des Moduls aufruft.</span><span class="sxs-lookup"><span data-stu-id="3492c-105">Merge tools should call the functions in Mergemod.dll version 2.0 to merge the module.</span></span> <span data-ttu-id="3492c-106">Frühere Versionen von Mergemod.dll können nicht zum Konfigurieren von Mergemodulen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3492c-106">Earlier versions of Mergemod.dll cannot be used to configure merge modules.</span></span>
-   <span data-ttu-id="3492c-107">Client Konfigurations Anwendungen sollten mit dem mergemodulbenutzer interagieren, um die Benutzer Auswahl für konfigurierbare Elemente zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="3492c-107">Client configuration applications should interact with the merge module user to collect the user selections for configurable items.</span></span>
-   <span data-ttu-id="3492c-108">Die Merge-Tools sollten Konfigurationsinformationen, die im Mergemodul erstellt wurden, für die Client Anwendung verfügbar machen, damit der Client diese Informationen verwenden kann, um den Benutzer abzufragen.</span><span class="sxs-lookup"><span data-stu-id="3492c-108">Merge tools should expose configuration information authored into the merge module to the client application so that the client can use this information to query the user.</span></span>
-   <span data-ttu-id="3492c-109">Wenn ein Zusammenführungstool während einer Zusammenführung auf ein konfigurierbares Element stößt, sollte es das Client Konfigurationstool für Anpassungs Informationen abrufen, die vom Benutzer abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="3492c-109">When a merge tool encounters a configurable item during a merge, it should call the client configuration tool for customization information obtained from the user.</span></span> <span data-ttu-id="3492c-110">Das Merge-Tool sollte die angegebenen Änderungen am Mergemodul vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3492c-110">The merge tool should make the specified changes to the merge module.</span></span>
-   <span data-ttu-id="3492c-111">Konfigurations Anwendungen sollten es dem Benutzer ermöglichen, Optionen für konfigurierbare Elemente bereitzustellen, aber alle möglichen Optionen müssen für den Benutzer nicht offengelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3492c-111">Configuration applications should enable the user to provide choices for configurable items, but all the possible choices do not need to be revealed to the user.</span></span> <span data-ttu-id="3492c-112">Das Mergetool kann Standardwerte für konfigurierbare Elemente verwenden, die der Benutzer nicht ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="3492c-112">The merge tool can use default values for configurable items that the user does not select.</span></span>
-   <span data-ttu-id="3492c-113">Wenn ein Benutzer keine Anpassungs Informationen bereitstellt, sollten die mergetools die im Mergemodul angegebenen Standard Konfigurationswerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="3492c-113">If a user does not provide customization information, merge tools should use the default configuration values that are specified in the merge module.</span></span>
-   <span data-ttu-id="3492c-114">Nachdem ein Benutzer eine bestimmte Auswahl für das Konfigurationstool erteilt hat, ruft das Merge-Tool Mergemod.dll auf, um den Merge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3492c-114">After a user gives the configuration tool specific selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

 

 



