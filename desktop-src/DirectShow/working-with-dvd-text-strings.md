---
description: Arbeiten mit DVD-Text Zeichenfolgen
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Arbeiten mit DVD-Text Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368174"
---
# <a name="working-with-dvd-text-strings"></a><span data-ttu-id="e4fd4-103">Arbeiten mit DVD-Text Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="e4fd4-103">Working with DVD Text Strings</span></span>

<span data-ttu-id="e4fd4-104">Einige DVD-Datenträger, insbesondere CDs-Datenträger, enthalten möglicherweise eine Liste mit Text Zeichenfolgen, um den Video-oder Audioinhalt zu ergänzen</span><span class="sxs-lookup"><span data-stu-id="e4fd4-104">Some DVD discs, especially karaoke discs, might contain a list of text strings to supplement the video or audio content.</span></span> <span data-ttu-id="e4fd4-105">Diese Text Zeichenfolgen enthalten Metadaten zum Inhalt, z. b. Titel Titel, Künstlernamen, Genre Informationen usw.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-105">These text strings contain metadata about the content, such as song titles, artist names, genre information, and so on.</span></span> <span data-ttu-id="e4fd4-106">Text Zeichenfolgen können in mehr als einer Sprache vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-106">Text strings can be present in more than one language.</span></span> <span data-ttu-id="e4fd4-107">Diese Zeichen folgen sind optional, und viele CDs verfügen nicht über diese Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-107">These strings are optional, and many discs do not have them.</span></span>

<span data-ttu-id="e4fd4-108">Wenn Sie Text Zeichenfolgen aus einer DVD abrufen möchten, verwenden Sie die [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Schnittstelle, die vom [DVD-Navigator](dvd-navigator-filter.md)verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-108">To retrieve text strings from a DVD, use the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interface, which is exposed by the [DVD Navigator](dvd-navigator-filter.md).</span></span> <span data-ttu-id="e4fd4-109">Es ist nicht erforderlich, ein DVD-Wiedergabe Diagramm zu erstellen, um die Text Zeichenfolgen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-109">You do not actually need to build a DVD playback graph to retrieve the text strings.</span></span> <span data-ttu-id="e4fd4-110">Sie können einfach den DVD-Navigator erstellen, das DVD-Volume festlegen und dann die entsprechenden Textzeichen folgen Methoden aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="e4fd4-110">You can simply create the DVD Navigator, set the DVD volume, and then call the relevant text-string methods:</span></span>



| <span data-ttu-id="e4fd4-111">Methode</span><span class="sxs-lookup"><span data-stu-id="e4fd4-111">Method</span></span>                                                                                  | <span data-ttu-id="e4fd4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4fd4-112">Description</span></span>                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4fd4-113">**IDvdInfo2:: getdvdtextnumoflanguages**</span><span class="sxs-lookup"><span data-stu-id="e4fd4-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | <span data-ttu-id="e4fd4-114">Ruft die Anzahl der Sprachen ab, für die Text Zeichenfolgen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-114">Gets the number of languages for which there are text strings.</span></span>                                                                                                                                  |
| [<span data-ttu-id="e4fd4-115">**IDvdInfo2:: getdvdtextlanguageinfo**</span><span class="sxs-lookup"><span data-stu-id="e4fd4-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | <span data-ttu-id="e4fd4-116">Ruft Informationen zu den Text Zeichenfolgen für eine Sprache ab.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-116">Gets information about the text strings for one language.</span></span>                                                                                                                                       |
| [<span data-ttu-id="e4fd4-117">**IDvdInfo2:: getdvdtextstringasunicode**</span><span class="sxs-lookup"><span data-stu-id="e4fd4-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | <span data-ttu-id="e4fd4-118">Ruft eine Text Zeichenfolge für eine angegebene Sprache nach Index ab.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-118">Gets a text string for a specified language, by index.</span></span>                                                                                                                                          |
| [<span data-ttu-id="e4fd4-119">**IDvdInfo2:: getdvdtextstringasnative**</span><span class="sxs-lookup"><span data-stu-id="e4fd4-119">**IDvdInfo2::GetDVDTextStringAsNative**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | <span data-ttu-id="e4fd4-120">Ruft eine Text Zeichenfolge als rohbytearray ab.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-120">Gets a text string as a raw byte array.</span></span> <span data-ttu-id="e4fd4-121">Verwenden Sie diese Methode, wenn die Text Zeichenfolge eine Zeichencodierung verwendet, die von [**getdvdtextstringasunicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-121">Use this method if the text string uses a character encoding not supported by [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span></span> |



 

<span data-ttu-id="e4fd4-122">Dies ist das grundlegende Verfahren zum erhalten von Text Zeichenfolgen:</span><span class="sxs-lookup"><span data-stu-id="e4fd4-122">Here is the basic procedure for getting text strings:</span></span>

1.  <span data-ttu-id="e4fd4-123">Aufrufen von [**IDvdInfo2:: getdvdtextnumoflanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) zum Ermitteln der Gesamtzahl der Sprachen, in denen die Text Zeichenfolgen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-123">Call [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) to find the total number of languages in which the text strings appear.</span></span> <span data-ttu-id="e4fd4-124">Wenn die Zahl 0 (null) ist, bedeutet dies, dass die DVD keine Text Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-124">If the number is zero, it means the DVD does not have any text strings.</span></span> <span data-ttu-id="e4fd4-125">(Dies ist möglicherweise der häufigste Fall.)</span><span class="sxs-lookup"><span data-stu-id="e4fd4-125">(This is perhaps the most common case, in fact.)</span></span>
2.  <span data-ttu-id="e4fd4-126">Wenn die Anzahl der Sprachen mindestens 1 ist, wenden Sie sich an [**IDvdInfo2:: getdvdtextlanguageinfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) , um Informationen zu den einzelnen Sprachen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-126">If the number of languages is at least one, call [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) to get information about each language.</span></span> <span data-ttu-id="e4fd4-127">Die Sprache wird durch den Index angegeben.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-127">The language is specified by index.</span></span> <span data-ttu-id="e4fd4-128">Die-Methode gibt die Gesamtanzahl von Text Zeichenfolgen in dieser Sprache, den Gebiets Schema Bezeichner (**LCID**) für die Sprache und die Zeichencodierung (Unicode oder andere) zurück.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-128">The method returns the total number of text strings in that language, the locale identifier (**LCID**) for the language, and the character encoding (Unicode or other).</span></span> <span data-ttu-id="e4fd4-129">Für DVD-Text Zeichenfolgen können mehrere verschiedene Zeichensätze verwendet werden. Diese werden in der [**DVD- \_ textcharset-Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset)aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-129">DVD text strings can use several different character sets; these are listed in [**DVD\_TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span></span>
3.  <span data-ttu-id="e4fd4-130">Um eine Text Zeichenfolge abzurufen, wenden Sie [**IDvdInfo2:: getdvdtextstringasunicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) oder [**IDvdInfo2:: getdvdtextstringasnative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)an.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-130">To get a text string, call [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) or [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span></span> <span data-ttu-id="e4fd4-131">Die erste Methode gibt eine Zeichenfolge mit breit Zeichen zurück, unterstützt jedoch nicht jeden Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-131">The first method returns a wide-character string, but does not support every character set.</span></span> <span data-ttu-id="e4fd4-132">Die zweite Methode gibt ein Bytearray zurück, das die unformatierten Textdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-132">The second method returns a byte array containing the raw text data.</span></span> <span data-ttu-id="e4fd4-133">Für beide Methoden können Sie die-Methode mit einem **null** -Puffer Zeiger aufzurufen, um die Größe der Zeichenfolge und den Texttyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-133">For both methods, you can call the method with a **NULL** buffer pointer to find the size of the string and the text type.</span></span> <span data-ttu-id="e4fd4-134">Weisen Sie dann einen Puffer zu, und wiederholen Sie die Methode, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-134">Then allocate a buffer and call the method again to get the string.</span></span>

<span data-ttu-id="e4fd4-135">Jede Text Zeichenfolge verfügt über einen zugeordneten bezeichnercode, der die Bedeutung der Text Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-135">Each text string has an associated identifier code, which indicates the meaning of the text string.</span></span> <span data-ttu-id="e4fd4-136">Der Bezeichner wird als ein [**DVD- \_ textstringtype**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-136">The identifier is returned as a [**DVD\_TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) value.</span></span> <span data-ttu-id="e4fd4-137">Es gibt zwei Kategorien von *Bezeichnern*: *Struktur* Bezeichner und Inhalts Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-137">There are two categories of identifier: *structure identifiers* and *content identifiers*.</span></span> <span data-ttu-id="e4fd4-138">Struktur Bezeichner verfügen über numerische Codes im Bereich 0x00 – 0x02f.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-138">Structure identifiers have numeric codes in the range 0x00–0x02F.</span></span> <span data-ttu-id="e4fd4-139">Inhalts Bezeichner haben einen Bereich von 0x30 und höher.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-139">Content identifiers have a range of 0x30 and higher.</span></span> <span data-ttu-id="e4fd4-140">(Die **DVD- \_ textstringtype** -Enumeration definiert eine Teilmenge der gängigsten Bezeichner, aber die [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Methoden können jeden bezeichnercode zurückgeben.) Ein Struktur Bezeichner beschreibt einen logischen Teil der DVD, z. b. Volume, Titel oder Teil des Titels (PTT).</span><span class="sxs-lookup"><span data-stu-id="e4fd4-140">(The **DVD\_TextStringType** enumeration defines a subset of the most common identifiers, but the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods can return any identifier code.) A structure identifier describes a logical portion of the DVD, such as volume, title, or part of title (PTT).</span></span> <span data-ttu-id="e4fd4-141">Ein Inhalts Bezeichner gibt die Bedeutung einer bestimmten Text Zeichenfolge an, z. b. Filmtitel, Titel oder Genre.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-141">A content identifier indicates the meaning of a particular text string, such as movie title, song title, or genre.</span></span>

<span data-ttu-id="e4fd4-142">Struktur Bezeichner sind keine Text Zeichenfolgen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-142">Structure identifiers do not have associated text strings.</span></span> <span data-ttu-id="e4fd4-143">Wenn ein Struktur Bezeichner in den Text Zeichenfolgen-Daten angezeigt wird, signalisiert er, dass die folgenden Text Zeichenfolgen für diesen logischen Teil der DVD gelten, bis zum nächsten Struktur Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-143">When a structure identifier appears in the text-string data, it signals that the following text strings apply to that logical portion of the DVD, up until the next structure identifier.</span></span> <span data-ttu-id="e4fd4-144">Die Position der Struktur Bezeichner innerhalb der Textdaten entspricht der logischen Hierarchie des DVD-Volumes.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-144">The position of the structure identifiers within the text data corresponds to the logical hierarchy of the DVD volume.</span></span> <span data-ttu-id="e4fd4-145">Beispielsweise stellt das erste Vorkommen des DVD- \_ Struktur \_ Titel Bezeichners (0x02) den ersten Titel im Volume dar, und das nächste Vorkommen stellt den zweiten Titel dar.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-145">For example, the first occurrence of the DVD\_Struct\_Title identifier (0x02) represents the first title in the volume, and the next occurrence represents the second title.</span></span>

<span data-ttu-id="e4fd4-146">In der folgenden Tabelle wird gezeigt, wie die Text Zeichenfolgen für eine DVD mit zwei Titeln definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-146">The following table shows how the text strings might be defined for a DVD with two titles.</span></span>



| <span data-ttu-id="e4fd4-147">DVD- \_ textstringtype</span><span class="sxs-lookup"><span data-stu-id="e4fd4-147">DVD\_TextStringType</span></span>        | <span data-ttu-id="e4fd4-148">Textzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e4fd4-148">Text string</span></span>  | <span data-ttu-id="e4fd4-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4fd4-149">Description</span></span>                                    |
|----------------------------|--------------|------------------------------------------------|
| <span data-ttu-id="e4fd4-150">DVD- \_ Struktur \_ Volume (0x01)</span><span class="sxs-lookup"><span data-stu-id="e4fd4-150">DVD\_Struct\_Volume (0x01)</span></span> | <span data-ttu-id="e4fd4-151">""</span><span class="sxs-lookup"><span data-stu-id="e4fd4-151">""</span></span>           | <span data-ttu-id="e4fd4-152">Struktur Bezeichner für die gesamte Seiten Seite.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-152">Structure identifier for the entire disc side.</span></span> |
| <span data-ttu-id="e4fd4-153">Allgemeiner DVD- \_ \_ Name (0x30)</span><span class="sxs-lookup"><span data-stu-id="e4fd4-153">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="e4fd4-154">"DVD-Volume"</span><span class="sxs-lookup"><span data-stu-id="e4fd4-154">"DVD Volume"</span></span> | <span data-ttu-id="e4fd4-155">Der Name des DVD-Volumes.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-155">DVD volume name.</span></span>                               |
| <span data-ttu-id="e4fd4-156">Titel der DVD- \_ Struktur \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="e4fd4-156">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="e4fd4-157">""</span><span class="sxs-lookup"><span data-stu-id="e4fd4-157">""</span></span>           | <span data-ttu-id="e4fd4-158">Struktur Bezeichner für den ersten Titel.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-158">Structure identifier for the first title.</span></span>      |
| <span data-ttu-id="e4fd4-159">Allgemeiner DVD- \_ \_ Name (0x30)</span><span class="sxs-lookup"><span data-stu-id="e4fd4-159">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="e4fd4-160">"Titel 1"</span><span class="sxs-lookup"><span data-stu-id="e4fd4-160">"Title 1"</span></span>    | <span data-ttu-id="e4fd4-161">Der Name des ersten Titels.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-161">Name of the first title.</span></span>                       |
| <span data-ttu-id="e4fd4-162">Titel der DVD- \_ Struktur \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="e4fd4-162">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="e4fd4-163">""</span><span class="sxs-lookup"><span data-stu-id="e4fd4-163">""</span></span>           | <span data-ttu-id="e4fd4-164">Struktur Bezeichner für den zweiten Titel.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-164">Structure identifier for the second title.</span></span>     |
| <span data-ttu-id="e4fd4-165">Allgemeiner DVD- \_ \_ Name (0x30)</span><span class="sxs-lookup"><span data-stu-id="e4fd4-165">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="e4fd4-166">"Title 2"</span><span class="sxs-lookup"><span data-stu-id="e4fd4-166">"Title 2"</span></span>    | <span data-ttu-id="e4fd4-167">Der Name des zweiten Titels.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-167">Name of the second title.</span></span>                      |



 

<span data-ttu-id="e4fd4-168">Die Methoden [**getdvdtextstringasunicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) und [**getdvdtextstringasnative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) behandeln Struktur Bezeichner und Inhalts Bezeichner identisch.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-168">The [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) and [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) methods treat structure identifiers and content identifiers the same.</span></span> <span data-ttu-id="e4fd4-169">Der einzige Unterschied besteht darin, dass der zugeordnete Text Puffer für Struktur Bezeichner leer ist.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-169">The only difference is that for structure identifiers, the associated text buffer is empty.</span></span> <span data-ttu-id="e4fd4-170">Es liegt an der Anwendung, die Beziehung zwischen den Text Zeichenfolgen und den logischen Teilen der DVD nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-170">It is up to the application to keep track of the relationship between the text strings and the logical portions of the DVD.</span></span>

<span data-ttu-id="e4fd4-171">Im folgenden Beispiel wird gezeigt, wie Sie Text Zeichenfolgen aus einer DVD erhalten.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-171">The following example shows how to get text strings from a DVD.</span></span> <span data-ttu-id="e4fd4-172">In diesem Beispiel werden einige Details ignoriert, die für eine echte Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-172">This example ignores some details that a real application would require.</span></span> <span data-ttu-id="e4fd4-173">(Er ignoriert z. b. Struktur Bezeichner.) Das Beispiel dient nur dazu, die richtige Sequenz von Aufrufen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-173">(For example, it ignores structure identifiers.) The example is only meant to show the correct sequence of calls.</span></span>


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



<span data-ttu-id="e4fd4-174">Informationen zu DVD-Text Zeichenfolgen finden Sie auf der [Website des DVD-Forums](https://go.microsoft.com/fwlink/?LinkId=8677).</span><span class="sxs-lookup"><span data-stu-id="e4fd4-174">For information on DVD text strings, see the [DVD Forum's Web site](https://go.microsoft.com/fwlink/?LinkId=8677).</span></span>

<span data-ttu-id="e4fd4-175">Die **cdvdcore:: getdvdtext** -Methode in der dvdsample-Anwendung veranschaulicht die grundlegenden Schritte beim Auflisten und Anzeigen von DVD-Text Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="e4fd4-175">The **CDvdCore::GetDvdText** method in the DVDSample application demonstrates the basic steps in enumerating and displaying DVD text strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4fd4-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4fd4-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4fd4-177">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e4fd4-177">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



