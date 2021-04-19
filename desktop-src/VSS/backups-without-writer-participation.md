---
description: Wenn ein VSS-Sicherungs Vorgang ohne Beteiligung eines Writers durchgeführt wird, kann die Erstellung von Schatten Kopien weiterhin stattfinden.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Sicherungen ohne Writer-Teilnahme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360871"
---
# <a name="backups-without-writer-participation"></a><span data-ttu-id="aed08-103">Sicherungen ohne Writer-Teilnahme</span><span class="sxs-lookup"><span data-stu-id="aed08-103">Backups without Writer Participation</span></span>

<span data-ttu-id="aed08-104">Wenn ein VSS-Sicherungs Vorgang ohne Beteiligung eines Writers durchgeführt wird, kann die Erstellung von Schatten Kopien weiterhin stattfinden.</span><span class="sxs-lookup"><span data-stu-id="aed08-104">When a VSS backup operation is conducted without the involvement of a writer, the shadow copy creation can still occur.</span></span>

<span data-ttu-id="aed08-105">Wie an anderer Stelle angegeben (siehe [Standard schattenkopiestatus](shadow-copies-and-shadow-copy-sets.md)), ist das Ergebnis dieser Art von Schatten Kopie ein Volume, das den Zustand eines Datenträgers zum Zeitpunkt der Schatten Kopie widerspiegelt: die Daten auf dem schattenkopierten Volume spiegeln möglicherweise unvollständige oder partielle e/a-Vorgänge wider und werden so beschrieben, dass Sie sich in einem [*Absturz konsistenten Zustand*](vssgloss-c.md)befinden.</span><span class="sxs-lookup"><span data-stu-id="aed08-105">As noted elsewhere (see [Default Shadow Copy State](shadow-copies-and-shadow-copy-sets.md)), the result of this type of shadow copy is a volume reflecting the state of a disk at the time of the shadow copy: data on the shadow-copied volume may reflect incomplete or partial I/O operations and is described as being in a [*crash-consistent state*](vssgloss-c.md).</span></span>

<span data-ttu-id="aed08-106">Es gibt mehrere Situationen, in denen eine Sicherungs Anwendung für Absturz konsistente Schatten Kopien von Daten erforderlich ist:</span><span class="sxs-lookup"><span data-stu-id="aed08-106">There are several situations that will require a backup application to work with crash consistent shadow copied data:</span></span>

-   <span data-ttu-id="aed08-107">**Daten werden von VSS-abhängigen Anwendungen verwaltet.**</span><span class="sxs-lookup"><span data-stu-id="aed08-107">**Data is managed by VSS-unaware applications**</span></span>

    <span data-ttu-id="aed08-108">Fast jedes System verfügt über einige Anwendungen – Text-Editoren, e-Mail-Reader, Word-Prozessoren usw. –, die VSS nicht wissen, ist es wahrscheinlich, dass einige der Daten auf einer Schatten Kopie als in einem Absturz konsistenten Zustand angesehen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="aed08-108">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware, so it is always likely that some of the data on a shadow copy will need to be thought of as being in a crash consistent state.</span></span>

    <span data-ttu-id="aed08-109">Bei dieser Art von Daten handelt es sich in der Regel nicht um System-oder Dienst kritische Daten, sodass die Sicherung nicht problematisch oder zumindest bei einer herkömmlichen Sicherung nicht problematisch sein sollte.</span><span class="sxs-lookup"><span data-stu-id="aed08-109">This sort of data is not typically system- or service-critical, so backing it up should not be problematic, or at least no more problematic than during a conventional backup.</span></span>

    <span data-ttu-id="aed08-110">Wie bei der Vorbereitung für konventionelle Sicherungen sollten Sicherungs Operatoren nach Möglichkeit versuchen, solche Anwendungen anzuhalten oder zu beenden, bevor Sie einen VSS-Sicherungsauftrag starten.</span><span class="sxs-lookup"><span data-stu-id="aed08-110">As with preparations for conventional backups, if possible, backup operators should attempt to suspend or terminate such applications prior to starting a VSS backup job.</span></span>

-   <span data-ttu-id="aed08-111">**System ohne VSS-kompatible Writer**</span><span class="sxs-lookup"><span data-stu-id="aed08-111">**System with no VSS-compatible writers**</span></span>

    <span data-ttu-id="aed08-112">Diese Situation kann relativ selten auftreten, da die meisten Systeme, die durch eine VSS-Sicherungs Anwendung gesichert werden können, über eine VSS-fähige Windows-Version verfügen, die Writer enthalten sollte.</span><span class="sxs-lookup"><span data-stu-id="aed08-112">This situation may be relatively rare because most systems that can be backed up by a VSS backup application will have a VSS-enabled version of Windows, which should contain writers.</span></span>

    <span data-ttu-id="aed08-113">Es gibt jedoch bestimmte Situationen, in denen dieses Problem auftreten kann – z. b. Wenn Sie ein System ohne VSS-Unterstützung sichern, aber das System ein VSS-fähiges Netzwerkgerät für seine Speicherung verwendet.</span><span class="sxs-lookup"><span data-stu-id="aed08-113">However, there are certain circumstances where this problem could arise—for instance, if you are backing up a system without VSS support but the system uses a VSS-enabled networked appliance for its storage.</span></span>

    <span data-ttu-id="aed08-114">Obwohl das Sichern des Systemstatus von einem Absturz konsistenten Abbild nicht optimal ist, kann es für einen Computer ausreichend sein, den Betriebsstatus neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="aed08-114">Although backing up a system's state from a crash-consistent image is not optimal, it may be sufficient for a computer to reboot to an operational status.</span></span> <span data-ttu-id="aed08-115">In vielen Fällen wird der Computer von unvollständigen e/a-Vorgängen in den Dateisystemen wieder hergestellt und wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aed08-115">In many cases, the computer will recover from any incomplete I/O operations to the file systems and will operate normally.</span></span>

-   <span data-ttu-id="aed08-116">**Ein Anforderer, der sich entscheidet, nicht mit den System Autoren zu arbeiten**</span><span class="sxs-lookup"><span data-stu-id="aed08-116">**A requester choosing not to work with the system writers**</span></span>

    <span data-ttu-id="aed08-117">Dieser Umstand tritt auf, wenn ein Anforderer sich entschieden hat, keine Writer-Komponenten hinzuzufügen oder alle Writer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="aed08-117">This circumstance would occur if a requester chose to add no writer components, or disabling all writers.</span></span>

    <span data-ttu-id="aed08-118">Das Ausführen von Sicherungen auf diese Weise wird im Allgemeinen nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="aed08-118">Performing backups in this way is generally discouraged.</span></span> <span data-ttu-id="aed08-119">Obwohl das zu sichernde schattenkopierte Volume ausreichen kann, um ein System in der Ausführung wiederherzustellen, ist es nicht wünschenswert.</span><span class="sxs-lookup"><span data-stu-id="aed08-119">Although the shadow-copied volume to back up might be sufficient to restore a system to running, it is not desirable.</span></span> <span data-ttu-id="aed08-120">Tatsache, dass die Schreiber, die auf dem System ausgeführt werden, mit Funktionen für die Zusammenarbeit mit VSS und Schatten Kopien entworfen wurden, kann die Sicherung Ihrer Daten auf diese Weise zu einer Instabilität führen.</span><span class="sxs-lookup"><span data-stu-id="aed08-120">In fact, given that the writers running on the system are designed with functionality to cooperate with VSS and shadow copies, backing up their data in this way might result in instability.</span></span>

 

 



