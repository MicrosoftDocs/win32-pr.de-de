---
description: Die Methode "kreatetransformsummaryinfo" des Datenbankobjekts erstellt den Zusammenfassungs Informationsdaten Strom einer vorhandenen Transformations Datei und füllt ihn auf. Diese Methode füllt die Eigenschaften mit den Basis-und Referenz-ProductCode und ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database. kreatetransformsummaryinfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369473"
---
# <a name="databasecreatetransformsummaryinfo-method"></a><span data-ttu-id="b6731-104">Database. kreatetransformsummaryinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="b6731-104">Database.CreateTransformSummaryInfo method</span></span>

<span data-ttu-id="b6731-105">Die Methode " **kreatetransformsummaryinfo** " des [**Daten Bank**](database-object.md) Objekts erstellt den Zusammenfassungs Informationsdaten Strom einer vorhandenen Transformations Datei und füllt ihn auf.</span><span class="sxs-lookup"><span data-stu-id="b6731-105">The **CreateTransformSummaryInfo** method of the [**Database**](database-object.md) object creates and populates the summary information stream of an existing transform file.</span></span> <span data-ttu-id="b6731-106">Diese Methode füllt die Eigenschaften mit den Basis-und Referenz- [**ProductCode**](productcode.md) und [**ProductVersion**](productversion.md).</span><span class="sxs-lookup"><span data-stu-id="b6731-106">This method fills in the properties with the base and reference [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6731-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6731-107">Syntax</span></span>


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a><span data-ttu-id="b6731-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6731-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6731-109">*Referenz*</span><span class="sxs-lookup"><span data-stu-id="b6731-109">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="b6731-110">Erforderliche Datenbank, in der die Änderungen nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b6731-110">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="b6731-111">*storage*</span><span class="sxs-lookup"><span data-stu-id="b6731-111">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="b6731-112">Der Name der generierten Transformations Datei.</span><span class="sxs-lookup"><span data-stu-id="b6731-112">The name of the generated transform file.</span></span> <span data-ttu-id="b6731-113">Diese Eingabe ist optional.</span><span class="sxs-lookup"><span data-stu-id="b6731-113">This is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b6731-114">*errorconditions*</span><span class="sxs-lookup"><span data-stu-id="b6731-114">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="b6731-115">Erforderliche Fehlerbedingungen, die unterdrückt werden sollen, wenn die Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6731-115">Required error conditions that should be suppressed when the transform is applied.</span></span> <span data-ttu-id="b6731-116">Kombinieren Sie einen oder mehrere der folgenden Fehler Bedingungs Werte.</span><span class="sxs-lookup"><span data-stu-id="b6731-116">Combine one or more of the following error condition values.</span></span>



| <span data-ttu-id="b6731-117">Name der Fehlerbedingung</span><span class="sxs-lookup"><span data-stu-id="b6731-117">Error condition name</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="b6731-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6731-118">Meaning</span></span>                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <span data-ttu-id="b6731-119"><dt>**msitransformerrornone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span></span> </dl>                                                                         | <span data-ttu-id="b6731-120">Keine der folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="b6731-120">None of the following conditions.</span></span><br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="b6731-121"><dt>**msitransformerroradde xistingrow**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span></span> </dl>                                 | <span data-ttu-id="b6731-122">Fügt eine Zeile hinzu, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b6731-122">Adds a row that already exists.</span></span><br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="b6731-123"><dt>**msitransformerrordeletenonexistingrow**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="b6731-124">Löscht eine Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b6731-124">Deletes a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="b6731-125"><dt>**msitransformerroradde xistingtable**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="b6731-126">Fügt eine Tabelle hinzu, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b6731-126">Adds a table that already exists.</span></span><br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="b6731-127"><dt>**msitransformerrordeletenonexistingtable**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="b6731-128">Löscht eine Tabelle, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b6731-128">Deletes a table that does not exist.</span></span><br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="b6731-129"><dt>**msitransformerrorupdatenonexistingrow**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span></span> </dl>        | <span data-ttu-id="b6731-130">Aktualisiert eine Zeile, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b6731-130">Updates a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="b6731-131"><dt>**msitransformerrorchangecodepage**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span></span> </dl>                                | <span data-ttu-id="b6731-132">Transformations-und Daten Bank Codepages stimmen nicht zu, und keine der Codepage ist neutral.</span><span class="sxs-lookup"><span data-stu-id="b6731-132">Transform and database code pages do not match and neither code page is neutral.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b6731-133">*validation*</span><span class="sxs-lookup"><span data-stu-id="b6731-133">*validation*</span></span> 
</dt> <dd>

<span data-ttu-id="b6731-134">Erforderlich, wenn die Transformation auf eine Datenbank angewendet wird. zeigt an, welche Eigenschaften überprüft werden sollten, um sicherzustellen, dass diese Transformation auf die Datenbank angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6731-134">Required when the transform is applied to a database; shows which properties should be validated to verify that this transform can be applied to the database.</span></span> <span data-ttu-id="b6731-135">Die Eigenschaften sind alle im Eigenschaften Satz für den [Zusammenfassungs Informationsstrom](summary-information-stream-property-set.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="b6731-135">The properties are all contained in the [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="b6731-136">Kombinieren Sie einen oder mehrere der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="b6731-136">Combine one or more of the following values.</span></span>



| <span data-ttu-id="b6731-137">Validierungsflag</span><span class="sxs-lookup"><span data-stu-id="b6731-137">Validation flag</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="b6731-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6731-138">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <span data-ttu-id="b6731-139"><dt>**msitransformvalidationnone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="b6731-140">Es wurde keine Validierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6731-140">No validation done.</span></span><br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <span data-ttu-id="b6731-141"><dt>**msitransformvalidationlanguage**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b6731-142">Die Standardsprache muss der Basisdatenbank entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b6731-142">Default language must match base database.</span></span><br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <span data-ttu-id="b6731-143"><dt>**msitransformvalidationproduct**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="b6731-144">Das Produkt muss der Basisdatenbank entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b6731-144">Product must match base database.</span></span><br/>          |



 

<span data-ttu-id="b6731-145">Wählen Sie zum Überprüfen der Produktversion zunächst mindestens eines dieser drei Flags aus, um anzugeben, wie viel der Version überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6731-145">To validate product version, first choose one or more of these three flags to indicate how much of the version is to be verified.</span></span>



| <span data-ttu-id="b6731-146">Validierungsflag</span><span class="sxs-lookup"><span data-stu-id="b6731-146">Validation flag</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="b6731-147">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6731-147">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <span data-ttu-id="b6731-148"><dt>**msitransformvalidationmajorver**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span></span> </dl>      | <span data-ttu-id="b6731-149">Prüft nur die Hauptversion.</span><span class="sxs-lookup"><span data-stu-id="b6731-149">Checks major version only.</span></span><br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <span data-ttu-id="b6731-150"><dt>**msitransformvalidationminorver**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span></span> </dl>     | <span data-ttu-id="b6731-151">Prüft nur die Haupt-und neben Version.</span><span class="sxs-lookup"><span data-stu-id="b6731-151">Checks major and minor version only.</span></span><br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <span data-ttu-id="b6731-152"><dt>**msitransformvalidationupdatever**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span></span> </dl> | <span data-ttu-id="b6731-153">Überprüft die Haupt-, neben-und Update Versionen.</span><span class="sxs-lookup"><span data-stu-id="b6731-153">Checks major, minor, and update versions.</span></span><br/> |



 

<span data-ttu-id="b6731-154">Wählen Sie dann eine der folgenden Optionen aus, um die erforderliche Beziehung zwischen der Produktversion der Datenbank, auf die die Transformation angewendet wird, und der der Basisdatenbank anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b6731-154">Then choose one of the following to indicate the required relationship between the product version of the database the transform is being applied to and that of the base database.</span></span>



| <span data-ttu-id="b6731-155">Validierungsflag</span><span class="sxs-lookup"><span data-stu-id="b6731-155">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="b6731-156">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6731-156">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <span data-ttu-id="b6731-157"><dt>**msitransformvalidationless**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span></span> </dl>                                          | <span data-ttu-id="b6731-158">Version < Basisversion angewendet</span><span class="sxs-lookup"><span data-stu-id="b6731-158">Applied version < base version</span></span><br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <span data-ttu-id="b6731-159"><dt>**msitransformvalidationlessorequal**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span></span> </dl>             | <span data-ttu-id="b6731-160">Angewendete Version <= Basisversion</span><span class="sxs-lookup"><span data-stu-id="b6731-160">Applied version <= base version</span></span><br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <span data-ttu-id="b6731-161"><dt>**msitransformvalidationequal**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span></span> </dl>                                     | <span data-ttu-id="b6731-162">Angewendete Version = Basisversion</span><span class="sxs-lookup"><span data-stu-id="b6731-162">Applied version = base version</span></span><br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <span data-ttu-id="b6731-163"><dt>**msitransformvalidationgreaterorequal**</dt> <dt>512</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span></span> </dl> | <span data-ttu-id="b6731-164">Angewendete Version >= Basisversion</span><span class="sxs-lookup"><span data-stu-id="b6731-164">Applied version >= base version</span></span><br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <span data-ttu-id="b6731-165"><dt>**msitransformvalidationgreater**</dt> <dt>1024</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span></span> </dl>                            | <span data-ttu-id="b6731-166">Version > Basisversion angewendet</span><span class="sxs-lookup"><span data-stu-id="b6731-166">Applied version > base version</span></span><br/>  |



 

<span data-ttu-id="b6731-167">Legen Sie das folgende Flag fest, um zu überprüfen, ob die Transformation auf ein Paket angewendet wird, das über den entsprechenden [**UpgradeCode**](upgradecode.md)verfügt.</span><span class="sxs-lookup"><span data-stu-id="b6731-167">To validate that the transform is being applied to a package having the appropriate [**UpgradeCode**](upgradecode.md), set the following flag.</span></span>



| <span data-ttu-id="b6731-168">Validierungsflag</span><span class="sxs-lookup"><span data-stu-id="b6731-168">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="b6731-169">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6731-169">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <span data-ttu-id="b6731-170"><dt>**msitransformvalidationupgradecode**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="b6731-171">Überprüft, ob die Transformation der geeignete [**UpgradeCode**](upgradecode.md)ist.</span><span class="sxs-lookup"><span data-stu-id="b6731-171">Validates that the transform is the appropriate [**UpgradeCode**](upgradecode.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6731-172">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6731-172">Return value</span></span>

<span data-ttu-id="b6731-173">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b6731-173">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6731-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6731-174">Remarks</span></span>

<span data-ttu-id="b6731-175">Um einen Zusammenfassungs Informationsdaten Strom für eine Transformation zu erstellen, müssen die [**ProductCode**](productcode.md) -Eigenschaft und die [**ProductVersion**](productversion.md) - [Eigenschaft](property-table.md) in den Eigenschaften Tabellen der Basis-und der Verweis Datenbank definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6731-175">To create a summary information stream for a transform, the [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md) properties must be defined in the [Property](property-table.md) tables of both the base and reference databases.</span></span> <span data-ttu-id="b6731-176">Wenn msitransformvalidationupgradecode verwendet wird, muss die [**UpgradeCode**](upgradecode.md) -Eigenschaft in beiden Datenbanken definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6731-176">If msiTransformValidationUpgradeCode is used, the [**UpgradeCode**](upgradecode.md) property must be defined in both databases.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6731-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6731-177">Requirements</span></span>



| <span data-ttu-id="b6731-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6731-178">Requirement</span></span> | <span data-ttu-id="b6731-179">Wert</span><span class="sxs-lookup"><span data-stu-id="b6731-179">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6731-180">Version</span><span class="sxs-lookup"><span data-stu-id="b6731-180">Version</span></span><br/> | <span data-ttu-id="b6731-181">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6731-181">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b6731-182">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b6731-182">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b6731-183">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6731-183">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b6731-184">DLL</span><span class="sxs-lookup"><span data-stu-id="b6731-184">DLL</span></span><br/>     | <dl> <span data-ttu-id="b6731-185"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6731-185"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b6731-186">IID</span><span class="sxs-lookup"><span data-stu-id="b6731-186">IID</span></span><br/>     | <span data-ttu-id="b6731-187">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b6731-187">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="b6731-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6731-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6731-189">Daten Bank Transformationen</span><span class="sxs-lookup"><span data-stu-id="b6731-189">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




