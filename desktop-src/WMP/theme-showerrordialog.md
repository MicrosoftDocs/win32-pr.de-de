---
title: Design. showerrordialog
description: Die showerrordialog-Methode zeigt das Standardfehler Dialogfeld an.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- Design. showerrordialog-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367039"
---
# <a name="themeshowerrordialog"></a><span data-ttu-id="6d981-104">Design. showerrordialog</span><span class="sxs-lookup"><span data-stu-id="6d981-104">THEME.showErrorDialog</span></span>

<span data-ttu-id="6d981-105">Die **showerrordialog** -Methode zeigt das Standardfehler Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="6d981-105">The **showErrorDialog** method displays the standard error dialog box.</span></span>

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a><span data-ttu-id="6d981-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d981-106">Parameters</span></span>

<span data-ttu-id="6d981-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d981-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d981-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d981-108">Return Value</span></span>

<span data-ttu-id="6d981-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6d981-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d981-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d981-110">Remarks</span></span>

<span data-ttu-id="6d981-111">Wenn **Settings. enableerrordialogs** false ist, kann diese Methode verwendet werden, um das Fehler Dialogfeld Programm gesteuert anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6d981-111">If **Settings.enableErrorDialogs** is false, this method can be used to programmatically display the error dialog.</span></span> <span data-ttu-id="6d981-112">Wenn in der Fehler Warteschlange keine Fehler vorliegen, wird das Fehler Dialogfeld nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d981-112">If there are no errors in the error queue, the error dialog box is not shown.</span></span>

<span data-ttu-id="6d981-113">Für Windows Media Player 9-Serie oder höher muss diese Methode vom Fehler Ereignishandler aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d981-113">For Windows Media Player 9 Series or later, this method must be called from the error event handler.</span></span> <span data-ttu-id="6d981-114">Windows Media Player 9 oder höher löscht die Fehler Warteschlange für Skins, nachdem das Fehler Ereignis ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6d981-114">Windows Media Player 9 Series or later clears the error queue for skins after the error event has been fired.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d981-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d981-115">Requirements</span></span>



| <span data-ttu-id="6d981-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d981-116">Requirement</span></span> | <span data-ttu-id="6d981-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6d981-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6d981-118">Version</span><span class="sxs-lookup"><span data-stu-id="6d981-118">Version</span></span><br/> | <span data-ttu-id="6d981-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6d981-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d981-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d981-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d981-121">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="6d981-121">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="6d981-122">**Settings. enableerrordialogs**</span><span class="sxs-lookup"><span data-stu-id="6d981-122">**Settings.enableErrorDialogs**</span></span>](settings-enableerrordialogs.md)
</dt> </dl>

 

 





