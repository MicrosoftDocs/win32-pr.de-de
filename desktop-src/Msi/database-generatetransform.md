---
description: Die GenerateTransform-Methode des Database-Objekts erstellt eine Transformation, die bei Anwendung auf die Objektdatenbank die Verweis Datenbank ergibt. Die Transformation wird im Speicher Objekt gespeichert.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database. GenerateTransform-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356418"
---
# <a name="databasegeneratetransform-method"></a><span data-ttu-id="1523b-104">Database. GenerateTransform-Methode</span><span class="sxs-lookup"><span data-stu-id="1523b-104">Database.GenerateTransform method</span></span>

<span data-ttu-id="1523b-105">Die **GenerateTransform** -Methode des [**Database**](database-object.md) -Objekts erstellt eine [*Transformation*](t-gly.md) , die bei Anwendung auf die Objektdatenbank die Verweis Datenbank ergibt.</span><span class="sxs-lookup"><span data-stu-id="1523b-105">The **GenerateTransform** method of the [**Database**](database-object.md) object creates a [*transform*](t-gly.md) that, when applied to the object database, results in the reference database.</span></span> <span data-ttu-id="1523b-106">Die Transformation wird im Speicher Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1523b-106">The transform is stored in the storage object.</span></span>

<span data-ttu-id="1523b-107">Wenn die Transformation während einer Installation angewendet werden soll, müssen Sie den Zusammenfassungs Informationsdaten Strom mithilfe [**der Methode "**](database-createtransformsummaryinfo.md) -Methode" mit der Methode "-Methode" auffüllen.</span><span class="sxs-lookup"><span data-stu-id="1523b-107">If the transform is to be applied during an installation you must use the [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) method to populate the summary information stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="1523b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1523b-108">Syntax</span></span>


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a><span data-ttu-id="1523b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1523b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1523b-110">*Referenz*</span><span class="sxs-lookup"><span data-stu-id="1523b-110">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="1523b-111">Erforderliche Datenbank, in der die Änderungen nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1523b-111">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="1523b-112">*storage*</span><span class="sxs-lookup"><span data-stu-id="1523b-112">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="1523b-113">Der Name der generierten Transformations Datei.</span><span class="sxs-lookup"><span data-stu-id="1523b-113">The name of the generated transform file.</span></span> <span data-ttu-id="1523b-114">Diese Eingabe ist optional.</span><span class="sxs-lookup"><span data-stu-id="1523b-114">This is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1523b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1523b-115">Return value</span></span>

<span data-ttu-id="1523b-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1523b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1523b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1523b-117">Remarks</span></span>

<span data-ttu-id="1523b-118">Eine Transformation kann am Ende einer Tabelle nicht-Primärschlüssel Spalten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1523b-118">A transform can add non-primary key columns to the end of a table.</span></span> <span data-ttu-id="1523b-119">Eine Transformation kann nicht erstellt werden, mit der einer Tabelle Primärschlüssel Spalten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1523b-119">A transform cannot be created that adds primary key columns to a table.</span></span> <span data-ttu-id="1523b-120">Eine Transformation kann nicht erstellt werden, um die Reihenfolge, die Namen oder die Definitionen von Spalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1523b-120">A transform cannot be created that changes the order, names, or definitions of columns.</span></span>

<span data-ttu-id="1523b-121">Diese Methode gibt einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1523b-121">This method returns a Boolean value.</span></span> <span data-ttu-id="1523b-122">Wenn eine Transformation generiert wird, wird true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1523b-122">It returns TRUE if a transform is generated.</span></span> <span data-ttu-id="1523b-123">Wenn eine Transformation nicht generiert wird, wird false zurückgegeben, da es keine Unterschiede zwischen den beiden Datenbanken gibt.</span><span class="sxs-lookup"><span data-stu-id="1523b-123">It returns FALSE if a transform is not generated because there are no differences between the two databases.</span></span> <span data-ttu-id="1523b-124">Wenn die Methode fehlschlägt, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="1523b-124">If the method fails, it generates an error.</span></span>

<span data-ttu-id="1523b-125">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="1523b-125">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1523b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1523b-126">Requirements</span></span>



| <span data-ttu-id="1523b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1523b-127">Requirement</span></span> | <span data-ttu-id="1523b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1523b-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1523b-129">Version</span><span class="sxs-lookup"><span data-stu-id="1523b-129">Version</span></span><br/> | <span data-ttu-id="1523b-130">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1523b-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1523b-131">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1523b-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1523b-132">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="1523b-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1523b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1523b-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="1523b-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1523b-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1523b-135">IID</span><span class="sxs-lookup"><span data-stu-id="1523b-135">IID</span></span><br/>     | <span data-ttu-id="1523b-136">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1523b-136">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="1523b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1523b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1523b-138">**Verbindung**</span><span class="sxs-lookup"><span data-stu-id="1523b-138">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="1523b-139">Daten Bank Transformationen</span><span class="sxs-lookup"><span data-stu-id="1523b-139">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




