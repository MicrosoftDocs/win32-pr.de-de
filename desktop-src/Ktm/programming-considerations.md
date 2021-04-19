---
description: 'Weitere Informationen: Programmier Überlegungen für das Schreiben von Ressourcen-Managern'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Überlegungen zur Programmierung beim Schreiben von Ressourcen-Managern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349466"
---
# <a name="programming-considerations-for-writing-resource-managers"></a><span data-ttu-id="1d73c-103">Überlegungen zur Programmierung beim Schreiben von Ressourcen-Managern</span><span class="sxs-lookup"><span data-stu-id="1d73c-103">Programming Considerations For Writing Resource Managers</span></span>

<span data-ttu-id="1d73c-104">Wenn Sie die Kerneltransaktions-Manager-API verwenden, um Ihren Anwendungen Transaktionsunterstützung hinzuzufügen, sollten Sie Folgendes beachten:</span><span class="sxs-lookup"><span data-stu-id="1d73c-104">When using the Kernel Transaction Manager API to add transaction support to your applications, consider the following:</span></span>

-   <span data-ttu-id="1d73c-105">Wenn Sie Ihren eigenen Ressourcen-Manager schreiben, sollten Sie über gute Kenntnisse der Verfahren und Protokolle der Transaktions Verwaltung verfügen.</span><span class="sxs-lookup"><span data-stu-id="1d73c-105">When you are writing your own resource manager, you should have a good, working knowledge of transaction management techniques and protocols.</span></span>
-   <span data-ttu-id="1d73c-106">Wenn Sie Ressourcen-Manager nicht ordnungsgemäß schreiben, können Sie Ihre eigenen Daten mit nicht ordnungsgemäß behandelten Wiederherstellungs Vorgängen beschädigen.</span><span class="sxs-lookup"><span data-stu-id="1d73c-106">If you do not write resource managers correctly, you can corrupt your own data with improperly handled recovery operations.</span></span> <span data-ttu-id="1d73c-107">Sie können auch das Ende des Transaktions Protokolls anheften und das Dateisystem mit Transaktions Protokollen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="1d73c-107">You can also pin the tail of transaction log and fill up your file system with transaction logs.</span></span>
-   <span data-ttu-id="1d73c-108">Wenn die Richtlinie für die Protokoll Größe nicht festgelegt ist, um zu verhindern, dass die Größe des Protokolls zunimmt, werden Transaktionen vom Ressourcen-Manager nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="1d73c-108">If your log size policy is not set to prevent the log from increasing in size, your resource manager will not stop transactions.</span></span> <span data-ttu-id="1d73c-109">Ihr Ressourcen-Manager muss das System nicht mehr aktualisieren, sodass die Dateisystemressourcen nicht überschritten werden.</span><span class="sxs-lookup"><span data-stu-id="1d73c-109">Your resource manager must stop updating the system so it does not overrun the file system resources.</span></span>
-   <span data-ttu-id="1d73c-110">Ressourcen-Manager sollten Zugriffs Steuerungs Listen (Access Control Lists, ACLs) verwenden, um den Zugriff auf die Protokolldateien zu steuern. Andernfalls können Denial-of-Service-Angriffe durchführt werden.</span><span class="sxs-lookup"><span data-stu-id="1d73c-110">Resource managers should use access control lists (ACLs) to control access to the log files; otherwise, denial of service attacks are possible.</span></span>
-   <span data-ttu-id="1d73c-111">Alle Ressourcen-Manager oder Transaktions Teilnehmer, die Daten zwischenspeichern, müssen sich für Benachrichtigungen vor der Vorbereitung anmelden.</span><span class="sxs-lookup"><span data-stu-id="1d73c-111">Any resource manager or transaction participant that caches data must enlist for pre-prepare notifications.</span></span> <span data-ttu-id="1d73c-112">Wenn eine Benachrichtigung vor der Vorbereitung empfangen wird, müssen Sie alle Ihre Daten leeren, damit sich alle Downstream-Ressourcen-Manager vor der Vorbereitungsphase eintragen können.</span><span class="sxs-lookup"><span data-stu-id="1d73c-112">When a pre-prepare notification is received, you must flush all your data, so that any downstream resource managers can enlist before the prepare phase.</span></span> <span data-ttu-id="1d73c-113">Alle weiteren Aufgaben in dieser Transaktion dürfen nicht zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1d73c-113">Any further work in that transaction must not be cached.</span></span>
-   <span data-ttu-id="1d73c-114">Schließt ein Eintragung-Handle nicht, solange die Transaktion noch aktiv ist. Dies bewirkt, dass für die Transaktion ein Rollback ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d73c-114">Do not close an enlistment handle while the transaction is still active; this will cause the transaction to be rolled back.</span></span>

 

 



