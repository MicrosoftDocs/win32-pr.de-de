---
description: Dies ist die IntegerData-Eigenschaft des Datensatz-Objekts. Diese Eigenschaft mit Lese-/Schreibzugriff überträgt ganzzahlige 32-Bit-Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes. Wenn ein Feldwert nicht in eine ganze Zahl konvertiert werden kann, wird "msidatabasenullinteger" zurückgegeben.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Record. IntegerData (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370123"
---
# <a name="recordintegerdata-property"></a><span data-ttu-id="3385e-105">Record. IntegerData (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3385e-105">Record.IntegerData property</span></span>

<span data-ttu-id="3385e-106">Dies ist die **IntegerData** -Eigenschaft des [**Datensatz**](record-object.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3385e-106">This is the **IntegerData** property of the [**Record**](record-object.md) object.</span></span> <span data-ttu-id="3385e-107">Diese Eigenschaft mit Lese-/Schreibzugriff überträgt ganzzahlige 32-Bit-Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="3385e-107">This read-write property transfers 32-bit integer data in to or out of a specified field within the record.</span></span> <span data-ttu-id="3385e-108">Wenn ein Feldwert nicht in eine ganze Zahl konvertiert werden kann, wird "msidatabasenullinteger" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3385e-108">If a field value cannot be converted to an integer, msiDatabaseNullInteger is returned.</span></span>

<span data-ttu-id="3385e-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3385e-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3385e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3385e-110">Syntax</span></span>


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="3385e-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3385e-111">Property value</span></span>

<span data-ttu-id="3385e-112">Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="3385e-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="3385e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3385e-113">Remarks</span></span>

<span data-ttu-id="3385e-114">Verwenden Sie msidatabasenullinteger, um ein ganz Zahl Feld für Datensätze auf NULL festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3385e-114">To set a record integer field to null, use msiDatabaseNullInteger.</span></span> <span data-ttu-id="3385e-115">Der zurückgegebene Wert eines nicht vorhandenen Felds ist msidatabasenullinteger.</span><span class="sxs-lookup"><span data-stu-id="3385e-115">The returned value of a nonexistent field is msiDatabaseNullInteger.</span></span> <span data-ttu-id="3385e-116">Der Versuch, einen Wert in einem nicht vorhandenen Feld zu speichern, verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="3385e-116">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3385e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3385e-117">Requirements</span></span>



| <span data-ttu-id="3385e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3385e-118">Requirement</span></span> | <span data-ttu-id="3385e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3385e-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3385e-120">Version</span><span class="sxs-lookup"><span data-stu-id="3385e-120">Version</span></span><br/> | <span data-ttu-id="3385e-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3385e-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3385e-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3385e-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3385e-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="3385e-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3385e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3385e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3385e-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3385e-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3385e-126">IID</span><span class="sxs-lookup"><span data-stu-id="3385e-126">IID</span></span><br/>     | <span data-ttu-id="3385e-127">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3385e-127">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




