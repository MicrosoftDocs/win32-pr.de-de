---
title: Die allgemeinen SIS-Speicher-und Common-Store Dateien
description: Alle Unterstützungs Dateien, die von einer SIS-Sicherung (Single Instance Store) verwaltet werden, werden als allgemeine Speicherdateien bezeichnet.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Allgemeine Sicherung von Filialen
- SIS-Sicherung (Single Instance Store), allgemeine Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858376"
---
# <a name="the-sis-common-store-and-common-store-files"></a><span data-ttu-id="c767e-105">Die allgemeinen SIS-Speicher-und Common-Store Dateien</span><span class="sxs-lookup"><span data-stu-id="c767e-105">The SIS Common Store and Common-Store Files</span></span>

<span data-ttu-id="c767e-106">Alle Unterstützungs Dateien, die von einer SIS-Sicherung (Single Instance Store) verwaltet werden, werden als *Allgemeine Speicherdateien* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c767e-106">All backing files maintained by single-instance store (SIS) backup are called *common-store files*.</span></span> <span data-ttu-id="c767e-107">Auf jedem SIS-verwalteten Volume ist ein *gemeinsamer Speicher* vorhanden, der alle auf dem Volume vorhandenen Dateien im allgemeinen Speicher enthält.</span><span class="sxs-lookup"><span data-stu-id="c767e-107">One *common store* exists on each SIS-maintained volume and contains all of the common-store files that exist on that volume.</span></span> <span data-ttu-id="c767e-108">Dieses Verzeichnis befindet sich im Stammverzeichnis des Volumes und hat den Namen " \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="c767e-108">This directory is located in the root directory of the volume and is named "\\SIS Common Store".</span></span> <span data-ttu-id="c767e-109">Der allgemeine Speicher ist als ein Verzeichnis implementiert, das vor normalem Benutzer Zugriff geschützt ist, da der Zugriff auf die Dateien des Common Stores nur direkt über die SIS-Sicherungs-API-Funktionen und nicht über Sicherungs-und Wiederherstellungs Anwendungen vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="c767e-109">The common store is implemented as a directory that is protected against normal user access, because common-store files are intended to be accessed directly only by SIS backup API functions and not backup and restore applications.</span></span>

<span data-ttu-id="c767e-110">Die Eigenschaften einer Datei mit dem allgemeinen Speicher sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c767e-110">The properties of a common-store file are the following:</span></span>

-   <span data-ttu-id="c767e-111">Eine Common Store-Datei kann über einen oder mehrere Links verfügen, die darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="c767e-111">A common-store file may have one or more links pointing to it.</span></span>
-   <span data-ttu-id="c767e-112">Nachdem er erstellt wurde, ändert sich der Inhalt einer Datei mit dem allgemeinen Speicher nie.</span><span class="sxs-lookup"><span data-stu-id="c767e-112">After it is created, the contents of a common-store file never change.</span></span>
-   <span data-ttu-id="c767e-113">Die Namen der Dateien des Common Stores sind global eindeutig – das heißt, Sie sind auf allen Volumes auf der ganzen Welt eindeutig, und die Bindung zwischen einem Dateinamen und den Daten des Common Stores ist Global statisch.</span><span class="sxs-lookup"><span data-stu-id="c767e-113">The names of common-store files are globally unique—that is, they are unique across all volumes across all systems in the world, and the binding between a common-store file name and its data is globally static.</span></span>

<span data-ttu-id="c767e-114">Wenn SIS auf einem Volume aktiviert ist, wird eine Kopie der doppelten Dateien im allgemeinen Speicher erstellt, und alle doppelten Dateien werden durch [SIS-Links](sis-links-and-reparse-points.md) ersetzt, die auf die Datei mit dem allgemeinen Speicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="c767e-114">When SIS is enabled on a volume, one copy of the duplicate files is then created to the common store, and all of the duplicate files are replaced with [SIS links](sis-links-and-reparse-points.md) pointing to the common-store file.</span></span> <span data-ttu-id="c767e-115">Weitere Informationen finden Sie unter [Aktivieren oder Deaktivieren von SIS auf einem Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in der TechNet-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c767e-115">For more information, see [Enabling or Disabling SIS on a Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in the TechNet documentation.</span></span>

<span data-ttu-id="c767e-116">Wenn auf einen der SIS-Links für einen Schreibvorgang zugegriffen wird, stellt der SIS-Filter zuerst den ursprünglichen Inhalt der SIS-Verknüpfungs Datei aus der Datei mit dem allgemeinen Speicher wieder her. der Analyse Punkt, der die SIS-Verknüpfungs Datei mit dem allgemeinen Speicher verbindet, wird entfernt, und der Schreibvorgang wird dann für die ursprüngliche Zieldatei durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c767e-116">When one of the SIS links is accessed for a write operation, the SIS filter first restores the original contents of the SIS link file from the common-store file, the reparse point linking the SIS link file to the common store is removed, and then the write operation is performed on the original destination file.</span></span>

<span data-ttu-id="c767e-117">Die Datei mit dem allgemeinen Speicher wird nur entfernt, wenn der letzte auf Sie verweisende SIS-Link gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c767e-117">The common-store file is removed only when the last SIS link pointing to it is deleted.</span></span>

 

 