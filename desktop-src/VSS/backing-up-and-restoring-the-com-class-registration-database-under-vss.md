---
description: Der Component Object Model (com) ist ein binärer Standard zum Schreiben von Komponenten Software in einer verteilten Computerumgebung.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Sichern und Wiederherstellen der com+-Klassen Registrierungsdatenbank unter VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362981"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a><span data-ttu-id="121ae-103">Sichern und Wiederherstellen der com+-Klassen Registrierungsdatenbank unter VSS</span><span class="sxs-lookup"><span data-stu-id="121ae-103">Backing Up and Restoring the COM+ Class Registration Database Under VSS</span></span>

<span data-ttu-id="121ae-104">Der Component Object Model (com) ist ein binärer Standard zum Schreiben von Komponenten Software in einer verteilten Computerumgebung.</span><span class="sxs-lookup"><span data-stu-id="121ae-104">The Component Object Model (COM) is a binary standard for writing component software in a distributed computing environment.</span></span>

<span data-ttu-id="121ae-105">In der ursprünglichen Win32-Implementierung wurden die Komponenten Bezeichner (GUIDs) und ein anderer com-Zustand in der Registrierung unter **HKEY \_ Classes \_ root \\ CLSID** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="121ae-105">The original Win32 implementation stored component identifiers (GUIDs) and other COM state in the registry under **HKEY\_CLASSES\_ROOT\\CLSID**.</span></span>

<span data-ttu-id="121ae-106">Die aktuelle Generierung der Component Object Model com+ bietet eine Registrierungs unabhängige Datenbank zum Speichern von Komponenten Registrierungsinformationen: der com+-Klassen Registrierungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="121ae-106">The current generation of the Component Object Model, COM+, offers a registry-independent database for storing component registration information: the COM+ Class Registration Database.</span></span>

<span data-ttu-id="121ae-107">Die com+-Klassen Registrierungsdatenbank unterstützt eine VSS Writer, mit der Anforderer die Registrierungsdatenbank mithilfe von Daten sichern kann, die auf einem schattenkopierten Volume gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="121ae-107">The COM+ Class Registration Database supports a VSS writer, which allows requesters to back up the registration database using data stored on a shadow-copied volume.</span></span>

<span data-ttu-id="121ae-108">Zum Wiederherstellen der COM+-Registrierungsdatenbank muss ein Anforderer die [icomadmincatalog:: restoreregdb](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="121ae-108">To restore the COM+ Registration Database, a requester must call the [ICOMAdminCatalog::RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="121ae-109">Weitere Informationen zum Registrierungs-Writer für die com+-Registrierung finden Sie unter [in-Box-VSS-](in-box-vss-writers.md)Writer.</span><span class="sxs-lookup"><span data-stu-id="121ae-109">For more information about the COM+ Registration Database writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
