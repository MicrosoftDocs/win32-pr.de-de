---
description: Die StringData-Eigenschaft des Datensatz-Objekts ist eine Lese-/Schreibeigenschaft, die Zeichen folgen Daten in ein oder aus einem angegebenen Feld im Datensatz überträgt. Wenn eine ganze Zahl oder ein Objekt gespeichert wurde, wird der zugehörige Zeichen folgen Wert zurückgegeben.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Record. StringData (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361947"
---
# <a name="recordstringdata-property"></a><span data-ttu-id="7e0de-104">Record. StringData (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e0de-104">Record.StringData property</span></span>

<span data-ttu-id="7e0de-105">Die **StringData** -Eigenschaft des [**Datensatz**](record-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die Zeichen folgen Daten in ein oder aus einem angegebenen Feld im Datensatz überträgt.</span><span class="sxs-lookup"><span data-stu-id="7e0de-105">The **StringData** property of the [**Record**](record-object.md) object is a read-write property that transfers string data in to or out of a specified field within the record.</span></span> <span data-ttu-id="7e0de-106">Wenn eine ganze Zahl oder ein Objekt gespeichert wurde, wird der zugehörige Zeichen folgen Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e0de-106">If an integer or object has been stored, its string value is returned.</span></span>

<span data-ttu-id="7e0de-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7e0de-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0de-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e0de-108">Syntax</span></span>


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="7e0de-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7e0de-109">Property value</span></span>

<span data-ttu-id="7e0de-110">Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="7e0de-110">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e0de-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e0de-111">Remarks</span></span>

<span data-ttu-id="7e0de-112">Der zurückgegebene Wert eines nicht vorhandenen Felds ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7e0de-112">The returned value of a nonexistent field is an empty string.</span></span> <span data-ttu-id="7e0de-113">Verwenden Sie entweder eine leere Variante oder eine leere Zeichenfolge, um ein Feld für die Daten Satz Zeichenfolge auf NULL festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7e0de-113">To set a record string field to null, use either an empty variant or an empty string.</span></span> <span data-ttu-id="7e0de-114">Der Versuch, einen Wert in einem nicht vorhandenen Feld zu speichern, verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="7e0de-114">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0de-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e0de-115">Requirements</span></span>



| <span data-ttu-id="7e0de-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e0de-116">Requirement</span></span> | <span data-ttu-id="7e0de-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7e0de-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0de-118">Version</span><span class="sxs-lookup"><span data-stu-id="7e0de-118">Version</span></span><br/> | <span data-ttu-id="7e0de-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7e0de-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7e0de-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e0de-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7e0de-121">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e0de-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7e0de-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7e0de-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e0de-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e0de-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7e0de-124">IID</span><span class="sxs-lookup"><span data-stu-id="7e0de-124">IID</span></span><br/>     | <span data-ttu-id="7e0de-125">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7e0de-125">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




