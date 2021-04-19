---
description: In diesem Artikel wird beschrieben, wie der Filter Graph-Manager einen Quell Filter anhand eines Datei namens eingibt.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrieren eines benutzerdefinierten Dateityps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342547"
---
# <a name="registering-a-custom-file-type"></a><span data-ttu-id="7adce-103">Registrieren eines benutzerdefinierten Dateityps</span><span class="sxs-lookup"><span data-stu-id="7adce-103">Registering a Custom File Type</span></span>

<span data-ttu-id="7adce-104">In diesem Artikel wird beschrieben, wie der Filter Graph-Manager einen Quell Filter anhand eines Datei namens eingibt.</span><span class="sxs-lookup"><span data-stu-id="7adce-104">This article describes how the Filter Graph Manager locates a source filter, given a file name.</span></span> <span data-ttu-id="7adce-105">Sie können diesen Mechanismus verwenden, um eigene benutzerdefinierte Dateitypen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7adce-105">You can use this mechanism to register your own custom file types.</span></span> <span data-ttu-id="7adce-106">Sobald der Dateityp registriert ist, lädt DirectShow automatisch den richtigen Quell Filter, wenn eine Anwendung [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)aufruft.</span><span class="sxs-lookup"><span data-stu-id="7adce-106">Once the file type is registered, DirectShow will automatically load the correct source filter whenever an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

-   [<span data-ttu-id="7adce-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7adce-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="7adce-108">Protokolle</span><span class="sxs-lookup"><span data-stu-id="7adce-108">Protocols</span></span>](#protocols)
-   [<span data-ttu-id="7adce-109">Dateierweiterungen</span><span class="sxs-lookup"><span data-stu-id="7adce-109">File Extensions</span></span>](#file-extensions)
-   [<span data-ttu-id="7adce-110">Bytes überprüfen</span><span class="sxs-lookup"><span data-stu-id="7adce-110">Check Bytes</span></span>](#check-bytes)
-   [<span data-ttu-id="7adce-111">Der Quell Filter wird geladen.</span><span class="sxs-lookup"><span data-stu-id="7adce-111">Loading the Source Filter</span></span>](#loading-the-source-filter)
-   [<span data-ttu-id="7adce-112">Benutzerdefinierte Dateitypen in Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="7adce-112">Custom File Types in Windows Media Player</span></span>](#custom-file-types-in-windows-media-player)
-   [<span data-ttu-id="7adce-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7adce-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="7adce-114">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7adce-114">Overview</span></span>

<span data-ttu-id="7adce-115">Um einen Quell Filter anhand eines angegebenen Datei namens zu suchen, versucht der Filter Graph-Manager, die folgenden Schritte in der angegebenen Reihenfolge durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="7adce-115">To locate a source filter from a given file name, the Filter Graph Manager attempts to do the following, in order:</span></span>

1.  <span data-ttu-id="7adce-116">Entspricht dem Protokoll, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7adce-116">Match the protocol, if any.</span></span>
2.  <span data-ttu-id="7adce-117">Mit der Dateierweiterung vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7adce-117">Match the file extension.</span></span>
3.  <span data-ttu-id="7adce-118">Vergleichen Sie die Muster der Bytes in der Datei, die als *Check Bytes* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7adce-118">Match patterns of bytes within the file, called *check bytes*.</span></span>

## <a name="protocols"></a><span data-ttu-id="7adce-119">Protokolle</span><span class="sxs-lookup"><span data-stu-id="7adce-119">Protocols</span></span>

<span data-ttu-id="7adce-120">Protokollnamen wie "FTP" oder "http" werden unter dem</span><span class="sxs-lookup"><span data-stu-id="7adce-120">Protocol names such as "ftp" or "http" are registered under the</span></span>

<span data-ttu-id="7adce-121">**HKEY- \_ Klassen Stamm \_**</span><span class="sxs-lookup"><span data-stu-id="7adce-121">**HKEY\_CLASSES\_ROOT**</span></span>

<span data-ttu-id="7adce-122">Schlüssel mit der folgenden Struktur:</span><span class="sxs-lookup"><span data-stu-id="7adce-122">key, with the following structure:</span></span>


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



<span data-ttu-id="7adce-123">Wenn der Dateiname oder die URL einen Doppelpunkt (': ') enthält, versucht der Filter Graph-Manager, den Teil vor ': ' als Protokollnamen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7adce-123">If the file name or URL contains a colon (':'), the Filter Graph Manager attempts to use the portion before the ':' as a protocol name.</span></span> <span data-ttu-id="7adce-124">Wenn der Name beispielsweise "myprot://MyFile.ext" lautet, sucht er nach einem Registrierungsschlüssel mit dem Namen " **myprot**".</span><span class="sxs-lookup"><span data-stu-id="7adce-124">For example, if the name is "myprot://myfile.ext", it searches for a registry key named **myprot**.</span></span> <span data-ttu-id="7adce-125">Wenn dieser Schlüssel vorhanden ist und einen Unterschlüssel mit dem Namen "Extensions" enthält, sucht der Filter Graph-Manager innerhalb des unter Schlüssels nach Einträgen, die der Dateierweiterung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7adce-125">If this key exists and contains a subkey named "Extensions", the Filter Graph Manager searches within that subkey for entries that match the file extension.</span></span> <span data-ttu-id="7adce-126">Der Wert des Schlüssels muss eine GUID in Form einer Zeichenfolge sein. Beispiel: " {00000000-0000-0000-0000-000000000000} ".</span><span class="sxs-lookup"><span data-stu-id="7adce-126">The value of the key must be a GUID in string form; for example, "{00000000-0000-0000-0000-000000000000}".</span></span> <span data-ttu-id="7adce-127">Wenn der Filter Diagramm-Manager keine Entsprechungen innerhalb des unter Schlüssels " **Erweiterungen** " aufweisen kann, sucht er nach einem Unterschlüssel namens **Quell Filter**, bei dem es sich auch um eine GUID im Zeichen folgen Format handeln muss.</span><span class="sxs-lookup"><span data-stu-id="7adce-127">If the Filter Graph Manager cannot match anything within the **Extensions** subkey, it looks for a subkey named **Source Filter**, which must also be a GUID in string form.</span></span>

<span data-ttu-id="7adce-128">Wenn der Filter Diagramm-Manager eine übereinstimmende GUID findet, wird diese als CLSID des Quell Filters verwendet, und es wird versucht, den Filter zu laden.</span><span class="sxs-lookup"><span data-stu-id="7adce-128">If the Filter Graph Manager finds a matching GUID, it uses this as the CLSID of the source filter, and attempts to load the filter.</span></span> <span data-ttu-id="7adce-129">Wenn keine Entsprechung gefunden wird, wird der Datei [Quellen Filter (URL)](file-source--url--filter.md) verwendet, der den Dateinamen als URL behandelt.</span><span class="sxs-lookup"><span data-stu-id="7adce-129">If it does not find a match, it uses the [File Source (URL)](file-source--url--filter.md) filter, which treats the file name as a URL.</span></span>

<span data-ttu-id="7adce-130">Dieser Algorithmus hat zwei Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="7adce-130">There are two exceptions to this algorithm:</span></span>

-   <span data-ttu-id="7adce-131">Um Treiber Buchstaben auszuschließen, werden Zeichen folgen mit einem Zeichen nicht als Protokolle betrachtet.</span><span class="sxs-lookup"><span data-stu-id="7adce-131">To exclude driver letters, single-character strings are not considered protocols.</span></span>
-   <span data-ttu-id="7adce-132">Wenn die Zeichenfolge "file:" oder "file://" ist, wird Sie nicht als Protokoll behandelt.</span><span class="sxs-lookup"><span data-stu-id="7adce-132">If the string is "file:" or "file://", it is not treated as a protocol.</span></span>

## <a name="file-extensions"></a><span data-ttu-id="7adce-133">Dateierweiterungen</span><span class="sxs-lookup"><span data-stu-id="7adce-133">File Extensions</span></span>

<span data-ttu-id="7adce-134">Wenn der Dateiname kein Protokoll enthält, sucht der Filter Graph-Manager in der Registrierung nach Einträgen mit den Schlüssel- **\_ \_ \\ Medientyp \\ Erweiterungen \\** der Schlüssel-HKEY-Klasse.*ext* \\ , wobei.*ext* ist die Dateierweiterung.</span><span class="sxs-lookup"><span data-stu-id="7adce-134">If there is no protocol in the file name, the Filter Graph Manager looks in the registry for entries with the key **HKEY\_CLASSES\_ROOT\\Media Type\\Extensions\\**.*ext*\\, where .*ext* is the file extension.</span></span> <span data-ttu-id="7adce-135">Wenn dieser Schlüssel vorhanden ist, enthält der Wert **Quell Filter** die CLSID des Quell Filters in Form einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7adce-135">If this key exists, the value **Source Filter** contains the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="7adce-136">Optional kann der Schlüsselwerte für **Medientyp** und **Untertyp** aufweisen, die den Haupttyp und die Untertyp-GUIDs enthalten.</span><span class="sxs-lookup"><span data-stu-id="7adce-136">Optionally, the key can have values for **Media Type** and **Subtype**, which give the major type and subtype GUIDs.</span></span>

## <a name="check-bytes"></a><span data-ttu-id="7adce-137">Bytes überprüfen</span><span class="sxs-lookup"><span data-stu-id="7adce-137">Check Bytes</span></span>

<span data-ttu-id="7adce-138">Einige Dateitypen können durch bestimmte Muster von Bits identifiziert werden, die bei bestimmten Byte Offsets in der Datei auftreten.</span><span class="sxs-lookup"><span data-stu-id="7adce-138">Some file types can be identified by specific patterns of bits occurring at specific byte offsets in the file.</span></span> <span data-ttu-id="7adce-139">Der Filter Graph-Manager sucht in der Registrierung nach Schlüsseln in der folgenden Form:</span><span class="sxs-lookup"><span data-stu-id="7adce-139">The Filter Graph Manager looks in the registry for keys with the following form:</span></span>

<span data-ttu-id="7adce-140">**HKEY \_ Klassen Stamm- \_ \\ mediaType \\**{ *Major Type* } \\ { *Untertyp* }</span><span class="sxs-lookup"><span data-stu-id="7adce-140">**HKEY\_CLASSES\_ROOT\\MediaType\\**{ *major type* }\\{ *subtype* }</span></span>

<span data-ttu-id="7adce-141">wobei *Haupttyp* und *Untertyp* GUIDs sind, die den Medientyp für den Bytestream definieren.</span><span class="sxs-lookup"><span data-stu-id="7adce-141">where *major type* and *subtype* are GUIDs that define the media type for the byte stream.</span></span> <span data-ttu-id="7adce-142">Jeder Schlüssel enthält einen oder mehrere Unterschlüssel, normalerweise den Namen "1", "2" usw., die die Überprüfung der Bytes definieren. und einen Unterschlüssel namens **Quell Filter** , der die CLSID des Quell Filters in Form von Zeichen folgen enthält.</span><span class="sxs-lookup"><span data-stu-id="7adce-142">Each key contains one or more subkeys, usually named 1, 2, and so on, which define the check bytes; and a subkey named **Source Filter** that gives the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="7adce-143">Bei den Check-Byte-unter Schlüsseln handelt es sich um Zeichen folgen, die einen oder mehrere Quads mit dem Namen enthalten:</span><span class="sxs-lookup"><span data-stu-id="7adce-143">The check-byte subkeys are strings that contain one or more quads of numbers called:</span></span>

<span data-ttu-id="7adce-144">*Offset*, *CB*, *Maske*, *Val*</span><span class="sxs-lookup"><span data-stu-id="7adce-144">*offset*, *cb*, *mask*, *val*</span></span>

<span data-ttu-id="7adce-145">Um die Datei abzugleichen, liest der Filter Graph-Manager CB-bytes, beginnend mit dem Byte Nummern Offset.</span><span class="sxs-lookup"><span data-stu-id="7adce-145">To match the file, the Filter Graph Manager reads cb bytes, starting from byte number offset.</span></span> <span data-ttu-id="7adce-146">Anschließend wird ein bitweiser And-Operator mit dem Wert in Mask durchführt.</span><span class="sxs-lookup"><span data-stu-id="7adce-146">It then performs a bitwise-AND against the value in mask.</span></span> <span data-ttu-id="7adce-147">Wenn das Ergebnis "Val" ist, ist die Datei für dieses Vierfache gleich.</span><span class="sxs-lookup"><span data-stu-id="7adce-147">If the result equals val, the file is a match for that quad.</span></span> <span data-ttu-id="7adce-148">Die Werte mask und Val werden in HEX angegeben.</span><span class="sxs-lookup"><span data-stu-id="7adce-148">The values mask and val are given in hex.</span></span> <span data-ttu-id="7adce-149">Ein leerer Eintrag für Mask wird als eine Zeichenfolge mit einer Länge von 1 s der Länge CB behandelt.</span><span class="sxs-lookup"><span data-stu-id="7adce-149">A blank entry for mask is treated as a string of 1s of length cb.</span></span> <span data-ttu-id="7adce-150">Ein negativer Wert für Offset gibt einen Offset vom Dateiende an.</span><span class="sxs-lookup"><span data-stu-id="7adce-150">A negative value for offset indicates an offset from the end of the file.</span></span> <span data-ttu-id="7adce-151">Um den Schlüssel abzugleichen, muss die Datei mit allen Quads in den unter Schlüsseln identisch sein.</span><span class="sxs-lookup"><span data-stu-id="7adce-151">To match the key, the file must match all of the quads in any of the subkeys.</span></span>

<span data-ttu-id="7adce-152">Nehmen Sie beispielsweise an, die Registrierung enthält die folgenden Schlüssel unter **HKCR- \\ Medientyp**:</span><span class="sxs-lookup"><span data-stu-id="7adce-152">For example, assume the registry contains the following keys under **HKCR\\Media Type**:</span></span>


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



<span data-ttu-id="7adce-153">Der erste Schlüssel entspricht dem Haupttyp MediaType \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="7adce-153">The first key corresponds to the major type MEDIATYPE\_Stream.</span></span> <span data-ttu-id="7adce-154">Der Unterschlüssel unten, der dem Untertyp "MediaType \_ MIDI" entspricht.</span><span class="sxs-lookup"><span data-stu-id="7adce-154">The subkey below that corresponds to the subtype MEDIATYPE\_Midi.</span></span> <span data-ttu-id="7adce-155">Der Wert für den Quell Filter Unterschlüssel ist CLSID \_ asynshader, die CLSID des [Datei Quell Filters (Async)](file-source--async--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7adce-155">The value for the Source Filter subkey is CLSID\_AsyncReader, the CLSID of the [File Source (Async)](file-source--async--filter.md) filter.</span></span>

<span data-ttu-id="7adce-156">Jeder Eintrag kann über mehrere Vierbeiner verfügen. alle müssen abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="7adce-156">Each entry can have multiple quadruples; all of them must match.</span></span> <span data-ttu-id="7adce-157">Im folgenden Beispiel müssen die ersten 4 Bytes der Datei 0xab, 0xCD, 0x12, 0x34; sein. und die letzten 4 Bytes der Datei müssen 0xab, 0xAB, 0x00, 0xAB lauten:</span><span class="sxs-lookup"><span data-stu-id="7adce-157">In the following example, the first 4 bytes of the file must be 0xAB, 0xCD, 0x12, 0x34; and the last 4 bytes of the file must be 0xAB, 0xAB, 0x00, 0xAB:</span></span>


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



<span data-ttu-id="7adce-158">Außerdem können mehrere Einträge unter einem einzelnen Medientyp aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="7adce-158">Also, there can be multiple entries listed under a single media type.</span></span> <span data-ttu-id="7adce-159">Eine Entsprechung zu den entsprechenden ist ausreichend.</span><span class="sxs-lookup"><span data-stu-id="7adce-159">A match to any of them is sufficient.</span></span> <span data-ttu-id="7adce-160">Dieses Schema ermöglicht eine Reihe alternativer Masken; beispielsweise WAV-Dateien, die möglicherweise über einen Riff-Header verfügen.</span><span class="sxs-lookup"><span data-stu-id="7adce-160">This scheme allows for a set of alternative masks; for instance, .wav files that might or might not have a RIFF header.</span></span>

> [!Note]  
> <span data-ttu-id="7adce-161">Dieses Schema ähnelt dem Schema, das von der [**getclassfile**](/windows/win32/api/objbase/nf-objbase-getclassfile) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7adce-161">This scheme is similar to the one used by the [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) function.</span></span>

 

## <a name="loading-the-source-filter"></a><span data-ttu-id="7adce-162">Der Quell Filter wird geladen.</span><span class="sxs-lookup"><span data-stu-id="7adce-162">Loading the Source Filter</span></span>

<span data-ttu-id="7adce-163">Vorausgesetzt, dass der Filter Graph-Manager einen passenden Quell Filter für die Datei findet, wird dieser Filter dem Diagramm hinzugefügt, der Filter für die [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) -Schnittstelle abgefragt und [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7adce-163">Assuming that the Filter Graph Manager finds a matching source filter for the file, it adds that filter to the graph, queries the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface, and calls [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span></span> <span data-ttu-id="7adce-164">Die Argumente für die **Load** -Methode sind der Dateiname und der Medientyp, wie in der Registrierung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7adce-164">The arguments to the **Load** method are the file name and the media type, as determined from the registry.</span></span>

<span data-ttu-id="7adce-165">Wenn der Filter Graph-Manager keine Elemente aus der Registrierung finden kann, wird standardmäßig der asynchrone Datei Quell Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="7adce-165">If the Filter Graph Manager cannot find anything from the registry, it defaults to using the Async File Source filter.</span></span> <span data-ttu-id="7adce-166">In diesem Fall wird der Medientyp auf **mediaType \_ Stream** und **mediasubtype \_ None** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7adce-166">In that case, it sets the media type to **MEDIATYPE\_Stream**, **MEDIASUBTYPE\_None**.</span></span>

## <a name="custom-file-types-in-windows-media-player"></a><span data-ttu-id="7adce-167">Benutzerdefinierte Dateitypen in Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="7adce-167">Custom File Types in Windows Media Player</span></span>

<span data-ttu-id="7adce-168">Windows Media Player verwendet einen zusätzlichen Satz von Registrierungs Einträgen.</span><span class="sxs-lookup"><span data-stu-id="7adce-168">Windows Media Player uses an additional set of registry entries.</span></span> <span data-ttu-id="7adce-169">Weitere Informationen finden Sie unter [Registrierungs Einstellungen für Dateinamen Erweiterungen](../wmp/file-name-extension-registry-settings.md) im Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="7adce-169">For more information, see [File Name Extension Registry Settings](../wmp/file-name-extension-registry-settings.md) in the Windows Media Player SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7adce-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7adce-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7adce-171">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="7adce-171">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 
