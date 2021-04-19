---
description: In diesem Thema werden die internen Details erläutert, wie der quellresolver eine Medienquelle erstellt.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Schema Handler und Byte-Stream Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359934"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a><span data-ttu-id="6cb29-103">Schema Handler und Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="6cb29-103">Scheme Handlers and Byte-Stream Handlers</span></span>

<span data-ttu-id="6cb29-104">In diesem Thema werden die internen Details erläutert, wie der quellresolver eine Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cb29-104">This topic describes the internal details of how the source resolver creates a media source.</span></span> <span data-ttu-id="6cb29-105">Lesen Sie dieses Thema, wenn Sie eine benutzerdefinierte Medienquelle für Media Foundation implementieren und die Medienquelle für Anwendungen über den quellresolver verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="6cb29-105">Read this topic if you are implementing a custom media source for Media Foundation, and you want the media source to be available to applications via the source resolver.</span></span>

<span data-ttu-id="6cb29-106">Der quellresolver kann eine Medienquelle aus einer URL oder einem Bytestream erstellen (d. h. ein [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Zeiger).</span><span class="sxs-lookup"><span data-stu-id="6cb29-106">The source resolver can create a media source from a URL or from a byte stream (that is, an [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) pointer).</span></span> <span data-ttu-id="6cb29-107">Hierfür werden Hilfsobjekte verwendet, die als *Handler* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6cb29-107">To do so, it uses helper objects called *handlers*.</span></span> <span data-ttu-id="6cb29-108">Für URLs verwendet der quellresolver *Schema Handler*.</span><span class="sxs-lookup"><span data-stu-id="6cb29-108">For URLs, the source resolver uses *scheme handlers*.</span></span> <span data-ttu-id="6cb29-109">Für Bytestreams werden *Byte Datenstrom Handler* verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cb29-109">For byte streams, it uses *byte-stream handlers*.</span></span>

<span data-ttu-id="6cb29-110">Ein Schema Handler nimmt eine URL als Eingabe an und erstellt entweder eine Medienquelle oder einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="6cb29-110">A scheme handler takes a URL as input and creates either a media source or a byte stream.</span></span> <span data-ttu-id="6cb29-111">Wenn ein Bytestream erstellt wird, übergibt der quellresolver diesen an einen bytestreamhandler, der die Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cb29-111">If it creates a byte stream, the source resolver will pass that to a byte-stream handler, which creates the media source.</span></span> <span data-ttu-id="6cb29-112">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6cb29-112">The following image illustrates this process.</span></span>

![Diagramm, das den Quell Auflösungsprozess anzeigt](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a><span data-ttu-id="6cb29-114">Schema Handler</span><span class="sxs-lookup"><span data-stu-id="6cb29-114">Scheme Handlers</span></span>

<span data-ttu-id="6cb29-115">Schema Handler werden verwendet, wenn die Anwendung [**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) oder die zugehörige asynchrone Entsprechung [**beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)aufruft.</span><span class="sxs-lookup"><span data-stu-id="6cb29-115">Scheme handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) or its asynchronous equivalent, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

<span data-ttu-id="6cb29-116">Der Quell Konflikt Löser sucht Schema Handler in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="6cb29-116">The source resolver looks up scheme handlers in the registry.</span></span> <span data-ttu-id="6cb29-117">Schema Handler werden nach dem URL-Schema unter den folgenden Schlüsseln aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="6cb29-117">Scheme handlers are listed by URL scheme, under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="6cb29-118">dabei *<scheme>* ist das URL-Schema, das der Handler analysieren soll.</span><span class="sxs-lookup"><span data-stu-id="6cb29-118">where *<scheme>* is the URL scheme that the handler is designed to parse.</span></span> <span data-ttu-id="6cb29-119">Das Schema enthält das nachfolgende Zeichen ': '; Beispiel: "http:".</span><span class="sxs-lookup"><span data-stu-id="6cb29-119">The scheme includes the trailing ':' character; for example, "http:".</span></span>

<span data-ttu-id="6cb29-120">Fügen Sie zum Registrieren eines neuen Schema Handlers einen Eintrag hinzu, dessen Name die CLSID des Schema Handlers ist, in kanonischer Zeichen folgen Form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="6cb29-120">To register a new scheme handler, add an entry whose name is the CLSID of the scheme handler, in canonical string form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="6cb29-121">Der Wert des Eintrags ist eine Zeichenfolge (reg \_ SZ), die eine kurze Beschreibung des Handlers enthält, z. b. "Mein Schema Handler".</span><span class="sxs-lookup"><span data-stu-id="6cb29-121">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Scheme Handler."</span></span> <span data-ttu-id="6cb29-122">Der wichtige Teil des Eintrags ist die CLSID.</span><span class="sxs-lookup"><span data-stu-id="6cb29-122">The important part of the entry is the CLSID.</span></span> <span data-ttu-id="6cb29-123">Der quellresolver erstellt den Handler durch Aufrufen von **CoCreateInstance** mit dieser CLSID.</span><span class="sxs-lookup"><span data-stu-id="6cb29-123">The source resolver creates the handler by calling **CoCreateInstance** with this CLSID.</span></span>

<span data-ttu-id="6cb29-124">Schema Handler machen die [**IMF Schema Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cb29-124">Scheme handlers expose the [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) interface.</span></span> <span data-ttu-id="6cb29-125">Wenn der quellresolver einen Schema Handler findet, der mit dem URL-Schema übereinstimmt, ruft der quellresolver [**imvschemehandler:: beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)auf und übergibt dabei die ursprüngliche URL.</span><span class="sxs-lookup"><span data-stu-id="6cb29-125">If the source resolver finds a scheme handler that matches the URL scheme, the source resolver calls [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passing in the original URL.</span></span> <span data-ttu-id="6cb29-126">Der Schema Handler öffnet die URL und versucht, den Inhalt zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="6cb29-126">The scheme handler will open the URL and attempt to parse the contents.</span></span> <span data-ttu-id="6cb29-127">An diesem Punkt verfügt der Schema Handler über zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="6cb29-127">At that point, the scheme handler has two options:</span></span>

-   <span data-ttu-id="6cb29-128">Erstellen Sie eine Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="6cb29-128">Create a media source.</span></span>
-   <span data-ttu-id="6cb29-129">Erstellen Sie einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="6cb29-129">Create a byte stream.</span></span>

<span data-ttu-id="6cb29-130">Wenn eine Medienquelle erstellt wird, gibt der quellresolver die Medienquelle an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="6cb29-130">If it creates a media source, the source resolver returns the media source to the application.</span></span> <span data-ttu-id="6cb29-131">Wenn ein Bytestream erstellt wird, versucht der quellresolver, einen entsprechenden bytestreamhandler zu finden, wie im nächsten Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6cb29-131">If it creates a byte stream, the source resolver attempts to find an appropriate byte-stream handler, as described in the next section.</span></span>

## <a name="byte-stream-handlers"></a><span data-ttu-id="6cb29-132">Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="6cb29-132">Byte-Stream Handlers</span></span>

<span data-ttu-id="6cb29-133">Byte-Datenstrom Handler werden verwendet, wenn die Anwendung [**IMF sourceresolver:: forateobjectfrooltestream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) oder die zugehörige asynchrone Entsprechung ( [**beginkreateobjectfromb-Stream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)) aufruft.</span><span class="sxs-lookup"><span data-stu-id="6cb29-133">Byte-stream handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) or its asynchronous equivalent, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span></span> <span data-ttu-id="6cb29-134">Sie werden auch verwendet, wenn ein Schema Handler einen Bytestream zurückgibt, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6cb29-134">They are also used when a scheme handler returns a byte stream, as described previously.</span></span>

<span data-ttu-id="6cb29-135">Wie bei Schema Handlern sind Byte-Stream-Handler in der Registrierung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cb29-135">As with scheme handlers, byte-stream handlers are listed in the registry.</span></span> <span data-ttu-id="6cb29-136">Sie werden entweder über die Dateinamenerweiterung oder den MIME-Typ (oder beides) unter den folgenden Schlüsseln aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="6cb29-136">They are listed either by file name extension or MIME type (or both), under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="6cb29-137">dabei *<ExtensionOrMimeType>* ist die Dateinamenerweiterung oder der MIME-Typ.</span><span class="sxs-lookup"><span data-stu-id="6cb29-137">where *<ExtensionOrMimeType>* is the file name extension or MIME type.</span></span> <span data-ttu-id="6cb29-138">Dateierweiterungen enthalten das erste Zeichen ".". Beispiel: ". wmv".</span><span class="sxs-lookup"><span data-stu-id="6cb29-138">File extensions include the initial '.' character; for example, ".wmv".</span></span>

<span data-ttu-id="6cb29-139">Die Dateinamenerweiterung ist Teil der URL, die von der Anwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6cb29-139">The file name extension is part of the URL, provided by the application.</span></span> <span data-ttu-id="6cb29-140">Der MIME-Typ ist möglicherweise über das [**MF- \_ Bytestream- \_ \_ Inhaltstyp Attribut im Bytestream**](mf-bytestream-content-type-attribute.md) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cb29-140">The MIME type might be available through the [**MF\_BYTESTREAM\_CONTENT\_TYPE**](mf-bytestream-content-type-attribute.md) attribute on the byte stream.</span></span>

<span data-ttu-id="6cb29-141">Fügen Sie zum Registrieren eines neuen bytestreamhandlers einen Eintrag hinzu, dessen Name die CLSID des Handlers ist, in kanonischer Zeichen folgen Form.</span><span class="sxs-lookup"><span data-stu-id="6cb29-141">To register a new byte-stream handler, add an entry whose name is the CLSID of the handler, in canonical string form.</span></span> <span data-ttu-id="6cb29-142">Der Wert des Eintrags ist eine Zeichenfolge (reg \_ SZ), die eine kurze Beschreibung des Handlers enthält, z. b. "My Byte-Stream Handler".</span><span class="sxs-lookup"><span data-stu-id="6cb29-142">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Byte-Stream Handler."</span></span> <span data-ttu-id="6cb29-143">Der quellresolver ruft **cokreateinstance** auf, um den Handler aus der CLSID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6cb29-143">The source resolver calls **CoCreateInstance** to create the handler from the CLSID.</span></span> <span data-ttu-id="6cb29-144">Sie können denselben Handler unter mehr als einer Erweiterung oder einem MIME-Typ registrieren.</span><span class="sxs-lookup"><span data-stu-id="6cb29-144">You can register the same handler under more than one extension or MIME type.</span></span>

<span data-ttu-id="6cb29-145">Byte Datenstrom Handler machen die [**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cb29-145">Byte-stream handlers expose the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="6cb29-146">Wenn der quellresolver einen passenden Byte Datenstrom Handler findet, wird [**IMF bytestreamhandler:: beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6cb29-146">If the source resolver finds a matching byte-stream handler, it calls [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="6cb29-147">Bei der Eingabe für diese Methode handelt es sich um einen Zeiger auf den Bytestream Plus um die ursprüngliche URL, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cb29-147">The input to this method is a pointer to the byte stream, plus the original URL, if available.</span></span> <span data-ttu-id="6cb29-148">Der Byte Datenstrom Handler liest aus dem Bytestream, bis er genug Daten analysiert, um die Medienquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6cb29-148">The byte-stream handler reads from the byte stream until it parses enough data to create the media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cb29-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cb29-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb29-150">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="6cb29-150">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



