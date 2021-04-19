---
title: Lesen von Attributwerten
description: Lesen von Attributwerten
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, Lesen von Werten
- Lesen von Attributwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339008"
---
# <a name="reading-attribute-values"></a><span data-ttu-id="9c229-114">Lesen von Attributwerten</span><span class="sxs-lookup"><span data-stu-id="9c229-114">Reading Attribute Values</span></span>

<span data-ttu-id="9c229-115">Die Attribute, die Sie in der Bibliothek und in Windows Media-Dateien finden, haben vordefinierte Namen.</span><span class="sxs-lookup"><span data-stu-id="9c229-115">The attributes you can find in the library and in Windows Media files have predefined names.</span></span> <span data-ttu-id="9c229-116">Sie können Code schreiben, der den Wert eines Attributs abruft, indem er den Namen dieses Attributs an *Medien* übergibt. **getiteminfo** oder *Medium*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="9c229-116">You can write code that retrieves the value of one attribute by passing the name of that attribute to *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="9c229-117">Sie können auch Code schreiben, der die Werte aller Attribute in einer Datei oder einem Element abruft.</span><span class="sxs-lookup"><span data-stu-id="9c229-117">You can also write code that retrieves the values of all of the attributes in a file or item.</span></span>

<span data-ttu-id="9c229-118">Im folgenden c#-Beispiel wird der Wert des **Title** -Attributs abgerufen und in einem Meldungs Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c229-118">The following C# example retrieves the value of the **Title** attribute and displays it in a message box.</span></span> <span data-ttu-id="9c229-119">In diesem Beispiel wurde das **Player** -Objekt als AxWMPLib. AxWindowsMediaPlayer Player definiert.</span><span class="sxs-lookup"><span data-stu-id="9c229-119">In this example, the **Player** object was defined as axWMPLib.AxWindowsMediaPlayer Player.</span></span>


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



<span data-ttu-id="9c229-120">Beim Aufrufen von **getItemInfoByType** ist der zweite Parameter eine Zeichenfolge, die die Sprache angibt.</span><span class="sxs-lookup"><span data-stu-id="9c229-120">In the call to **getItemInfoByType**, the second parameter is a string that specifies the language.</span></span> <span data-ttu-id="9c229-121">Wenn Sie wie in diesem Beispiel gezeigt eine leere Zeichenfolge übergeben, ruft die-Methode den-Wert in der Standardsprache ab.</span><span class="sxs-lookup"><span data-stu-id="9c229-121">If you pass an empty string as shown in this example, the method retrieves the value in the default language.</span></span> <span data-ttu-id="9c229-122">Weitere Informationen zum dritten Parameter finden Sie unter [Attribute mit mehreren Werten](attributes-with-multiple-values.md).</span><span class="sxs-lookup"><span data-stu-id="9c229-122">For information about the third parameter, see [Attributes with Multiple Values](attributes-with-multiple-values.md).</span></span>

<span data-ttu-id="9c229-123">Im folgenden c#-Beispiel werden die Werte für ein bestimmtes Attribut im aktuellen Medien Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9c229-123">The following C# example retrieves the values for a given attribute in the current media item.</span></span> <span data-ttu-id="9c229-124">Diese Werte werden als eine durch Semikolons getrennte Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c229-124">It returns these values as a semicolon-delimited string.</span></span> <span data-ttu-id="9c229-125">Beachten Sie, dass bei Attributen, die als-Objekte dargestellt werden, wie z. b. **WM/ \_ liedsynchron**, **WM/Bild** und **WM/userweburl**, die-Funktion eine leere Zeichenfolge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9c229-125">Note that for attributes represented as objects, such as **WM/Lyrics\_Synchronised**, **WM/Picture**, and **WM/UserWebURL**, the function returns an empty string.</span></span>


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



<span data-ttu-id="9c229-126">Das dritte Argument, das an die **getItemInfoByType** -Methode übermittelt wird, ist der Index eines bestimmten Attributs in einem Attribut Satz mit demselben Namen.</span><span class="sxs-lookup"><span data-stu-id="9c229-126">The third argument passed to the **getItemInfoByType** method is the index of a particular attribute in a set of attributes with the same name.</span></span>

<span data-ttu-id="9c229-127">Sie können ähnlichen Code verwenden, um Attribute abzurufen, die eindeutige Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9c229-127">You can use similar code to retrieve attributes that have unique names.</span></span> <span data-ttu-id="9c229-128">In diesen Fällen gibt **getattributezähltbytype** den Wert 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="9c229-128">In those cases, **getAttributeCountByType** returns 1.</span></span> <span data-ttu-id="9c229-129">Im obigen Beispiel wird der aufzurufende " **getItemInfoByType** " nur einmal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c229-129">In the example shown earlier, the call to **getItemInfoByType** would execute only once.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c229-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c229-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c229-131">**Ändern von Attributwerten**</span><span class="sxs-lookup"><span data-stu-id="9c229-131">**Changing Attribute Values**</span></span>](changing-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="9c229-132">**Medien Element Attribute**</span><span class="sxs-lookup"><span data-stu-id="9c229-132">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="9c229-133">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="9c229-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="9c229-134">**Lesen von Attributwerten von einer CD oder DVD**</span><span class="sxs-lookup"><span data-stu-id="9c229-134">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




