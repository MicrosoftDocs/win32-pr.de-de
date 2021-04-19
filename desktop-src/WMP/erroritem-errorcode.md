---
title: ErrorItem. ErrorCode
description: Die ErrorCode-Eigenschaft ruft den aktuellen Fehlercode ab.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem. ErrorCode-Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353820"
---
# <a name="erroritemerrorcode"></a><span data-ttu-id="2ce4d-104">ErrorItem. ErrorCode</span><span class="sxs-lookup"><span data-stu-id="2ce4d-104">ErrorItem.errorCode</span></span>

<span data-ttu-id="2ce4d-105">Die **errorCode** -Eigenschaft ruft den aktuellen Fehlercode ab.</span><span class="sxs-lookup"><span data-stu-id="2ce4d-105">The **errorCode** property retrieves the current error code.</span></span>

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a><span data-ttu-id="2ce4d-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2ce4d-106">Possible Values</span></span>

<span data-ttu-id="2ce4d-107">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="2ce4d-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce4d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ce4d-108">Remarks</span></span>

<span data-ttu-id="2ce4d-109">Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="2ce4d-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="2ce4d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ce4d-110">Examples</span></span>

<span data-ttu-id="2ce4d-111">Im folgenden JScript-Beispiel wird *ErrorItem* verwendet. **errorCode** in einem Ereignishandler, um dem Benutzer den Fehlercode anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2ce4d-111">The following JScript example uses *ErrorItem*.**errorCode** in an event handler to display the error code to the user.</span></span> <span data-ttu-id="2ce4d-112">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ce4d-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="2ce4d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ce4d-113">Requirements</span></span>



| <span data-ttu-id="2ce4d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ce4d-114">Requirement</span></span> | <span data-ttu-id="2ce4d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2ce4d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce4d-116">Version</span><span class="sxs-lookup"><span data-stu-id="2ce4d-116">Version</span></span><br/> | <span data-ttu-id="2ce4d-117">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2ce4d-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2ce4d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="2ce4d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="2ce4d-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce4d-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce4d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ce4d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce4d-121">**ErrorItem-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2ce4d-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="2ce4d-122">**ErrorItem. ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2ce4d-122">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> </dl>

 

 





