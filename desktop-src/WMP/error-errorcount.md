---
title: Fehler. errorCount
description: Die errorCount-Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- 'Fehler: errorCount Windows Media Player'
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371979"
---
# <a name="errorerrorcount"></a><span data-ttu-id="c6fce-104">Fehler. errorCount</span><span class="sxs-lookup"><span data-stu-id="c6fce-104">Error.errorCount</span></span>

<span data-ttu-id="c6fce-105">Die **errorCount** -Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="c6fce-105">The **errorCount** property retrieves the number of errors in the error queue.</span></span>

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a><span data-ttu-id="c6fce-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c6fce-106">Possible Values</span></span>

<span data-ttu-id="c6fce-107">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="c6fce-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6fce-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6fce-108">Remarks</span></span>

<span data-ttu-id="c6fce-109">Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6fce-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="c6fce-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6fce-110">Examples</span></span>

<span data-ttu-id="c6fce-111">Im folgenden JScript-Beispiel wird ein *Fehler* verwendet. **errorCount** in einem Ereignishandler, um den Benutzer über den letzten Fehler in der Fehler Warteschlange zu informieren.</span><span class="sxs-lookup"><span data-stu-id="c6fce-111">The following JScript example uses *Error*.**errorCount** in an event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="c6fce-112">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6fce-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c6fce-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6fce-113">Requirements</span></span>



| <span data-ttu-id="c6fce-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6fce-114">Requirement</span></span> | <span data-ttu-id="c6fce-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c6fce-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6fce-116">Version</span><span class="sxs-lookup"><span data-stu-id="c6fce-116">Version</span></span><br/> | <span data-ttu-id="c6fce-117">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c6fce-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c6fce-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c6fce-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="c6fce-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6fce-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6fce-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6fce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fce-121">**Error-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c6fce-121">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





