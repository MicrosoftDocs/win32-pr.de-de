---
description: Die setassingleton-Methode des Objekts "errbemubjectpath" erzwingt, dass der Pfad eine Singleton-WMI-Instanz einer Klasse adressiert. Eine Singleton-Klasse ist eine Klasse, die nie mehr als eine Instanz aufweisen kann.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Errbemubjectpath.-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351097"
---
# <a name="swbemobjectpathsetassingleton-method"></a><span data-ttu-id="b1fd5-104">"Errbemubjectpath. \*"-Methode</span><span class="sxs-lookup"><span data-stu-id="b1fd5-104">SWbemObjectPath.SetAsSingleton method</span></span>

<span data-ttu-id="b1fd5-105">Die **setassingleton** -Methode des Objekts " [**errbemubjectpath**](swbemobjectpath.md) " erzwingt, dass der Pfad eine Singleton-WMI-Instanz einer Klasse adressiert.</span><span class="sxs-lookup"><span data-stu-id="b1fd5-105">The **SetAsSingleton** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a singleton WMI instance of a class.</span></span> <span data-ttu-id="b1fd5-106">Eine Singleton-Klasse ist eine Klasse, die nie mehr als eine Instanz aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="b1fd5-106">A singleton class is a class that can never have more than one instance.</span></span>

<span data-ttu-id="b1fd5-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b1fd5-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span> <span data-ttu-id="b1fd5-108">Errbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="b1fd5-108">SWbemObjectPath</span></span>

## <a name="syntax"></a><span data-ttu-id="b1fd5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1fd5-109">Syntax</span></span>


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a><span data-ttu-id="b1fd5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1fd5-110">Parameters</span></span>

<span data-ttu-id="b1fd5-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b1fd5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1fd5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1fd5-112">Return value</span></span>

<span data-ttu-id="b1fd5-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b1fd5-113">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b1fd5-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b1fd5-114">Error codes</span></span>

<span data-ttu-id="b1fd5-115">Nach Abschluss der **setassingleton** -Methode kann das **Err** -Objekt den folgenden Fehlercode enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1fd5-115">Upon completion of the **SetAsSingleton** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="b1fd5-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b1fd5-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b1fd5-117">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b1fd5-117">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1fd5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1fd5-118">Requirements</span></span>



| <span data-ttu-id="b1fd5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1fd5-119">Requirement</span></span> | <span data-ttu-id="b1fd5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b1fd5-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1fd5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1fd5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1fd5-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1fd5-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1fd5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1fd5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1fd5-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1fd5-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1fd5-125">Header</span><span class="sxs-lookup"><span data-stu-id="b1fd5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1fd5-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1fd5-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1fd5-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b1fd5-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1fd5-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1fd5-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1fd5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b1fd5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1fd5-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1fd5-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1fd5-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1fd5-131">CLSID</span></span><br/>                    | <span data-ttu-id="b1fd5-132">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="b1fd5-132">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="b1fd5-133">IID</span><span class="sxs-lookup"><span data-stu-id="b1fd5-133">IID</span></span><br/>                      | <span data-ttu-id="b1fd5-134">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="b1fd5-134">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




