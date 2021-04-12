---
description: Der Ressourcenschutz verhindert die Ersetzung von Systemdateien und Ordnern sowie Registrierungs Schlüsseln, die für das Betriebssystem von wesentlicher Bedeutung sind. Durch das ändern geschützter Ressourcen können Anwendungs-oder Systemfehler verursacht werden.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Windows-Ressourcenschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347218"
---
# <a name="windows-resource-protection"></a><span data-ttu-id="b0df3-104">Windows-Ressourcenschutz</span><span class="sxs-lookup"><span data-stu-id="b0df3-104">Windows Resource Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="b0df3-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="b0df3-105">Purpose</span></span>

<span data-ttu-id="b0df3-106">Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil des Betriebssystems installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0df3-106">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="b0df3-107">Es wurde ab Windows Server 2008 und Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0df3-107">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="b0df3-108">Anwendungen sollten diese Ressourcen nicht überschreiben, da Sie vom System und anderen Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0df3-108">Applications should not overwrite these resources because they are used by the system and other applications.</span></span> <span data-ttu-id="b0df3-109">Der Schutz dieser Ressourcen verhindert Anwendungs-und Betriebssystem Fehler.</span><span class="sxs-lookup"><span data-stu-id="b0df3-109">Protecting these resources prevents application and operating system failures.</span></span> <span data-ttu-id="b0df3-110">WRP ist der neue Name für den Windows-Datei Schutz (WFP).</span><span class="sxs-lookup"><span data-stu-id="b0df3-110">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="b0df3-111">WRP schützt Registrierungsschlüssel und Ordner sowie wichtige Systemdateien.</span><span class="sxs-lookup"><span data-stu-id="b0df3-111">WRP protects registry keys and folders as well as essential system files.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b0df3-112">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="b0df3-112">Where applicable</span></span>

<span data-ttu-id="b0df3-113">Alle Windows-basierten Anwendungen und deren Installationsprogramme, die unter Windows Server 2008 oder Windows Vista und höheren Betriebssystemen ausgeführt werden, sollten sich von WRP unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b0df3-113">All Windows-based applications and their installation programs that run on Windows Server 2008 or Windows Vista, and later operating systems, should be aware of WRP.</span></span> <span data-ttu-id="b0df3-114">Alle Windows-basierten Anwendungen, die unter Microsoft Windows Server 2003 oder Windows XP ausgeführt werden, und die zugehörigen Installationsprogramme sollten WFP beachten.</span><span class="sxs-lookup"><span data-stu-id="b0df3-114">All Windows-based applications that run on Microsoft Windows Server 2003 or Windows XP and their installation programs should be aware of WFP.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b0df3-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="b0df3-115">Developer audience</span></span>

<span data-ttu-id="b0df3-116">Die WRP-API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="b0df3-116">The WRP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="b0df3-117">Die WRP-API verfügt über zwei Funktionen: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) und [**sfciskeyprotected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span><span class="sxs-lookup"><span data-stu-id="b0df3-117">The WRP API has two functions: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b0df3-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="b0df3-118">Run-time requirements</span></span>

<span data-ttu-id="b0df3-119">Anwendungen, die nur die [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) -Funktion verwenden, benötigen Windows Server 2008, Windows Vista, Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b0df3-119">Applications that use only the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) function require Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.</span></span> <span data-ttu-id="b0df3-120">Anwendungen, die die [**sfciskeyprotected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) -Funktion verwenden, benötigen Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b0df3-120">Applications that use the [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) function require Windows Server 2008 or Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0df3-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b0df3-121">In this section</span></span>



| <span data-ttu-id="b0df3-122">Thema</span><span class="sxs-lookup"><span data-stu-id="b0df3-122">Topic</span></span>                                                                                     | <span data-ttu-id="b0df3-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0df3-123">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="b0df3-124">Informationen zu Windows-Ressourcenschutz</span><span class="sxs-lookup"><span data-stu-id="b0df3-124">About Windows Resource Protection</span></span>](about-windows-file-protection.md)<br/>         | <span data-ttu-id="b0df3-125">Allgemeine Informationen zu WRP.</span><span class="sxs-lookup"><span data-stu-id="b0df3-125">General information about WRP.</span></span><br/>   |
| [<span data-ttu-id="b0df3-126">Windows-Ressourcenschutz Referenz</span><span class="sxs-lookup"><span data-stu-id="b0df3-126">Windows Resource Protection Reference</span></span>](windows-file-protection-reference.md)<br/> | <span data-ttu-id="b0df3-127">Referenz Dokumentation für WRP.</span><span class="sxs-lookup"><span data-stu-id="b0df3-127">Reference documentation for WRP.</span></span><br/> |



 

 

 




