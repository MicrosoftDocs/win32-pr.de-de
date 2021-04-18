---
title: Error. Item-Methode
description: Die Item-Methode ruft ein ErrorItem-Objekt aus der Fehler Warteschlange ab.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, Fehler Klasse
- Error-Klasse, Windows-Media Player, Element-Methode
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364787"
---
# <a name="erroritem-method"></a><span data-ttu-id="5a030-106">Error. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="5a030-106">Error.item method</span></span>

<span data-ttu-id="5a030-107">Die **Item** -Methode ruft ein **ErrorItem** -Objekt aus der Fehler Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="5a030-107">The **item** method retrieves an **ErrorItem** object from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a030-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a030-108">Syntax</span></span>


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="5a030-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a030-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a030-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a030-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a030-111">**Zahl** (**Long**), die den Index des abzurufenden **ErrorItem** -Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="5a030-111">**Number** (**long**) containing the index of the **ErrorItem** object to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a030-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a030-112">Return value</span></span>

<span data-ttu-id="5a030-113">Diese Methode gibt ein **ErrorItem** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5a030-113">This method returns an **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a030-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a030-114">Remarks</span></span>

<span data-ttu-id="5a030-115">Windows Media Player kann als Reaktion auf eine Fehlerbedingung eine Reihe von Fehlern generieren.</span><span class="sxs-lookup"><span data-stu-id="5a030-115">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="5a030-116">Diese Methode ermöglicht das Abrufen eines bestimmten Fehlers in der Warteschlange mithilfe einer Indexnummer.</span><span class="sxs-lookup"><span data-stu-id="5a030-116">This method allows the retrieval of a specific error in the queue by using an index number.</span></span> <span data-ttu-id="5a030-117">Die Indexnummern für die Fehler Warteschlange beginnen mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5a030-117">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="5a030-118">Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="5a030-118">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="5a030-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a030-119">Examples</span></span>

<span data-ttu-id="5a030-120">Der *Fehler* wird im folgenden JScript-Beispiel verwendet. **Item** -Objekt in einem Ereignishandler, um den Benutzer auf den letzten Fehler aufmerksam zu machen.</span><span class="sxs-lookup"><span data-stu-id="5a030-120">The following JScript example uses the *Error*.**item** object in an event handler to alert the user to the most recent error.</span></span> <span data-ttu-id="5a030-121">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a030-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a><span data-ttu-id="5a030-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a030-122">Requirements</span></span>



| <span data-ttu-id="5a030-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a030-123">Requirement</span></span> | <span data-ttu-id="5a030-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5a030-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a030-125">Version</span><span class="sxs-lookup"><span data-stu-id="5a030-125">Version</span></span><br/> | <span data-ttu-id="5a030-126">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5a030-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5a030-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5a030-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a030-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a030-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a030-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a030-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a030-130">**Error-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5a030-130">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="5a030-131">**ErrorItem-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5a030-131">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





