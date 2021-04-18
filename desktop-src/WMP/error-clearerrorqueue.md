---
title: Error. clearerrorqueue-Methode
description: Mit der clearerrorqueue-Methode werden die Fehler in der Fehler Warteschlange gelöscht. | Error. clearerrorqueue-Methode
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- clearerrorqueue-Methode, Windows Media Player
- clearerrorqueue-Methode, Windows Media Player, Error-Klasse
- Error-Klasse, Windows Media Player, clearerrorqueue-Methode
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358054"
---
# <a name="errorclearerrorqueue-method"></a><span data-ttu-id="6e4b1-107">Error. clearerrorqueue-Methode</span><span class="sxs-lookup"><span data-stu-id="6e4b1-107">Error.clearErrorQueue method</span></span>

<span data-ttu-id="6e4b1-108">Mit der **clearerrorqueue** -Methode werden die Fehler in der Fehler Warteschlange gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4b1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e4b1-109">Syntax</span></span>


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a><span data-ttu-id="6e4b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e4b1-110">Parameters</span></span>

<span data-ttu-id="6e4b1-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e4b1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e4b1-112">Return value</span></span>

<span data-ttu-id="6e4b1-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e4b1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e4b1-114">Remarks</span></span>

<span data-ttu-id="6e4b1-115">Diese Methode ist nützlich, um die Fehler Warteschlange zu löschen, nachdem eine Reihe von Fehlern verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-115">This method is useful to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="6e4b1-116">Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-116">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="6e4b1-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e4b1-117">Examples</span></span>

<span data-ttu-id="6e4b1-118">Im folgenden JScript-Beispiel wird ein *Fehler* verwendet. **clearerrorqueue** in einem Ereignishandler, um die Fehler Warteschlange zu leeren, nachdem alle Fehlerbeschreibungen angezeigt wurden.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-118">The following JScript example uses *Error*.**clearErrorQueue** in an event handler to empty the error queue after all error descriptions are displayed.</span></span> <span data-ttu-id="6e4b1-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="6e4b1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e4b1-120">Requirements</span></span>



| <span data-ttu-id="6e4b1-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e4b1-121">Requirement</span></span> | <span data-ttu-id="6e4b1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6e4b1-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e4b1-123">Version</span><span class="sxs-lookup"><span data-stu-id="6e4b1-123">Version</span></span><br/> | <span data-ttu-id="6e4b1-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6e4b1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e4b1-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e4b1-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e4b1-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e4b1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e4b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e4b1-128">**Error-Objekt**</span><span class="sxs-lookup"><span data-stu-id="6e4b1-128">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





