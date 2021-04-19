---
description: In der Tabelle ODBCDatasource sind die Datenquellen aufgelistet, die zur Installation gehören.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: ODBCDatasource-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353132"
---
# <a name="odbcdatasource-table"></a><span data-ttu-id="caa2c-103">ODBCDatasource-Tabelle</span><span class="sxs-lookup"><span data-stu-id="caa2c-103">ODBCDataSource Table</span></span>

<span data-ttu-id="caa2c-104">In der Tabelle ODBCDatasource sind die Datenquellen aufgelistet, die zur Installation gehören.</span><span class="sxs-lookup"><span data-stu-id="caa2c-104">The ODBCDataSource table lists the data sources belonging to the installation.</span></span>

<span data-ttu-id="caa2c-105">Die ODBCDatasource-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="caa2c-105">The ODBCDataSource table has the following columns.</span></span>



| <span data-ttu-id="caa2c-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="caa2c-106">Column</span></span>            | <span data-ttu-id="caa2c-107">Typ</span><span class="sxs-lookup"><span data-stu-id="caa2c-107">Type</span></span>                         | <span data-ttu-id="caa2c-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="caa2c-108">Key</span></span> | <span data-ttu-id="caa2c-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="caa2c-109">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="caa2c-110">DataSource</span><span class="sxs-lookup"><span data-stu-id="caa2c-110">DataSource</span></span>        | [<span data-ttu-id="caa2c-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="caa2c-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="caa2c-112">J</span><span class="sxs-lookup"><span data-stu-id="caa2c-112">Y</span></span>   | <span data-ttu-id="caa2c-113">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-113">N</span></span>        |
| <span data-ttu-id="caa2c-114">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="caa2c-114">Component\_</span></span>       | [<span data-ttu-id="caa2c-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="caa2c-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="caa2c-116">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-116">N</span></span>   | <span data-ttu-id="caa2c-117">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-117">N</span></span>        |
| <span data-ttu-id="caa2c-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="caa2c-118">Description</span></span>       | [<span data-ttu-id="caa2c-119">Text</span><span class="sxs-lookup"><span data-stu-id="caa2c-119">Text</span></span>](text.md)             | <span data-ttu-id="caa2c-120">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-120">N</span></span>   | <span data-ttu-id="caa2c-121">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-121">N</span></span>        |
| <span data-ttu-id="caa2c-122">Driverdescription</span><span class="sxs-lookup"><span data-stu-id="caa2c-122">DriverDescription</span></span> | [<span data-ttu-id="caa2c-123">Text</span><span class="sxs-lookup"><span data-stu-id="caa2c-123">Text</span></span>](text.md)             | <span data-ttu-id="caa2c-124">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-124">N</span></span>   | <span data-ttu-id="caa2c-125">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-125">N</span></span>        |
| <span data-ttu-id="caa2c-126">Registrierung</span><span class="sxs-lookup"><span data-stu-id="caa2c-126">Registration</span></span>      | [<span data-ttu-id="caa2c-127">Integer</span><span class="sxs-lookup"><span data-stu-id="caa2c-127">Integer</span></span>](integer.md)       | <span data-ttu-id="caa2c-128">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-128">N</span></span>   | <span data-ttu-id="caa2c-129">N</span><span class="sxs-lookup"><span data-stu-id="caa2c-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="caa2c-130">Spalten</span><span class="sxs-lookup"><span data-stu-id="caa2c-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="caa2c-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span><span class="sxs-lookup"><span data-stu-id="caa2c-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span></span>
</dt> <dd>

<span data-ttu-id="caa2c-132">Interner Tokenname für die Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="caa2c-132">Internal token name for data source.</span></span> <span data-ttu-id="caa2c-133">Ein Primärschlüssel für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="caa2c-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="caa2c-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="caa2c-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="caa2c-135">Externer Schlüssel in der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="caa2c-135">External key into the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="caa2c-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="caa2c-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="caa2c-137">Die Beschreibung, die für diese Datenquelle registriert ist.</span><span class="sxs-lookup"><span data-stu-id="caa2c-137">The description registered for this data source.</span></span> <span data-ttu-id="caa2c-138">Dieser Wert kann nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="caa2c-138">This value cannot be localized.</span></span> <span data-ttu-id="caa2c-139">ODBC-Datenquellen Beschreibungen dürfen die maximale SQL-DSN-Länge nicht überschreiten \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="caa2c-139">ODBC data source descriptions cannot exceed SQL\_MAX\_DSN\_LENGTH.</span></span>

</dd> <dt>

<span data-ttu-id="caa2c-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>Driverdescription</span><span class="sxs-lookup"><span data-stu-id="caa2c-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span></span>
</dt> <dd>

<span data-ttu-id="caa2c-141">Zugeordneter Treiber, der möglicherweise bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="caa2c-141">Associated driver which may be pre-existing.</span></span> <span data-ttu-id="caa2c-142">Dieser Wert kann nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="caa2c-142">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="caa2c-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Nummern</span><span class="sxs-lookup"><span data-stu-id="caa2c-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registration</span></span>
</dt> <dd>

<span data-ttu-id="caa2c-144">Dieses Feld gibt den Registrierungstyp für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="caa2c-144">This field specifies the type of registration for the data source.</span></span>



| <span data-ttu-id="caa2c-145">Konstante</span><span class="sxs-lookup"><span data-stu-id="caa2c-145">Constant</span></span>                                      | <span data-ttu-id="caa2c-146">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="caa2c-146">Hexadecimal</span></span> | <span data-ttu-id="caa2c-147">Decimal</span><span class="sxs-lookup"><span data-stu-id="caa2c-147">Decimal</span></span> | <span data-ttu-id="caa2c-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="caa2c-148">Description</span></span>                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| <span data-ttu-id="caa2c-149">**msidbodbcdatasourceregistrationpermachine**</span><span class="sxs-lookup"><span data-stu-id="caa2c-149">**msidbODBCDataSourceRegistrationPerMachine**</span></span> | <span data-ttu-id="caa2c-150">0x000</span><span class="sxs-lookup"><span data-stu-id="caa2c-150">0x000</span></span>       | <span data-ttu-id="caa2c-151">0</span><span class="sxs-lookup"><span data-stu-id="caa2c-151">0</span></span>       | <span data-ttu-id="caa2c-152">Die Datenquelle wird pro Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="caa2c-152">Data source is registered per machine.</span></span> |
| <span data-ttu-id="caa2c-153">**msidbodbcdatasourceregistrationperuser**</span><span class="sxs-lookup"><span data-stu-id="caa2c-153">**msidbODBCDataSourceRegistrationPerUser**</span></span>    | <span data-ttu-id="caa2c-154">0x001</span><span class="sxs-lookup"><span data-stu-id="caa2c-154">0x001</span></span>       | <span data-ttu-id="caa2c-155">1</span><span class="sxs-lookup"><span data-stu-id="caa2c-155">1</span></span>       | <span data-ttu-id="caa2c-156">Die Datenquelle wird pro Benutzer registriert.</span><span class="sxs-lookup"><span data-stu-id="caa2c-156">Data source is registered per user.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="caa2c-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caa2c-157">Remarks</span></span>

<span data-ttu-id="caa2c-158">Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="caa2c-158">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="caa2c-159">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="caa2c-159">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="caa2c-160">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="caa2c-160">Validation</span></span>

<dl>

[<span data-ttu-id="caa2c-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="caa2c-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="caa2c-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="caa2c-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="caa2c-163">ICE32</span><span class="sxs-lookup"><span data-stu-id="caa2c-163">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="caa2c-164">ICE45</span><span class="sxs-lookup"><span data-stu-id="caa2c-164">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="caa2c-165">ICE98</span><span class="sxs-lookup"><span data-stu-id="caa2c-165">ICE98</span></span>](ice98.md)  
</dl>

 

 



