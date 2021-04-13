---
title: Auflisten von Schriftarten
description: In dieser Übersicht wird gezeigt, wie die Schriftarten in der System Schriftart Auflistung nach dem Familiennamen aufgelistet werden.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9db05deb6b367f1392151ac8c12f2792d6e34f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390604"
---
# <a name="how-to-enumerate-fonts"></a><span data-ttu-id="aca35-103">Auflisten von Schriftarten</span><span class="sxs-lookup"><span data-stu-id="aca35-103">How to Enumerate Fonts</span></span>

<span data-ttu-id="aca35-104">In dieser Übersicht wird gezeigt, wie die Schriftarten in der System Schriftart Auflistung nach dem Familiennamen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="aca35-104">This overview will show how to enumerate the fonts in the system font collection, by family name.</span></span>

<span data-ttu-id="aca35-105">Diese Übersicht besteht aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="aca35-105">This overview consists of the following parts:</span></span>

-   [<span data-ttu-id="aca35-106">Schritt 1: Holen Sie sich die System Schriftart Auflistung.</span><span class="sxs-lookup"><span data-stu-id="aca35-106">Step 1: Get the System Font Collection.</span></span>](#step-1-get-the-system-font-collection)
-   [<span data-ttu-id="aca35-107">Schritt 2: erhalten Sie die Anzahl der Schriftfamilien.</span><span class="sxs-lookup"><span data-stu-id="aca35-107">Step 2: Get the Font Family Count.</span></span>](#step-2-get-the-font-family-count)
-   [<span data-ttu-id="aca35-108">Erstellen Sie eine for-Schleife.</span><span class="sxs-lookup"><span data-stu-id="aca35-108">Make a For Loop.</span></span>](#make-a-for-loop)
    -   [<span data-ttu-id="aca35-109">Schritt 3: Holen Sie sich die Schriftfamilie.</span><span class="sxs-lookup"><span data-stu-id="aca35-109">Step 3: Get the Font Family.</span></span>](#step-3-get-the-font-family)
    -   [<span data-ttu-id="aca35-110">Schritt 4: Holen Sie sich die Familiennamen.</span><span class="sxs-lookup"><span data-stu-id="aca35-110">Step 4: Get the Family Names.</span></span>](#step-4-get-the-family-names)
    -   [<span data-ttu-id="aca35-111">Schritt 5: Suchen Sie den Namen des Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="aca35-111">Step 5: Find the Locale Name.</span></span>](#step-5-find-the-locale-name)
    -   [<span data-ttu-id="aca35-112">Schritt 6: gibt die Länge der Zeichen folgen Länge für den Familiennamen und die Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="aca35-112">Step 6: Get the Length of the Family Name String Length and the String.</span></span>](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [<span data-ttu-id="aca35-113">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="aca35-113">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="aca35-114">Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="aca35-114">Example Code</span></span>](#example-code)

## <a name="step-1-get-the-system-font-collection"></a><span data-ttu-id="aca35-115">Schritt 1: Holen Sie sich die System Schriftart Auflistung.</span><span class="sxs-lookup"><span data-stu-id="aca35-115">Step 1: Get the System Font Collection.</span></span>

<span data-ttu-id="aca35-116">Verwenden Sie die [**getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) -Methode, die von der DirectWrite-Factory bereitgestellt wird, um eine [**idwrite-FontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) mit allen darin enthaltenen System Schriftarten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="aca35-116">Use the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method provided by the DirectWrite Factory to return an [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) with all of the system fonts in it.</span></span>


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a><span data-ttu-id="aca35-117">Schritt 2: erhalten Sie die Anzahl der Schriftfamilien.</span><span class="sxs-lookup"><span data-stu-id="aca35-117">Step 2: Get the Font Family Count.</span></span>

<span data-ttu-id="aca35-118">Anschließend können Sie die Anzahl der Schriftfamilien aus der Schriftart Auflistung mithilfe von [**idschreitefontcollection:: getfontfamilycount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount)erhalten.</span><span class="sxs-lookup"><span data-stu-id="aca35-118">Next, get the font family count from the font collection by using [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span></span> <span data-ttu-id="aca35-119">Wir verwenden diese, um jede Schriftfamilie in der Auflistung zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="aca35-119">We'll use this to loop over each font family in the collection.</span></span>


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a><span data-ttu-id="aca35-120">Erstellen Sie eine for-Schleife.</span><span class="sxs-lookup"><span data-stu-id="aca35-120">Make a For Loop.</span></span>


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



<span data-ttu-id="aca35-121">Nachdem Sie nun über die Schriftart Auflistung und die Anzahl der Schriftart verfügen, werden die verbleibenden Schritte über jede Schriftfamilie geführt, das [**idschreitefontfamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) -Objekt abgerufen und abgefragt.</span><span class="sxs-lookup"><span data-stu-id="aca35-121">Now that you have the font collection and the font count, the remaining steps loop over each font family, retrieving the [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object and querying it.</span></span>

### <a name="step-3-get-the-font-family"></a><span data-ttu-id="aca35-122">Schritt 3: Holen Sie sich die Schriftfamilie.</span><span class="sxs-lookup"><span data-stu-id="aca35-122">Step 3: Get the Font Family.</span></span>

<span data-ttu-id="aca35-123">Zum Aufrufen eines [**idwrite-FontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) -Objekts verwenden Sie [**idschreitefontcollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) , und übergeben Sie dabei den aktuellen Index *i*.</span><span class="sxs-lookup"><span data-stu-id="aca35-123">Get a [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object by using [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) and passing it the current index, *i*.</span></span>


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a><span data-ttu-id="aca35-124">Schritt 4: Holen Sie sich die Familiennamen.</span><span class="sxs-lookup"><span data-stu-id="aca35-124">Step 4: Get the Family Names.</span></span>

<span data-ttu-id="aca35-125">Sie erhalten die Namen der Schriftfamilie mithilfe von [**idschreitefontfamily:: getfamilynames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span><span class="sxs-lookup"><span data-stu-id="aca35-125">Get the font family names by using the [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span></span> <span data-ttu-id="aca35-126">Dabei handelt es sich um ein [**idwrite-ocalizedstrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="aca35-126">This is an [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) object.</span></span> <span data-ttu-id="aca35-127">Es können mehrere lokalisierte Versionen des Familiennamens für die Schriftfamilie vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="aca35-127">It can have multiple localized versions of the family name for the font family.</span></span>


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a><span data-ttu-id="aca35-128">Schritt 5: Suchen Sie den Namen des Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="aca35-128">Step 5: Find the Locale Name.</span></span>

<span data-ttu-id="aca35-129">Verwenden Sie die [**idwrite-ocalizedstrings:: findlocalename**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) -Methode, um den Namen der Schriftart Famliy im gewünschten Gebiets Schema zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aca35-129">Get the font famliy name in the locale you want by using the [**IDWriteLocalizedStrings::FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) method.</span></span> <span data-ttu-id="aca35-130">In diesem Fall wird zuerst das Standard Gebiets Schema abgerufen und angefordert.</span><span class="sxs-lookup"><span data-stu-id="aca35-130">In this case, first the default locale is retrieved and requested.</span></span> <span data-ttu-id="aca35-131">Wenn dies nicht funktioniert, wird das Gebiets Schema "en-US" angefordert.</span><span class="sxs-lookup"><span data-stu-id="aca35-131">If that does not work, the "en-us" locale is requested.</span></span> <span data-ttu-id="aca35-132">Wenn keines der angegebenen Gebiets Schemas gefunden wird, greift dieses Beispiel einfach auf den Index 0 zurück, das erste verfügbare Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="aca35-132">If either of the specified locales are not found, this example simply falls back to index 0, the first available locale.</span></span>


```C++
UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;
```



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a><span data-ttu-id="aca35-133">Schritt 6: gibt die Länge der Zeichen folgen Länge für den Familiennamen und die Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="aca35-133">Step 6: Get the Length of the Family Name String Length and the String.</span></span>

<span data-ttu-id="aca35-134">Zum Schluss wird die Länge der Zeichenfolge für den Familiennamen mithilfe von " [**idwrite telocalizedstrings:: GetStringLength" abgerufen**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span><span class="sxs-lookup"><span data-stu-id="aca35-134">Finally, get the length of the family name string by using [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span></span> <span data-ttu-id="aca35-135">Verwenden Sie diese Länge, um eine Zeichenfolge zu zuordnen, die groß genug ist, um den Namen aufzunehmen, und dann den Namen der Schriftfamilie mit [**idschreitelocalizedstrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aca35-135">Use this length to allocate a string large enough to hold the name and then get the font family name by using [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span></span>


```C++
UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}
```



## <a name="conclusion"></a><span data-ttu-id="aca35-136">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="aca35-136">Conclusion</span></span>

<span data-ttu-id="aca35-137">Nachdem Sie den Familiennamen oder die Namen im Gebiets Schema eingegeben haben, können Sie Sie für den Benutzer auflisten oder an "kreatetextformat" übergeben, um mit der Formatierung von Text mit der angegebenen Schriftfamilie zu beginnen, usw.</span><span class="sxs-lookup"><span data-stu-id="aca35-137">Once you have the family name or names in the locale, you can list them for the user to choose from, or pass it to CreateTextFormat to begin formatting text with the specified font family, and so on.</span></span>

## <a name="example-code"></a><span data-ttu-id="aca35-138">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="aca35-138">Example Code</span></span>

<span data-ttu-id="aca35-139">Den vollständigen Quellcode für dieses Beispiel finden Sie unter [Beispiel für Schriftart-Enumeration](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="aca35-139">To see the full source code for this example see the [Font Enumeration Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

 

 