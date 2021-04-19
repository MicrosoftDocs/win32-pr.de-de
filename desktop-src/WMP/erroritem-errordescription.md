---
title: ErrorItem. ErrorDescription
description: Die ErrorDescription-Eigenschaft ruft eine Beschreibung des Fehlers ab.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem. ErrorDescription-Windows-Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355279"
---
# <a name="erroritemerrordescription"></a><span data-ttu-id="60fe1-104">ErrorItem. ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="60fe1-104">ErrorItem.errorDescription</span></span>

<span data-ttu-id="60fe1-105">Die **ErrorDescription** -Eigenschaft ruft eine Beschreibung des Fehlers ab.</span><span class="sxs-lookup"><span data-stu-id="60fe1-105">The **errorDescription** property retrieves a description of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a><span data-ttu-id="60fe1-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="60fe1-106">Possible Values</span></span>

<span data-ttu-id="60fe1-107">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="60fe1-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="60fe1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60fe1-108">Remarks</span></span>

<span data-ttu-id="60fe1-109">Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="60fe1-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="60fe1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60fe1-110">Examples</span></span>

<span data-ttu-id="60fe1-111">Im folgenden JScript-Beispiel wird *ErrorItem* verwendet. **ErrorDescription** in einem Ereignishandler, um dem Benutzer die Fehlermeldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="60fe1-111">The following JScript example uses *ErrorItem*.**errorDescription** in an event handler to display the error message to the user.</span></span> <span data-ttu-id="60fe1-112">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="60fe1-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="60fe1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60fe1-113">Requirements</span></span>



| <span data-ttu-id="60fe1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60fe1-114">Requirement</span></span> | <span data-ttu-id="60fe1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="60fe1-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60fe1-116">Version</span><span class="sxs-lookup"><span data-stu-id="60fe1-116">Version</span></span><br/> | <span data-ttu-id="60fe1-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="60fe1-117">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="60fe1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="60fe1-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="60fe1-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60fe1-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60fe1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60fe1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fe1-121">**ErrorItem-Objekt**</span><span class="sxs-lookup"><span data-stu-id="60fe1-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





