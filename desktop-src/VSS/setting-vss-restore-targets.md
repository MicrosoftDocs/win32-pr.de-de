---
description: Mithilfe der IVssComponent-Schnittstelle kann ein Writer genau anpassen, wie Dateien auf Komponentenbasis wieder hergestellt werden.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Festlegen von VSS-Wiederherstellungs Zielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368255"
---
# <a name="setting-vss-restore-targets"></a><span data-ttu-id="c1bc2-103">Festlegen von VSS-Wiederherstellungs Zielen</span><span class="sxs-lookup"><span data-stu-id="c1bc2-103">Setting VSS Restore Targets</span></span>

<span data-ttu-id="c1bc2-104">Mithilfe der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle kann ein Writer genau anpassen, wie Dateien auf Komponentenbasis wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-104">The [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface enables a writer to fine-tune exactly how files are restored on a component-by-component basis.</span></span>

<span data-ttu-id="c1bc2-105">Da es möglich ist, dass die Systemkonfiguration während der Wiederherstellung etwas anderes als das bei der Sicherung erwartete ist, wird der Wiederherstellungs Ziel Mechanismus bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-105">Because it is possible that the system configuration during restore is something other than that anticipated during backup, the restore target mechanism is provided.</span></span>

<span data-ttu-id="c1bc2-106">Sie ermöglicht es Writer, [**IVssComponent:: abtrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) aufzurufen, um zu ändern, wie die Komponenten, die explizit im Sicherungs Komponenten Dokument [*enthalten*](vssgloss-e.md) sind, wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-106">It allows writers to call [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) to change how those components that are [*explicitly included*](vssgloss-e.md) in the Backup Components Document are restored.</span></span> <span data-ttu-id="c1bc2-107">Dadurch wird auch der Wiederherstellungs Mechanismus geändert, der für die [*implizit enthaltenen*](vssgloss-i.md)Komponenten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-107">This also changes the restoration mechanism used on those components that are [*implicitly included*](vssgloss-i.md).</span></span>

<span data-ttu-id="c1bc2-108">Dateiwiederherstellung, die während eines Systemneustarts stattfindet (unter den Enumerationswerten der [**VSS \_ restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) Enumeration VSS \_ RME \_ Restore \_ at \_ Reboot und VSS \_ RME \_ Restore \_ at \_ Reboot \_ \_ , wenn nicht \_ ersetzen), kann von Wiederherstellungs Zielen nicht beeinflusst werden, da die Dateien von " **muvefileex** " an den endgültigen Speicherort kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-108">File restoration that takes place during a system reboot (under the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration values VSS\_RME\_RESTORE\_AT\_REBOOT and VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE) cannot be affected by restore targets because there are no running VSS services when **MoveFileEx** copies files to their final location.</span></span>

<span data-ttu-id="c1bc2-109">Ebenso kann die \_ benutzerdefinierte VSS RME \_ -Wiederherstellung beeinträchtigt werden, da jede benutzerdefinierte Wiederherstellung für einen bestimmten Writer spezifisch ist und Wiederherstellungs Ziele berücksichtigen oder ignorieren kann.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-109">Similarly, VSS\_RME\_CUSTOM restores may or may not be affected, because each custom restore is specific to a given writer and can choose to respect or ignore restore targets.</span></span>

<span data-ttu-id="c1bc2-110">Anforderer und Writer können [**IVssComponent:: getrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) verwenden, um das Wiederherstellungs Ziel eines Komponenten Satzes zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-110">Requesters and writers can use [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) to check the restore target of a component set.</span></span>

<span data-ttu-id="c1bc2-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) unterstützt die folgenden Wiederherstellungs Ziele, die für eine Komponente festgelegt werden können, die auf Komponentenebene festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="c1bc2-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supports the following restore targets, which can be set on a component set by component set basis:</span></span>

-   <span data-ttu-id="c1bc2-112">VSS \_ RT- \_ Original.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-112">VSS\_RT\_ORIGINAL.</span></span> <span data-ttu-id="c1bc2-113">Die von der [**VSS \_ restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) Enumeration festgelegte Wiederherstellungsmethode wird beachtet.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-113">The restore method specified by the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration will be respected.</span></span>
-   <span data-ttu-id="c1bc2-114">VSS \_ RT- \_ Alternative.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-114">VSS\_RT\_ALTERNATE.</span></span> <span data-ttu-id="c1bc2-115">Die Dateien werden an einem Speicherort wieder hergestellt, der aus einer vorhandenen alternativen Speicherort Zuordnung ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-115">The files are restored to a location determined from an existing alternate location mapping.</span></span> <span data-ttu-id="c1bc2-116">Wenn eine Alternative Speicherort Zuordnung vorhanden ist, die einem Pfad in einer Komponenten Satz-Unterkomponente entspricht, stellen Sie nach Möglichkeit eine Wiederherstellung am alternativen Speicherort Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1bc2-116">If an alternate location mapping matching a path in a component set subcomponent exists, restore to the alternate location if possible; otherwise, return an error.</span></span>

 

 



