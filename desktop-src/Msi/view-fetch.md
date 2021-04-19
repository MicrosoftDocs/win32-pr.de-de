---
description: Mit der FETCH-Methode des View-Objekts wird die nächste Zeile von Spaltendaten abgerufen, wenn im Resultset weitere Zeilen verfügbar sind; andernfalls ist es NULL. Rufen Sie die Execute-Methode vor der FETCH-Methode auf.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. FETCH-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365920"
---
# <a name="viewfetch-method"></a><span data-ttu-id="24697-104">View. FETCH-Methode</span><span class="sxs-lookup"><span data-stu-id="24697-104">View.Fetch method</span></span>

<span data-ttu-id="24697-105">Mit der **Fetch** -Methode des [**View**](view-object.md) -Objekts wird die nächste Zeile von Spaltendaten abgerufen, wenn im Resultset weitere Zeilen verfügbar sind; andernfalls ist es NULL.</span><span class="sxs-lookup"><span data-stu-id="24697-105">The **Fetch** method of the [**View**](view-object.md) object retrieves the next row of column data if more rows are available in the result set, otherwise it is Null.</span></span> <span data-ttu-id="24697-106">Rufen Sie die [**Execute**](view-execute.md) -Methode vor der **Fetch** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="24697-106">Call the [**Execute**](view-execute.md) method before the **Fetch** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="24697-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="24697-107">Syntax</span></span>


```JScript
View.Fetch()
```



## <a name="parameters"></a><span data-ttu-id="24697-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="24697-108">Parameters</span></span>

<span data-ttu-id="24697-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="24697-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24697-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24697-110">Return value</span></span>

<span data-ttu-id="24697-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="24697-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24697-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24697-112">Remarks</span></span>

<span data-ttu-id="24697-113">Das gleiche [**Datensatz**](record-object.md) -Objekt sollte zum Abrufen der Daten in mehreren Zeilen verwendet werden. andernfalls sollte das Objekt freigegeben werden, indem der Gültigkeitsbereich verlassen wird.</span><span class="sxs-lookup"><span data-stu-id="24697-113">The same [**Record**](record-object.md) object should be used to retrieve the data in multiple rows, or else the object should be released by going out of scope.</span></span> <span data-ttu-id="24697-114">Der Datensatz kann für das Ende des Resultsets mithilfe der Syntax "if fetchrecord is Nothing" getestet werden.</span><span class="sxs-lookup"><span data-stu-id="24697-114">The record can be tested for the end of the result set using the syntax "If FetchRecord Is Nothing".</span></span>

## <a name="requirements"></a><span data-ttu-id="24697-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24697-115">Requirements</span></span>



| <span data-ttu-id="24697-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24697-116">Requirement</span></span> | <span data-ttu-id="24697-117">Wert</span><span class="sxs-lookup"><span data-stu-id="24697-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24697-118">Version</span><span class="sxs-lookup"><span data-stu-id="24697-118">Version</span></span><br/> | <span data-ttu-id="24697-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="24697-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="24697-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="24697-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="24697-121">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="24697-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="24697-122">DLL</span><span class="sxs-lookup"><span data-stu-id="24697-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="24697-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24697-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="24697-124">IID</span><span class="sxs-lookup"><span data-stu-id="24697-124">IID</span></span><br/>     | <span data-ttu-id="24697-125">IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="24697-125">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




