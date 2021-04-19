---
description: Sichern von Volumes, während Anwendungen auf einem System weiterhin auf die Volumes schreiben. Minimieren Sie die Ausfallzeiten der Anwendung, indem Sie schnell eine Momentaufnahme (Schatten Kopie) eines Volumes erstellen, das alle Daten dupliziert. Durchführen einer Sicherung mit mehreren Volumes
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348187"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="b34ae-105">Volumeschattenkopie-Dienst</span><span class="sxs-lookup"><span data-stu-id="b34ae-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="b34ae-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="b34ae-106">Purpose</span></span>

<span data-ttu-id="b34ae-107">Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von COM-Schnittstellen, der ein Framework implementiert, das das Ausführen von Volumesicherungen ermöglicht, während Anwendungen auf einem System weiterhin auf die Volumes schreiben.</span><span class="sxs-lookup"><span data-stu-id="b34ae-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="b34ae-108">Eine Einführung in VSS für Systemadministratoren finden Sie unter [Volumeschattenkopie-Dienst](/windows-server/storage/file-server/volume-shadow-copy-service) in der TechNet-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b34ae-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b34ae-109">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="b34ae-109">Run-time requirements</span></span>

<span data-ttu-id="b34ae-110">VSS wird unter Microsoft Windows XP und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b34ae-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="b34ae-111">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" in der Dokumentation für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="b34ae-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="b34ae-112">Alle 32-Bit-VSS-Anwendungen (Requester, Anbieter und Writer) müssen als native 32-Bit-oder 64-Bit-Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b34ae-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="b34ae-113">Die Ausführung unter WOW64 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b34ae-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="b34ae-114">Weitere Informationen finden Sie [unter Unterstützte Konfigurationen und Einschränkungen](usage-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="b34ae-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="b34ae-115">**Windows Server 2003 und Windows XP:** Das Ausführen von 32-Bit-VSS-Anforderern unter WOW64 wird unterstützt, jedoch nicht für Sicherungen des Systemstatus.</span><span class="sxs-lookup"><span data-stu-id="b34ae-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="b34ae-116">Das Ausführen von 32-Bit-VSS-Anbietern und-Writern unter WOW64 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b34ae-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="b34ae-117">Unterstützung für die Ausführung von 32-Bit-Anforderern unter WOW64 wurde in Windows Vista und nachfolgenden Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="b34ae-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="b34ae-118">Eine Schatten Kopie, die auf Windows Server 2003 R2 oder Windows Server 2003 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b34ae-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="b34ae-119">Eine Schatten Kopie, die auf Windows Server 2008 R2 oder Windows Server 2008 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2003 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b34ae-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="b34ae-120">Eine Schatten Kopie, die auf Windows Server 2008 erstellt wurde, kann jedoch auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 ausgeführt wird, und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="b34ae-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="b34ae-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b34ae-121">In this section</span></span>



| <span data-ttu-id="b34ae-122">Thema</span><span class="sxs-lookup"><span data-stu-id="b34ae-122">Topic</span></span>                                                          | <span data-ttu-id="b34ae-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b34ae-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b34ae-124">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b34ae-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="b34ae-125">Beschreibt das VSS-Objektmodell, Sicherungs-und Wiederherstellungs Strategien und die Vorgehensweise beim Erstellen von VSS-Anbietern,-Anforderern und-Writern.</span><span class="sxs-lookup"><span data-stu-id="b34ae-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="b34ae-126">Verweis</span><span class="sxs-lookup"><span data-stu-id="b34ae-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="b34ae-127">Beschreibt VSS-Klassen,-Datentypen,-Enumerationen,-Funktionen,-Schnittstellen und-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="b34ae-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="b34ae-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b34ae-128">Additional resources</span></span>



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34ae-129">Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="b34ae-129">Windows Vista and later</span></span>            | <span data-ttu-id="b34ae-130">VSS ist im Microsoft Windows Software Development Kit (SDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b34ae-130">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b34ae-131">Sie können das SDK für Windows 7 und Windows Server 2008 R2 aus dem [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279)installieren.</span><span class="sxs-lookup"><span data-stu-id="b34ae-131">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="b34ae-132">Sie können auch die [ISO-Version](https://www.microsoft.com/download/details.aspx?id=8442) des SDK aus dem Windows Download Center herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b34ae-132">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="b34ae-133">Frühere Versionen des SDK können von der [Windows SDK Download Seite](https://msdn.microsoft.com/windows/bb980924.aspx)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b34ae-133">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="b34ae-134">Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b34ae-134">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="b34ae-135">VSS ist im SDK für Volumeschattenkopie-Dienst 7,2 verfügbar, das Sie aus dem [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490)herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="b34ae-135">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="b34ae-136">Beachten Sie, dass die 64-Bit-Vssapi. lib-Dateien in den Verzeichnissen unter dem \\ Verzeichnis Win2003 obj für die 64-Bit-Versionen von Windows Server 2003 und Windows XP verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b34ae-136">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
