---
description: Die ReserveCost-Tabelle ist eine optionale Tabelle, mit der der Autor in jedem Verzeichnis, das vom Installationsstatus einer Komponente abhängt, eine Menge Speicherplatz reservieren kann.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: ReserveCost-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959982"
---
# <a name="reservecost-table"></a><span data-ttu-id="149e2-103">ReserveCost-Tabelle</span><span class="sxs-lookup"><span data-stu-id="149e2-103">ReserveCost Table</span></span>

<span data-ttu-id="149e2-104">Die ReserveCost-Tabelle ist eine optionale Tabelle, mit der der Autor in jedem Verzeichnis, das vom Installationsstatus einer Komponente abhängt, eine Menge Speicherplatz reservieren kann.</span><span class="sxs-lookup"><span data-stu-id="149e2-104">The ReserveCost table is an optional table that allows the author to reserve an amount of disk space in any directory that depends on the installation state of a component.</span></span>

<span data-ttu-id="149e2-105">Die ReserveCost-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="149e2-105">The ReserveCost table has the following columns.</span></span>



| <span data-ttu-id="149e2-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="149e2-106">Column</span></span>        | <span data-ttu-id="149e2-107">Typ</span><span class="sxs-lookup"><span data-stu-id="149e2-107">Type</span></span>                               | <span data-ttu-id="149e2-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="149e2-108">Key</span></span> | <span data-ttu-id="149e2-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="149e2-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="149e2-110">Reservekey</span><span class="sxs-lookup"><span data-stu-id="149e2-110">ReserveKey</span></span>    | [<span data-ttu-id="149e2-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="149e2-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="149e2-112">J</span><span class="sxs-lookup"><span data-stu-id="149e2-112">Y</span></span>   | <span data-ttu-id="149e2-113">N</span><span class="sxs-lookup"><span data-stu-id="149e2-113">N</span></span>        |
| <span data-ttu-id="149e2-114">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="149e2-114">Component\_</span></span>   | [<span data-ttu-id="149e2-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="149e2-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="149e2-116">N</span><span class="sxs-lookup"><span data-stu-id="149e2-116">N</span></span>   | <span data-ttu-id="149e2-117">N</span><span class="sxs-lookup"><span data-stu-id="149e2-117">N</span></span>        |
| <span data-ttu-id="149e2-118">Reservefolder</span><span class="sxs-lookup"><span data-stu-id="149e2-118">ReserveFolder</span></span> | [<span data-ttu-id="149e2-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="149e2-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="149e2-120">N</span><span class="sxs-lookup"><span data-stu-id="149e2-120">N</span></span>   | <span data-ttu-id="149e2-121">J</span><span class="sxs-lookup"><span data-stu-id="149e2-121">Y</span></span>        |
| <span data-ttu-id="149e2-122">Reservelocal</span><span class="sxs-lookup"><span data-stu-id="149e2-122">ReserveLocal</span></span>  | [<span data-ttu-id="149e2-123">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="149e2-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="149e2-124">N</span><span class="sxs-lookup"><span data-stu-id="149e2-124">N</span></span>   | <span data-ttu-id="149e2-125">N</span><span class="sxs-lookup"><span data-stu-id="149e2-125">N</span></span>        |
| <span data-ttu-id="149e2-126">Reservesource</span><span class="sxs-lookup"><span data-stu-id="149e2-126">ReserveSource</span></span> | [<span data-ttu-id="149e2-127">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="149e2-127">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="149e2-128">N</span><span class="sxs-lookup"><span data-stu-id="149e2-128">N</span></span>   | <span data-ttu-id="149e2-129">N</span><span class="sxs-lookup"><span data-stu-id="149e2-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="149e2-130">Spalten</span><span class="sxs-lookup"><span data-stu-id="149e2-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="149e2-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>Reservekey</span><span class="sxs-lookup"><span data-stu-id="149e2-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span></span>
</dt> <dd>

<span data-ttu-id="149e2-132">Primärschlüssel, der einen ReserveCost-Tabelleneintrag eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="149e2-132">Primary key that uniquely identifies a ReserveCost table entry.</span></span>

</dd> <dt>

<span data-ttu-id="149e2-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="149e2-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="149e2-134">Externer Schlüssel für Spalte einer der [Komponenten](component-table.md) Tabellen.</span><span class="sxs-lookup"><span data-stu-id="149e2-134">External key to column one of the [Component](component-table.md) table.</span></span> <span data-ttu-id="149e2-135">Reserviert eine angegebene Menge an Speicherplatz, wenn diese Komponente installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="149e2-135">Reserves a specified amount of space if this component is to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="149e2-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>Reservefolder</span><span class="sxs-lookup"><span data-stu-id="149e2-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span></span>
</dt> <dd>

<span data-ttu-id="149e2-137">Diese Spalte enthält den Namen einer Eigenschaft, bei der es sich um den vollständigen Pfad zum Zielverzeichnis handelt.</span><span class="sxs-lookup"><span data-stu-id="149e2-137">This column contains the name of a property that is the full path to the destination directory.</span></span> <span data-ttu-id="149e2-138">Dieser Eigenschaftsname ist in der Regel der Name eines Verzeichnisses in der [Verzeichnis](directory-table.md) Tabelle oder der Name eines Eigenschaften Satzes, der mithilfe der [AppSearch](appsearch-action.md) -Aktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="149e2-138">This property name is typically the name of a directory in the [Directory](directory-table.md) table or the name of a property set obtained using the [Appsearch](appsearch-action.md) action.</span></span> <span data-ttu-id="149e2-139">Dadurch wird die Menge des Speicherplatzes, der in reservelocal oder reservesource angegeben ist, den volumekosten des Geräts hinzugefügt, das das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="149e2-139">This adds the amount of disk space specified in ReserveLocal or ReserveSource to the volume cost of the device containing the directory.</span></span>

</dd> <dt>

<span data-ttu-id="149e2-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>Reservelocal</span><span class="sxs-lookup"><span data-stu-id="149e2-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span></span>
</dt> <dd>

<span data-ttu-id="149e2-141">Die Anzahl der Bytes an Speicherplatz, die reserviert werden sollen, wenn die verknüpfte Komponente zur lokalen Installation installiert wird.</span><span class="sxs-lookup"><span data-stu-id="149e2-141">The number of bytes of disk space to reserve if the linked component is installed to run locally.</span></span>

</dd> <dt>

<span data-ttu-id="149e2-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>Reservesource</span><span class="sxs-lookup"><span data-stu-id="149e2-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span></span>
</dt> <dd>

<span data-ttu-id="149e2-143">Die Anzahl der Bytes an Speicherplatz, die reserviert werden sollen, wenn die verknüpfte Komponente zum Ausführen von der Quelle installiert wird.</span><span class="sxs-lookup"><span data-stu-id="149e2-143">The number of bytes of disk space to reserve if the linked component is installed to run from source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="149e2-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="149e2-144">Remarks</span></span>

<span data-ttu-id="149e2-145">Die Reservierung von Kosten auf diese Weise kann für Autoren nützlich sein, die sicherstellen möchten, dass nach Abschluss der Installation ein Minimum an Speicherplatz verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="149e2-145">Reserving cost in this way could be useful for authors who want to ensure that a minimum amount of disk space will be available after the installation is completed.</span></span> <span data-ttu-id="149e2-146">Beispielsweise kann dieser Speicherplatz für Benutzer Dokumente oder Anwendungs Dateien (z. b. Indexdateien) reserviert werden, die erst erstellt werden, nachdem die Anwendung nach der Installation gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="149e2-146">For example, this disk space might be reserved for user documents or for application files (such as index files) that are created only after the application is started following installation.</span></span>

<span data-ttu-id="149e2-147">Mithilfe der Tabelle ReserveCost können Sie benutzerdefinierte Aktionen verwenden, um die ungefähren Kosten für beliebige Dateien, Registrierungseinträge oder andere Elemente anzugeben, die von der benutzerdefinierten Aktion installiert werden könnten.</span><span class="sxs-lookup"><span data-stu-id="149e2-147">You can use the ReserveCost table to enable custom actions to specify an approximate cost for any files, registry entries, or other items that the custom action might install.</span></span> <span data-ttu-id="149e2-148">Benutzerdefinierte Aktionen, die der ReserveCost-Tabelle Einträge hinzufügen, sollten zwischen den Aktionen " [costinitialize](costinitialize-action.md) " und " [filecost](filecost-action.md) " sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="149e2-148">Custom actions that add entries to the ReserveCost table should be sequenced between the [CostInitialize](costinitialize-action.md) and [FileCost](filecost-action.md) actions.</span></span> <span data-ttu-id="149e2-149">Dies ist erforderlich, damit die filecost-Aktion die Kosten aller von Einträgen in der ReserveCost-Tabelle betroffenen Komponenten ordnungsgemäß initialisieren kann.</span><span class="sxs-lookup"><span data-stu-id="149e2-149">This is necessary for the FileCost action to correctly initialize the costing of all components affected by entries in the ReserveCost table.</span></span>

## <a name="validation"></a><span data-ttu-id="149e2-150">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="149e2-150">Validation</span></span>

<dl>

[<span data-ttu-id="149e2-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="149e2-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="149e2-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="149e2-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="149e2-153">ICE32</span><span class="sxs-lookup"><span data-stu-id="149e2-153">ICE32</span></span>](ice32.md)  
</dl>

 

 



