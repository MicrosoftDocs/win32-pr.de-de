---
title: Closedcaption. samifilename
description: Die samifilename-Eigenschaft gibt den Namen der Datei an, die die für den Untertitel erforderlichen Informationen enthält, oder ruft ihn ab.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- Closedcaption. samifilename-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364896"
---
# <a name="closedcaptionsamifilename"></a><span data-ttu-id="fcfd9-104">Closedcaption. samifilename</span><span class="sxs-lookup"><span data-stu-id="fcfd9-104">ClosedCaption.SAMIFileName</span></span>

<span data-ttu-id="fcfd9-105">Die **samifilename** -Eigenschaft gibt den Namen der Datei an, die die für den Untertitel erforderlichen Informationen enthält, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-105">The **SAMIFileName** property specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a><span data-ttu-id="fcfd9-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="fcfd9-106">Possible Values</span></span>

<span data-ttu-id="fcfd9-107">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcfd9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcfd9-108">Remarks</span></span>

<span data-ttu-id="fcfd9-109">Die in der Synchronisierung verfügbare Medienaustausch Datei (Sami) muss eine SMI-oder. Sami-Dateinamenerweiterung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-109">The Synchronized Accessible Media Interchange (SAMI) file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="fcfd9-110">Wenn Sie keinen Wert für **samifilename** angeben, ruft diese Eigenschaft eine Zeichenfolge ab, die den Dateinamen oder die URL enthält, die dem aktuellen Medien Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-110">If you don't specify a value for **SAMIFileName**, this property retrieves a string containing the file name or URL associated with the current media item.</span></span> <span data-ttu-id="fcfd9-111">Diese Zuordnung kann auftreten, wenn eine Sami-Datei mithilfe des *Sami* URL-Parameters angegeben wird, oder automatisch, wenn die Sami-Datei den gleichen Namen hat wie der Name der digitalen Mediendatei (mit Ausnahme der Dateinamenerweiterung).</span><span class="sxs-lookup"><span data-stu-id="fcfd9-111">This association can occur when a SAMI file is specified using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file name (except for the file name extension).</span></span> <span data-ttu-id="fcfd9-112">Wenn dem aktuellen Medium keine samische Datei zugeordnet ist, ruft diese Eigenschaft eine leere Zeichenfolge ("") ab.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-112">If there is no SAMI file associated with the current media, this property retrieves an empty string ("").</span></span>

<span data-ttu-id="fcfd9-113">Nachdem Sie einen Wert für **samifilename** angegeben haben, wird dieser Wert beibehalten, bis Sie einen neuen Wert angeben (oder bis ein neues Medien Element mithilfe des *Sami* URL-Parameters geöffnet wird).</span><span class="sxs-lookup"><span data-stu-id="fcfd9-113">Once you specify a value for **SAMIFileName**, that value persists until you specify a new value (or until a new media item is opened using the *sami* URL parameter).</span></span> <span data-ttu-id="fcfd9-114">Daher müssen Sie einen neuen Wert für diese Eigenschaft angeben, bevor Sie die einzelnen neuen Medienelemente wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-114">Therefore, you must specify a new value for this property before you play each new media item.</span></span> <span data-ttu-id="fcfd9-115">Auf diese Weise wird der neue Wert für **samifilename** wirksam, wenn das nächste Medien Element geöffnet wird (oder wenn *Player*.**Close** wird aufgerufen.)</span><span class="sxs-lookup"><span data-stu-id="fcfd9-115">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when *Player*.**close** is called).</span></span> <span data-ttu-id="fcfd9-116">Das Angeben eines neuen Werts für **samifilename** hat keine Auswirkung auf das aktuelle Medium.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-116">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="fcfd9-117">Um zu bewirken, dass Windows Media Player die mit einem bestimmten Medien Element verknüpfte Sami-Datei zurückgibt, geben Sie einen Wert für **samifilename** an, der einer leeren Zeichenfolge ("") entspricht, bevor Sie das nächste Medien Element wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-117">To cause Windows Media Player to return to using the SAMI file associated with a particular media item, specify a value for **SAMIFileName** equal to an empty string ("") before you play the next media item.</span></span>

<span data-ttu-id="fcfd9-118">**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-118">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="fcfd9-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcfd9-119">Examples</span></span>

<span data-ttu-id="fcfd9-120">In den folgenden drei JScript-Beispielen wird *closedcaption* verwendet. **Samifilename** zum Angeben des Namens einer Textdatei mit geschlossener Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-120">The following three JScript examples use *ClosedCaption*.**SAMIFileName** to specify the name of a closed caption text file.</span></span> <span data-ttu-id="fcfd9-121">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a><span data-ttu-id="fcfd9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcfd9-122">Requirements</span></span>



| <span data-ttu-id="fcfd9-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcfd9-123">Requirement</span></span> | <span data-ttu-id="fcfd9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fcfd9-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfd9-125">Version</span><span class="sxs-lookup"><span data-stu-id="fcfd9-125">Version</span></span><br/> | <span data-ttu-id="fcfd9-126">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fcfd9-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fcfd9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fcfd9-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="fcfd9-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcfd9-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcfd9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcfd9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcfd9-130">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="fcfd9-130">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="fcfd9-131">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="fcfd9-131">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="fcfd9-132">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="fcfd9-132">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





