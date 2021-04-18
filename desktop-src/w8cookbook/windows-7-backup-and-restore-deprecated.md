---
title: Windows 7-Sicherung und-Wiederherstellung als veraltet markiert
description: Windows 7-Sicherung und-Wiederherstellung als veraltet markiert
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106340741"
---
# <a name="windows-7-backup-and-restore-deprecated"></a><span data-ttu-id="3adfa-103">Windows 7-Sicherung und-Wiederherstellung als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="3adfa-103">Windows 7 Backup and Restore deprecated</span></span>

## <a name="platform"></a><span data-ttu-id="3adfa-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="3adfa-104">Platform</span></span>

<span data-ttu-id="3adfa-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="3adfa-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="3adfa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3adfa-106">Description</span></span>

<span data-ttu-id="3adfa-107">Es gibt zwar keine Verhaltensänderungen an Sicherung und Wiederherstellung, diese Funktion ist jedoch veraltet und wird nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3adfa-107">While there is no behavioral change to Backup and Restore, this function is being deprecated and will not be updated.</span></span> <span data-ttu-id="3adfa-108">Sie wurde nur selten verwendet, und ihre Funktionalität wurde durch die neue Funktion "Datei Versionsverlauf" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3adfa-108">It was rarely used and its functionality has been replaced by the new File History feature.</span></span> <span data-ttu-id="3adfa-109">Es wird unter Windows 8 und Enthusiasten ausgeliefert, die von Windows 7 auf Windows 8 aktualisiert haben oder von der Sicherung und Wiederherstellung abhängig sind, oder die Datenträger Abbild Sicherung kann Sie weiterhin verwenden.</span><span class="sxs-lookup"><span data-stu-id="3adfa-109">It will ship in Windows 8 and enthusiasts who upgraded from Windows 7 to Windows 8 or depend on Backup and Restore or disk image backup will be still able to use it.</span></span> <span data-ttu-id="3adfa-110">Alle Zugriffspunkte für die Sicherung und Wiederherstellung, mit Ausnahme der Systemsteuerung, wurden jedoch entfernt.</span><span class="sxs-lookup"><span data-stu-id="3adfa-110">However, all access points to Backup and Restore, with the exception of the Control Panel, have been removed.</span></span> <span data-ttu-id="3adfa-111">Das von der Sicherung und Wiederherstellung verwendete System Steuerungs Applet wurde in Windows 7-Dateiwiederherstellung umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3adfa-111">The Control Panel applet used by Backup and Restore was renamed to Windows 7 File Recovery.</span></span>

<span data-ttu-id="3adfa-112">OEMs, die den Registrierungsschlüssel für die Deaktivierung der Sicherungs Benachrichtigung in Ihren Images festgelegt haben, müssen das nicht mehr tun.</span><span class="sxs-lookup"><span data-stu-id="3adfa-112">OEMs that were setting the registry key to disable backup notification in their images will no longer need to do that.</span></span>

<span data-ttu-id="3adfa-113">Es wird nicht empfohlen, beide Features gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3adfa-113">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="3adfa-114">Der Datei Versionsverlauf überprüft, ob der Sicherungs Zeitplan vorhanden und aktiv ist. wenn er einen gefunden hat, kann er von Benutzern nicht eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3adfa-114">File History checks if Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="3adfa-115">In diesem Fall müssen Benutzer, die den Datei Versionsverlauf verwenden möchten, den Windows-Sicherungs Zeitplan löschen.</span><span class="sxs-lookup"><span data-stu-id="3adfa-115">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="3adfa-116">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="3adfa-116">Manifestation</span></span>

<span data-ttu-id="3adfa-117">Workflows können unterbrochen werden, und die Dokumentation, die sich auf die vorherige Methode zum Zugreifen auf das Windows-Sicherungs-und Wiederherstellungs Feature bezieht, muss aktualisiert werden, um diese Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="3adfa-117">Workflows may be interrupted and documentation that refers to the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="mitigation"></a><span data-ttu-id="3adfa-118">Minderung</span><span class="sxs-lookup"><span data-stu-id="3adfa-118">Mitigation</span></span>

<span data-ttu-id="3adfa-119">Apps, die möglicherweise die Sicherung und Wiederherstellung initiieren, sollten neu geschrieben werden, um zu überprüfen, ob der Datei Versionsverlauf auf ON fest steht, und Benutzern</span><span class="sxs-lookup"><span data-stu-id="3adfa-119">Apps that might trigger Backup and Restore should be rewritten to check if File History is on and let users choose their preferred method.</span></span>

 

 




