---
description: Beschreibt zwei Arten von Datenträger Kontingent Limits und wie die Datenträger Kontingent Limits gemessen werden.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limits für Datenträger Kontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358544"
---
# <a name="disk-quota-limits"></a><span data-ttu-id="0e0ea-103">Limits für Datenträger Kontingente</span><span class="sxs-lookup"><span data-stu-id="0e0ea-103">Disk Quota Limits</span></span>

<span data-ttu-id="0e0ea-104">Der Speicherplatz, den die einzelnen Dateien verwenden, wird direkt dem Benutzer in Rechnung gestellt, der die Datei besitzt.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-104">The disk space that each file uses is charged directly to the user who owns the file.</span></span> <span data-ttu-id="0e0ea-105">Der Besitzer einer Datei wird durch die Sicherheits-ID (Security Identifier, SID) in den Sicherheitsinformationen für die Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-105">The owner of a file is identified by the security identifier (SID) in the security information for the file.</span></span> <span data-ttu-id="0e0ea-106">Der Gesamt Speicherplatz, der einem Benutzer in Rechnung gestellt wird, ist die Summe der Länge aller Datenströme.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-106">The total disk space charged to a user is the sum of the length of all data streams.</span></span> <span data-ttu-id="0e0ea-107">Das heißt, dass Eigenschaften Satz-Streams und residente Benutzerdaten Ströme das Kontingent des Benutzers beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-107">In other words, property set streams and resident user data streams affect the user's quota.</span></span>

<span data-ttu-id="0e0ea-108">Das Kontingent wird für erneute Analyse Punkte, Sicherheits Deskriptoren oder andere Metadaten, die den Dateien zugeordnet sind, nicht in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-108">Quota is not charged for re-parse points, security descriptors, or other metadata that is associated with the files.</span></span> <span data-ttu-id="0e0ea-109">Das komprimieren oder Dekomprimieren von Dateien wirkt sich nicht auf den für die Dateien gemeldeten Speicherplatz aus.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-109">Compressing or decompressing files does not affect the disk space reported for the files.</span></span> <span data-ttu-id="0e0ea-110">Daher können Kontingent Einstellungen auf einem Volume mit Einstellungen auf einem anderen Volume verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-110">Therefore, quota settings on one volume can be compared to settings on another volume.</span></span>

<span data-ttu-id="0e0ea-111">Es gibt zwei Arten von Datenträger Kontingent Limits, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-111">There are two types of disk quota limits, as shown in the following table.</span></span>



| <span data-ttu-id="0e0ea-112">Begrenzung</span><span class="sxs-lookup"><span data-stu-id="0e0ea-112">Limit</span></span>                        | <span data-ttu-id="0e0ea-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e0ea-113">Description</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0ea-114">Schwellenwert für Warnung</span><span class="sxs-lookup"><span data-stu-id="0e0ea-114">Warning threshold</span></span><br/> | <span data-ttu-id="0e0ea-115">Sie können das System so konfigurieren, dass ein System Protokolldatei-Eintrag generiert wird, wenn der Speicherplatz, der dem Benutzer berechnet wird, diesen Wert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-115">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="0e0ea-116">Feste Kontingente</span><span class="sxs-lookup"><span data-stu-id="0e0ea-116">Hard quota</span></span><br/>        | <span data-ttu-id="0e0ea-117">Sie können das System so konfigurieren, dass ein System Protokolldatei-Eintrag generiert wird, wenn der Speicherplatz, der dem Benutzer berechnet wird, diesen Wert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-117">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span> <span data-ttu-id="0e0ea-118">Sie können das System auch so konfigurieren, dass dem Benutzer zusätzlicher Speicherplatz verweigert wird, wenn der Speicherplatz, der dem Benutzer in Rechnung gestellt wird, diesen Wert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-118">You can also configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.</span></span><br/> |



 

<span data-ttu-id="0e0ea-119">Das NTFS-Dateisystem erstellt automatisch einen Benutzer Kontingent Eintrag, wenn ein Benutzer zum ersten Mal auf das Volume schreibt.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-119">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="0e0ea-120">Einträge, die automatisch erstellt werden, werden die Standardwerte für Warnungs Schwellenwert und feste Kontingent Grenze für das Volume zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0e0ea-120">Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume.</span></span>

 

 




