---
title: Neue Funktion "Datei Versionsverlauf"
description: Neue Funktion "Datei Versionsverlauf"
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104102470"
---
# <a name="new-file-history-feature"></a><span data-ttu-id="9c880-103">Neue Funktion "Datei Versionsverlauf"</span><span class="sxs-lookup"><span data-stu-id="9c880-103">New File History feature</span></span>

## <a name="platform"></a><span data-ttu-id="9c880-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="9c880-104">Platform</span></span>

<span data-ttu-id="9c880-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c880-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="9c880-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c880-106">Description</span></span>

<span data-ttu-id="9c880-107">Die neue Funktion "Datei Versionsverlauf" ersetzt die vorhandene Sicherungs-und Wiederherstellungs Funktion und bietet Schutz für Benutzer Dateien, die in Benutzer Bibliotheken gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9c880-107">The new File History feature replaces the existing Backup and Restore function, and offers protection for user files stored in user libraries.</span></span> <span data-ttu-id="9c880-108">Es wird ein Satz von APIs bereitgestellt, mit denen Entwicklerprogramm gesteuert den Datei Versionsverlauf aktivieren und ein bestimmtes Speicher Ziel auswählen können.</span><span class="sxs-lookup"><span data-stu-id="9c880-108">A set of APIs is provided that allows developers to programmatically enable File History and select a specific storage target.</span></span> <span data-ttu-id="9c880-109">Die Dokumentation für diese APIs ist auf MSDN verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c880-109">Documentation for these APIs is available on MSDN.</span></span>

<span data-ttu-id="9c880-110">Dies kann sich auf Workflows im Zusammenhang mit Datenschutz und Dokumentation auswirken, die von der Windows-Sicherung und-Wiederherstellung abhängen.</span><span class="sxs-lookup"><span data-stu-id="9c880-110">It may affect workflows related to data protection and documentation that depend on the Windows Backup and Restore feature.</span></span>

<span data-ttu-id="9c880-111">Es wird nicht empfohlen, beide Features gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c880-111">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="9c880-112">Der Datei Versionsverlauf überprüft, ob ein Sicherungs Zeitplan vorhanden ist, und ist aktiv. Wenn ein Sicherungs Zeitplan gefunden wird, kann er von Benutzern nicht eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9c880-112">File History checks if a Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="9c880-113">In diesem Fall müssen Benutzer, die den Datei Versionsverlauf verwenden möchten, den Windows-Sicherungs Zeitplan löschen.</span><span class="sxs-lookup"><span data-stu-id="9c880-113">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9c880-114">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="9c880-114">Manifestation</span></span>

<span data-ttu-id="9c880-115">Workflows können unterbrochen werden, und die Dokumentation für die vorherige Methode zum Zugreifen auf das Windows-Sicherungs-und Wiederherstellungs Feature muss aktualisiert werden, um diese Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="9c880-115">Workflows may be interrupted and documentation for the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="solution"></a><span data-ttu-id="9c880-116">Lösung</span><span class="sxs-lookup"><span data-stu-id="9c880-116">Solution</span></span>

<span data-ttu-id="9c880-117">Überarbeiten Sie apps, die Workflows enthalten, die durch das neue Feature "Datei Versionsverlauf" beeinträchtigt werden, um Konflikte zu entfernen und den neuen Satz von APIs zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="9c880-117">Revise apps that contain workflows that are adversely impacted by the new File History feature to remove any conflicts and incorporate the new set of APIs.</span></span>

## <a name="tests"></a><span data-ttu-id="9c880-118">Tests</span><span class="sxs-lookup"><span data-stu-id="9c880-118">Tests</span></span>

<span data-ttu-id="9c880-119">Die-API ermöglicht Entwicklern, zu bestimmen, ob der Datei Versionsverlauf aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9c880-119">The API allows developers to determine if File History is turned on.</span></span>

 

 




