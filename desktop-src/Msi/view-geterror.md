---
description: Die GetError-Methode des View-Objekts gibt den Überprüfungs Fehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: View. GetError-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366002"
---
# <a name="viewgeterror-method"></a><span data-ttu-id="ae3b7-103">View. GetError-Methode</span><span class="sxs-lookup"><span data-stu-id="ae3b7-103">View.GetError method</span></span>

<span data-ttu-id="ae3b7-104">Die **getError** -Methode des [**View**](view-object.md) -Objekts gibt den Überprüfungs Fehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-104">The **GetError** method of the [**View**](view-object.md) object returns the Validation error and the column name for which the error occurred.</span></span> <span data-ttu-id="ae3b7-105">In Automation ist der zurückgegebene Wert eine Zeichenfolge der Form \# \# ColumnName, wobei der \# \# einen zweistelligen Fehlercode darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-105">In automation, the returned value is a string of the form \#\#ColumnName, where the \#\# represents a 2-digit error code.</span></span> <span data-ttu-id="ae3b7-106">Gibt den ersten Fehler im Fehler Array der Ansicht zurück. nachfolgende Aufrufe geben den nächsten Wert im Fehler Array zurück.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-106">It returns the first error in the view's error array; subsequent calls return the next value in the error array.</span></span> <span data-ttu-id="ae3b7-107">Sobald der Wert "00" zurückgegeben wird, sind keine weiteren Fehler mehr vorhanden, und nachfolgende Aufrufe durchlaufen das Array lediglich erneut.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-107">Once a value of '00' is returned, no more errors exist, and subsequent calls merely loop through the array again.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3b7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae3b7-108">Syntax</span></span>


```JScript
View.GetError()
```



## <a name="parameters"></a><span data-ttu-id="ae3b7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae3b7-109">Parameters</span></span>

<span data-ttu-id="ae3b7-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae3b7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae3b7-111">Return value</span></span>

<span data-ttu-id="ae3b7-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae3b7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae3b7-113">Requirements</span></span>



| <span data-ttu-id="ae3b7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae3b7-114">Requirement</span></span> | <span data-ttu-id="ae3b7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ae3b7-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3b7-116">Version</span><span class="sxs-lookup"><span data-stu-id="ae3b7-116">Version</span></span><br/> | <span data-ttu-id="ae3b7-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ae3b7-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ae3b7-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ae3b7-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="ae3b7-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ae3b7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ae3b7-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae3b7-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae3b7-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ae3b7-122">IID</span><span class="sxs-lookup"><span data-stu-id="ae3b7-122">IID</span></span><br/>     | <span data-ttu-id="ae3b7-123">IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ae3b7-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




