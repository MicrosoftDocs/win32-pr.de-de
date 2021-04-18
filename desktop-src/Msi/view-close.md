---
description: Die Close-Methode des View-Objekts beendet die Abfrage Ausführung und gibt Datenbankressourcen frei.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357703"
---
# <a name="viewclose-method"></a><span data-ttu-id="20648-103">View. Close-Methode</span><span class="sxs-lookup"><span data-stu-id="20648-103">View.Close method</span></span>

<span data-ttu-id="20648-104">Die **Close** -Methode des [**View**](view-object.md) -Objekts beendet die Abfrage Ausführung und gibt Datenbankressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="20648-104">The **Close** method of the [**View**](view-object.md) object terminates query execution and releases database resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="20648-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20648-105">Syntax</span></span>


```JScript
View.Close()
```



## <a name="parameters"></a><span data-ttu-id="20648-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20648-106">Parameters</span></span>

<span data-ttu-id="20648-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="20648-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20648-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20648-108">Return value</span></span>

<span data-ttu-id="20648-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="20648-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20648-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20648-110">Remarks</span></span>

<span data-ttu-id="20648-111">Diese Methode muss aufgerufen werden, bevor die [**Execute**](view-execute.md) -Methode erneut für das [**View**](view-object.md) -Objekt aufgerufen wird, es sei denn, alle Zeilen des Resultsets wurden mit der [**Fetch**](view-fetch.md) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="20648-111">This method must be called before the [**Execute**](view-execute.md) method is called again on the [**View**](view-object.md) object unless all rows of the result set have been obtained with the [**Fetch**](view-fetch.md) method.</span></span> <span data-ttu-id="20648-112">Sie wird intern aufgerufen, wenn die Ansicht zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="20648-112">It is called internally when the view is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="20648-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20648-113">Requirements</span></span>



| <span data-ttu-id="20648-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20648-114">Requirement</span></span> | <span data-ttu-id="20648-115">Wert</span><span class="sxs-lookup"><span data-stu-id="20648-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20648-116">Version</span><span class="sxs-lookup"><span data-stu-id="20648-116">Version</span></span><br/> | <span data-ttu-id="20648-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20648-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="20648-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20648-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="20648-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="20648-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="20648-120">DLL</span><span class="sxs-lookup"><span data-stu-id="20648-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="20648-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20648-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="20648-122">IID</span><span class="sxs-lookup"><span data-stu-id="20648-122">IID</span></span><br/>     | <span data-ttu-id="20648-123">IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="20648-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




