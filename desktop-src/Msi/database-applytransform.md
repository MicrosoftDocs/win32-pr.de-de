---
description: Die "applytransform"-Methode des Datenbankobjekts wendet die Transformation auf diese Datenbank an.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database. applytransform-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361423"
---
# <a name="databaseapplytransform-method"></a><span data-ttu-id="35ea5-103">Database. applytransform-Methode</span><span class="sxs-lookup"><span data-stu-id="35ea5-103">Database.ApplyTransform method</span></span>

<span data-ttu-id="35ea5-104">Die " **applytransform** "-Methode des [**Daten Bank**](database-object.md) Objekts wendet die Transformation auf diese Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="35ea5-104">The **ApplyTransform** method of the [**Database**](database-object.md) object applies the transform to this database.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ea5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35ea5-105">Syntax</span></span>


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a><span data-ttu-id="35ea5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35ea5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ea5-107">*storage*</span><span class="sxs-lookup"><span data-stu-id="35ea5-107">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="35ea5-108">Der Pfad zur angewendeten Transformations Datei.</span><span class="sxs-lookup"><span data-stu-id="35ea5-108">Path to the transform file being applied.</span></span> <span data-ttu-id="35ea5-109">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="35ea5-109">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="35ea5-110">*errorconditions*</span><span class="sxs-lookup"><span data-stu-id="35ea5-110">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="35ea5-111">Gibt die Fehlerbedingungen an, die unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="35ea5-111">Specifies the error conditions that are to be suppressed.</span></span> <span data-ttu-id="35ea5-112">Geben Sie als eine Kombination der folgenden ganzzahligen Werte an.</span><span class="sxs-lookup"><span data-stu-id="35ea5-112">Specify as a combination of the following integer values.</span></span>



| <span data-ttu-id="35ea5-113">Fehlerzustand</span><span class="sxs-lookup"><span data-stu-id="35ea5-113">Error condition</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="35ea5-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="35ea5-114">Meaning</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="35ea5-115"><dt>**msitransformerroradentxistingrow**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span></span> </dl>                                 | <span data-ttu-id="35ea5-116">Fügt eine Zeile hinzu, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35ea5-116">Adds a row that already exists.</span></span><br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="35ea5-117"><dt>**msitransformerrordeletenonexistingrow**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="35ea5-118">Löscht eine Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35ea5-118">Deletes a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="35ea5-119"><dt>**msitransformerroradde xistingtable**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span></span> </dl>                         | <span data-ttu-id="35ea5-120">Fügt eine Tabelle hinzu, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35ea5-120">Adds a table that already exists.</span></span><br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="35ea5-121"><dt>**msitransformerrordeletenonexistingtable**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="35ea5-122">Löscht eine Tabelle, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35ea5-122">Deletes a table that does not exist.</span></span><br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="35ea5-123"><dt>**msitransformerrorupdatenonexistingrow**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span></span> </dl>         | <span data-ttu-id="35ea5-124">Aktualisiert eine Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35ea5-124">Updates a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="35ea5-125"><dt>**msitransformerrorchangecodepage**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span></span> </dl>                                 | <span data-ttu-id="35ea5-126">Die Transformations-und Daten Bank Codepages stimmen nicht mit einer neutralen Codepage identisch.</span><span class="sxs-lookup"><span data-stu-id="35ea5-126">Transform and database code pages do not match and neither has a neutral code page.</span></span><br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <span data-ttu-id="35ea5-127"><dt>**msitransformerrorviewtransform**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span></span> </dl>                                     | <span data-ttu-id="35ea5-128">Erstellt die temporäre [ \_ transformview-Tabelle](-transformview-table.md).</span><span class="sxs-lookup"><span data-stu-id="35ea5-128">Creates the temporary [\_TransformView table](-transformview-table.md).</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ea5-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35ea5-129">Return value</span></span>

<span data-ttu-id="35ea5-130">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="35ea5-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ea5-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35ea5-131">Remarks</span></span>

<span data-ttu-id="35ea5-132">Die **applytransform** -Methode verzögert das Transformieren von Tabellen bis zum letzten möglichen Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="35ea5-132">The **ApplyTransform** method delays transforming tables until the last possible moment.</span></span> <span data-ttu-id="35ea5-133">Die in **applytransform** beschriebenen Schritte sind die sofortige Transformation der Tabellen-und Spalten Kataloge für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="35ea5-133">The steps taken in **ApplyTransform** are to immediately transform the table and column catalogs for the database.</span></span> <span data-ttu-id="35ea5-134">Die Tabellen-und Spalten Kataloge werden entsprechend der hinzugefügten oder gelöschten Tabelle und der hinzugefügten Spalte aktualisiert (das Löschen von Spalten ist nicht zulässig).</span><span class="sxs-lookup"><span data-stu-id="35ea5-134">The table and column catalogs are updated according to which table is added or deleted and which column is added (no deletion of columns is allowed).</span></span> <span data-ttu-id="35ea5-135">Wenn eine Tabelle momentan in den Arbeitsspeicher geladen wird und transformiert werden muss, wird Sie transformiert.</span><span class="sxs-lookup"><span data-stu-id="35ea5-135">If a table is currently loaded in memory and needs to be transformed, it is transformed.</span></span> <span data-ttu-id="35ea5-136">Andernfalls wird der Tabellen Status auf festgelegt, der eine Transformation erfordert, sodass beim Laden der Tabelle oder beim commitcommit der Datenbank die Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="35ea5-136">Otherwise, the table state is set to that requiring a transform so that when the table is loaded, or when the database is committed, the transform is applied.</span></span> <span data-ttu-id="35ea5-137">Die Transformation in dieser Instanz bedeutet, dass die tatsächlichen (Zeilen-) Daten der Tabelle hinzugefügt, gelöscht oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="35ea5-137">Transform in this instance means that the actual (row) data of the table is added, deleted, or updated.</span></span>

<span data-ttu-id="35ea5-138">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="35ea5-138">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ea5-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35ea5-139">Requirements</span></span>



| <span data-ttu-id="35ea5-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35ea5-140">Requirement</span></span> | <span data-ttu-id="35ea5-141">Wert</span><span class="sxs-lookup"><span data-stu-id="35ea5-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ea5-142">Version</span><span class="sxs-lookup"><span data-stu-id="35ea5-142">Version</span></span><br/> | <span data-ttu-id="35ea5-143">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="35ea5-143">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="35ea5-144">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35ea5-144">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="35ea5-145">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="35ea5-145">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="35ea5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="35ea5-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="35ea5-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35ea5-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="35ea5-148">IID</span><span class="sxs-lookup"><span data-stu-id="35ea5-148">IID</span></span><br/>     | <span data-ttu-id="35ea5-149">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="35ea5-149">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="35ea5-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35ea5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ea5-151">**Verbindung**</span><span class="sxs-lookup"><span data-stu-id="35ea5-151">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="35ea5-152">Daten Bank Transformationen</span><span class="sxs-lookup"><span data-stu-id="35ea5-152">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




