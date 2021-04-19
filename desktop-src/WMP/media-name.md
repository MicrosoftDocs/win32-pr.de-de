---
title: Media.name
description: Die Name-Eigenschaft gibt den Namen des Medien Elements an oder ruft ihn ab.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.Name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368585"
---
# <a name="medianame"></a><span data-ttu-id="e3507-104">Media.name</span><span class="sxs-lookup"><span data-stu-id="e3507-104">Media.name</span></span>

<span data-ttu-id="e3507-105">Die **Name** -Eigenschaft gibt den Namen des Medien Elements an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e3507-105">The **name** property specifies or retrieves the name of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3507-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3507-106">Syntax</span></span>

<span data-ttu-id="e3507-107">*Player*. *currentMedia*. **Name**</span><span class="sxs-lookup"><span data-stu-id="e3507-107">*player*.*currentMedia*.**name**</span></span>

## <a name="possible-values"></a><span data-ttu-id="e3507-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e3507-108">Possible Values</span></span>

<span data-ttu-id="e3507-109">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge** , die den Namen des Medien Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="e3507-109">This property is a read/write **String** containing the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3507-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3507-110">Remarks</span></span>

<span data-ttu-id="e3507-111">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3507-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="e3507-112">Um den Wert dieser Eigenschaft anzugeben, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3507-112">To specify the value of this property, full access to the library is required.</span></span> <span data-ttu-id="e3507-113">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e3507-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e3507-114">Bevor Sie diese Methode verwenden, um den Namen eines Medien Elements anzugeben, verwenden Sie **isleseronlyitem** , um zu bestimmen, ob der Name festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3507-114">Before using this method to specify the name of a media item, use **isReadOnlyItem** to determine whether the name can be set.</span></span>

<span data-ttu-id="e3507-115">**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e3507-115">**Windows Media Player 10 Mobile:** This property is read-only.</span></span>

## <a name="examples"></a><span data-ttu-id="e3507-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3507-116">Examples</span></span>

<span data-ttu-id="e3507-117">Im folgenden JScript-Beispiel werden *Medien* verwendet. **Name** , um den Namen des aktuellen Medien Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e3507-117">The following JScript example uses *Media*.**name** to change the name of the current media item.</span></span> <span data-ttu-id="e3507-118">Mit einem HTML-Text Eingabe Element namens "NameText" kann der Benutzer eine Text Zeichenfolge für den neuen Namen eingeben.</span><span class="sxs-lookup"><span data-stu-id="e3507-118">An HTML TEXT input element named NameText allows the user to enter a text string for the new name.</span></span> <span data-ttu-id="e3507-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3507-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a><span data-ttu-id="e3507-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3507-120">Requirements</span></span>



| <span data-ttu-id="e3507-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3507-121">Requirement</span></span> | <span data-ttu-id="e3507-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e3507-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3507-123">Version</span><span class="sxs-lookup"><span data-stu-id="e3507-123">Version</span></span><br/> | <span data-ttu-id="e3507-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e3507-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e3507-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e3507-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="e3507-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3507-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3507-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3507-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3507-128">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="e3507-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e3507-129">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e3507-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e3507-130">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e3507-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





