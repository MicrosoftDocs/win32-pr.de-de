---
title: Error. WebHelp-Methode
description: Die WebHelp-Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null). | Error. WebHelp-Methode
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- WebHelp-Methode (Windows Media Player)
- WebHelp-Methode, Windows Media Player, Fehler Klasse
- Error-Klasse, Windows Media Player, WebHelp-Methode
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370280"
---
# <a name="errorwebhelp-method"></a><span data-ttu-id="2bd1f-107">Error. WebHelp-Methode</span><span class="sxs-lookup"><span data-stu-id="2bd1f-107">Error.webHelp method</span></span>

<span data-ttu-id="2bd1f-108">Die **WebHelp** -Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null).</span><span class="sxs-lookup"><span data-stu-id="2bd1f-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd1f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd1f-109">Syntax</span></span>


```JScript
Error.webHelp()
```



## <a name="parameters"></a><span data-ttu-id="2bd1f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bd1f-110">Parameters</span></span>

<span data-ttu-id="2bd1f-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bd1f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bd1f-112">Return value</span></span>

<span data-ttu-id="2bd1f-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd1f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bd1f-114">Remarks</span></span>

<span data-ttu-id="2bd1f-115">Die Web-Hilfeseiten enthalten stets die neuesten und detailliertesten Informationen zu Windows Media Player-Fehlern.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="2bd1f-116">Diese Methode überträgt automatisch die anderen Informationen, die von der Webhilfe benötigt werden, z. b. die verwendete Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="2bd1f-117">Wenn Sie direkt auf die Web-Hilfeseiten zugreifen möchten, verwenden Sie die folgenden Links zu Fehlercode und Support Center.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-117">To access the Web Help pages directly, use the following error code and support center links.</span></span>

-   [<span data-ttu-id="2bd1f-118">Windows Media Player-Fehler Code Informationen</span><span class="sxs-lookup"><span data-stu-id="2bd1f-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="2bd1f-119">Windows Media Player-Lösungs Center</span><span class="sxs-lookup"><span data-stu-id="2bd1f-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

<span data-ttu-id="2bd1f-120">**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-120">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="examples"></a><span data-ttu-id="2bd1f-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bd1f-121">Examples</span></span>

<span data-ttu-id="2bd1f-122">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das die Microsoft Windows Media Player-Webhilfe Seite aufruft.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-122">The following example creates an HTML BUTTON element that launches the Microsoft Windows Media Player Web Help page.</span></span> <span data-ttu-id="2bd1f-123">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a><span data-ttu-id="2bd1f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd1f-124">Requirements</span></span>



| <span data-ttu-id="2bd1f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bd1f-125">Requirement</span></span> | <span data-ttu-id="2bd1f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2bd1f-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd1f-127">Version</span><span class="sxs-lookup"><span data-stu-id="2bd1f-127">Version</span></span><br/> | <span data-ttu-id="2bd1f-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2bd1f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2bd1f-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="2bd1f-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bd1f-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd1f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bd1f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd1f-132">**Error-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2bd1f-132">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





