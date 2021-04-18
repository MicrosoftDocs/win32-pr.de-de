---
description: Die vorab ausgewählte Eigenschaft gibt an, dass bereits Features ausgewählt wurden und dass das Auswahl Dialogfeld nicht angezeigt werden muss. Bedingte Ausdrücke, die davon abhängen, ob Features bereits installiert sind, verwenden diesen Wert.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Vorab ausgewählte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361422"
---
# <a name="preselected-property"></a><span data-ttu-id="7ff20-103">Vorab ausgewählte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7ff20-103">Preselected property</span></span>

<span data-ttu-id="7ff20-104">Die **vorab ausgewählte** Eigenschaft gibt an, dass bereits Features ausgewählt wurden und dass das Auswahl Dialogfeld nicht angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7ff20-104">The **Preselected** property indicates that features have already been selected and that the selection dialog need not be shown.</span></span>

<span data-ttu-id="7ff20-105">Bedingte Ausdrücke, die davon abhängen, ob Features bereits installiert sind, verwenden diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="7ff20-105">Conditional expressions which depend on whether features are already installed use this value.</span></span> <span data-ttu-id="7ff20-106">Beispielsweise kann die-Eigenschaft verwendet werden, um alle Dialogfelder zu unterdrücken, die während der Wiederaufnahme einer angehaltenen Installation die Funktionsauswahl betreffen.</span><span class="sxs-lookup"><span data-stu-id="7ff20-106">For example, the property can be used to suppress any dialogs involving feature selections during the resumption of a suspended installation.</span></span>

<span data-ttu-id="7ff20-107">Der Installer legt die **vorab ausgewählte** Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der folgenden Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ff20-107">The installer sets the **Preselected** property to a value of "1" during the resumption of a suspended installation or when any of the following properties are specified on the command line.</span></span> <span data-ttu-id="7ff20-108">Wenn die **vorab ausgewählte** Eigenschaft auf 1 festgelegt wurde, verwendet das Installationsprogramm die Bedingungs [Tabelle](condition-table.md) nicht, um die Auswahl der Features auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="7ff20-108">If the **Preselected** property has been set to 1, the installer does not use the [Condition table](condition-table.md) to evaluate the selection of features.</span></span> <span data-ttu-id="7ff20-109">Funktionen werden basierend auf den folgenden Eigenschaften installiert.</span><span class="sxs-lookup"><span data-stu-id="7ff20-109">Features are installed based upon the following properties.</span></span> <span data-ttu-id="7ff20-110">Das Installationsprogramm wertet diese Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="7ff20-110">The installer always evaluates these properties in the following order:</span></span>

1.  [<span data-ttu-id="7ff20-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="7ff20-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="7ff20-112">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="7ff20-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="7ff20-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="7ff20-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="7ff20-114">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="7ff20-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="7ff20-115">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="7ff20-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="7ff20-116">**Benen**</span><span class="sxs-lookup"><span data-stu-id="7ff20-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="7ff20-117">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="7ff20-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="7ff20-118">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="7ff20-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="7ff20-119">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="7ff20-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="7ff20-120">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="7ff20-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="7ff20-121">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="7ff20-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="7ff20-122">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="7ff20-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

## <a name="requirements"></a><span data-ttu-id="7ff20-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ff20-123">Requirements</span></span>



| <span data-ttu-id="7ff20-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ff20-124">Requirement</span></span> | <span data-ttu-id="7ff20-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7ff20-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff20-126">Version</span><span class="sxs-lookup"><span data-stu-id="7ff20-126">Version</span></span><br/> | <span data-ttu-id="7ff20-127">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7ff20-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7ff20-128">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7ff20-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7ff20-129">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ff20-129">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7ff20-130">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff20-130">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ff20-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ff20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff20-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ff20-132">Properties</span></span>](properties.md)
</dt> </dl>

 

 




