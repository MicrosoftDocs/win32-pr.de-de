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
# <a name="how-to-enumerate-fonts"></a>Auflisten von Schriftarten

In dieser Übersicht wird gezeigt, wie die Schriftarten in der System Schriftart Auflistung nach dem Familiennamen aufgelistet werden.

Diese Übersicht besteht aus den folgenden Teilen:

-   [Schritt 1: Holen Sie sich die System Schriftart Auflistung.](#step-1-get-the-system-font-collection)
-   [Schritt 2: erhalten Sie die Anzahl der Schriftfamilien.](#step-2-get-the-font-family-count)
-   [Erstellen Sie eine for-Schleife.](#make-a-for-loop)
    -   [Schritt 3: Holen Sie sich die Schriftfamilie.](#step-3-get-the-font-family)
    -   [Schritt 4: Holen Sie sich die Familiennamen.](#step-4-get-the-family-names)
    -   [Schritt 5: Suchen Sie den Namen des Gebiets Schemas.](#step-5-find-the-locale-name)
    -   [Schritt 6: gibt die Länge der Zeichen folgen Länge für den Familiennamen und die Zeichenfolge an.](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [Zusammenfassung](#conclusion)
-   [Beispiel Code](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>Schritt 1: Holen Sie sich die System Schriftart Auflistung.

Verwenden Sie die [**getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) -Methode, die von der DirectWrite-Factory bereitgestellt wird, um eine [**idwrite-FontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) mit allen darin enthaltenen System Schriftarten zurückzugeben.


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>Schritt 2: erhalten Sie die Anzahl der Schriftfamilien.

Anschließend können Sie die Anzahl der Schriftfamilien aus der Schriftart Auflistung mithilfe von [**idschreitefontcollection:: getfontfamilycount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount)erhalten. Wir verwenden diese, um jede Schriftfamilie in der Auflistung zu durchlaufen.


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>Erstellen Sie eine for-Schleife.


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



Nachdem Sie nun über die Schriftart Auflistung und die Anzahl der Schriftart verfügen, werden die verbleibenden Schritte über jede Schriftfamilie geführt, das [**idschreitefontfamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) -Objekt abgerufen und abgefragt.

### <a name="step-3-get-the-font-family"></a>Schritt 3: Holen Sie sich die Schriftfamilie.

Zum Aufrufen eines [**idwrite-FontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) -Objekts verwenden Sie [**idschreitefontcollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) , und übergeben Sie dabei den aktuellen Index *i*.


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>Schritt 4: Holen Sie sich die Familiennamen.

Sie erhalten die Namen der Schriftfamilie mithilfe von [**idschreitefontfamily:: getfamilynames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames). Dabei handelt es sich um ein [**idwrite-ocalizedstrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) -Objekt. Es können mehrere lokalisierte Versionen des Familiennamens für die Schriftfamilie vorhanden sein.


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>Schritt 5: Suchen Sie den Namen des Gebiets Schemas.

Verwenden Sie die [**idwrite-ocalizedstrings:: findlocalename**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) -Methode, um den Namen der Schriftart Famliy im gewünschten Gebiets Schema zu erhalten. In diesem Fall wird zuerst das Standard Gebiets Schema abgerufen und angefordert. Wenn dies nicht funktioniert, wird das Gebiets Schema "en-US" angefordert. Wenn keines der angegebenen Gebiets Schemas gefunden wird, greift dieses Beispiel einfach auf den Index 0 zurück, das erste verfügbare Gebiets Schema.


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



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a>Schritt 6: gibt die Länge der Zeichen folgen Länge für den Familiennamen und die Zeichenfolge an.

Zum Schluss wird die Länge der Zeichenfolge für den Familiennamen mithilfe von " [**idwrite telocalizedstrings:: GetStringLength" abgerufen**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength). Verwenden Sie diese Länge, um eine Zeichenfolge zu zuordnen, die groß genug ist, um den Namen aufzunehmen, und dann den Namen der Schriftfamilie mit [**idschreitelocalizedstrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring)zu erhalten.


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



## <a name="conclusion"></a>Zusammenfassung

Nachdem Sie den Familiennamen oder die Namen im Gebiets Schema eingegeben haben, können Sie Sie für den Benutzer auflisten oder an "kreatetextformat" übergeben, um mit der Formatierung von Text mit der angegebenen Schriftfamilie zu beginnen, usw.

## <a name="example-code"></a>Beispielcode

Den vollständigen Quellcode für dieses Beispiel finden Sie unter [Beispiel für Schriftart-Enumeration](/samples/browse/?redirectedfrom=MSDN-samples).

 

 