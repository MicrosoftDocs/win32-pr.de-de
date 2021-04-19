---
description: Erläutert, wie Sie den Zugriff auf Ihren Datenspeicher über einen OpenSearch-Webdienst aktivieren und wie Sie potenzielle Barrieren dafür vermeiden.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Aktivieren des Datenspeicher in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346913"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a><span data-ttu-id="5e579-103">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="5e579-103">Enabling Your Data Store in Windows Federated Search</span></span>

<span data-ttu-id="5e579-104">Erläutert, wie Sie den Zugriff auf Ihren Datenspeicher über einen [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst aktivieren und wie Sie potenzielle Barrieren dafür vermeiden.</span><span class="sxs-lookup"><span data-stu-id="5e579-104">Explains how to enable your data store to be accessed by an [OpenSearch](https://github.com/dewitt/opensearch) web service, and how to avoid potential barriers for doing so.</span></span>

<span data-ttu-id="5e579-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="5e579-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="5e579-106">Bedingungen für die Akzeptanz von Suchanforderungen</span><span class="sxs-lookup"><span data-stu-id="5e579-106">Conditions for Search Request Acceptance</span></span>](#conditions-for-search-request-acceptance)
    -   [<span data-ttu-id="5e579-107">Unterstützte Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="5e579-107">Supported Query Syntax</span></span>](#supported-query-syntax)
    -   [<span data-ttu-id="5e579-108">Unterstützte Authentifizierungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="5e579-108">Supported Authentication Protocols</span></span>](#supported-authentication-protocols)
-   [<span data-ttu-id="5e579-109">Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom</span><span class="sxs-lookup"><span data-stu-id="5e579-109">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [<span data-ttu-id="5e579-110">Beispiel für eine RSS-Feed-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5e579-110">Example of an RSS Feed Output</span></span>](#example-of-an-rss-feed-output)
-   [<span data-ttu-id="5e579-111">Automatische Zuordnung zu Windows Shell-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e579-111">Automatic Mapping to Windows Shell Properties</span></span>](#automatic-mapping-to-windows-shell-properties)
-   [<span data-ttu-id="5e579-112">Grundlegendes zur Zuordnung von Elementen zu Dateitypen in Windows</span><span class="sxs-lookup"><span data-stu-id="5e579-112">Understanding How Windows Maps Items to File Types</span></span>](#understanding-how-windows-maps-items-to-file-types)
-   [<span data-ttu-id="5e579-113">Vermeiden potenzieller Barrieren für die Aktivierung eines Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="5e579-113">Avoiding Potential Barriers to Enabling a Data Store</span></span>](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [<span data-ttu-id="5e579-114">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e579-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="5e579-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e579-115">Related topics</span></span>](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a><span data-ttu-id="5e579-116">Bedingungen für die Akzeptanz von Suchanforderungen</span><span class="sxs-lookup"><span data-stu-id="5e579-116">Conditions for Search Request Acceptance</span></span>

<span data-ttu-id="5e579-117">Der [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst, den Sie auf dem Webserver erstellen, **muss** die folgenden zwei Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="5e579-117">The [OpenSearch](https://github.com/dewitt/opensearch) web service you create on your web server **must** fulfill the following two requirements:</span></span>

-   <span data-ttu-id="5e579-118">Es ist möglich, eine `GET URL` Abfrage vom Client zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="5e579-118">Be able to accept a `GET URL` query from the client.</span></span>
-   <span data-ttu-id="5e579-119">Erlauben Sie, dass die Suchbegriffe in die URL eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="5e579-119">Permit the search terms to be embedded in the URL.</span></span>

    <span data-ttu-id="5e579-120">Im folgenden Beispiel wird gezeigt, wie ein Suchbegriff in eine URL eingebettet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e579-120">The following example shows how a search term can be embedded in a URL.</span></span>

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> <span data-ttu-id="5e579-121">Die Verbund Suche unterstützt das Senden `POST` von Anforderungen an einen Webdienst nicht.</span><span class="sxs-lookup"><span data-stu-id="5e579-121">Federated search does not support sending `POST` requests to a web service.</span></span>

 

<span data-ttu-id="5e579-122">Weitere Informationen zum Erstellen einer URL finden Sie unter "URL-Vorlagen Parameter" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="5e579-122">For more information about constructing a URL, see "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

### <a name="supported-query-syntax"></a><span data-ttu-id="5e579-123">Unterstützte Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="5e579-123">Supported Query Syntax</span></span>

<span data-ttu-id="5e579-124">In Windows 7 wird keine bestimmte Abfrage Syntax erwartet.</span><span class="sxs-lookup"><span data-stu-id="5e579-124">There is no specific query syntax expected in Windows 7.</span></span> <span data-ttu-id="5e579-125">Der OpenSearch-Anbieter akzeptiert alle Bedingungen, die der Benutzer in das Eingabefeld in Windows-Explorer eingibt, und codiert ihn in die URL.</span><span class="sxs-lookup"><span data-stu-id="5e579-125">The OpenSearch provider accepts whatever terms the user enters in the input box in Windows Explorer, and encodes it into the URL.</span></span> <span data-ttu-id="5e579-126">Dies erfolgt entsprechend der URL-Vorlage, die unter "URL-Vorlagen Parameter" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5e579-126">It does so according to the URL template described in "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

<span data-ttu-id="5e579-127">Benutzer erwarten, dass separate Begriffe als implizit und zusammen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="5e579-127">Users expect that separate terms are treated as implicitly ANDed together.</span></span> <span data-ttu-id="5e579-128">Eine Abfrage für "Microsoft Windows" sollte z. b. nur Ergebnisse zurückgeben, die sowohl "Windows" als auch "Microsoft" enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e579-128">For example, a query for "Microsoft Windows" should return only results that contain both "Windows" and "Microsoft".</span></span>

### <a name="supported-authentication-protocols"></a><span data-ttu-id="5e579-129">Unterstützte Authentifizierungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="5e579-129">Supported Authentication Protocols</span></span>

<span data-ttu-id="5e579-130">Windows Federated Search unterstützt die Windows-basierte Authentifizierung und kann über die folgenden Protokolle Anmelde Informationen für Webdienste bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="5e579-130">Windows Federated Search supports Windows-based authentication, and can provide credentials to web services via the following protocols:</span></span>

-   <span data-ttu-id="5e579-131">NTLM.</span><span class="sxs-lookup"><span data-stu-id="5e579-131">NTLM.</span></span>
-   <span data-ttu-id="5e579-132">Kerberos.</span><span class="sxs-lookup"><span data-stu-id="5e579-132">Kerberos.</span></span>
-   <span data-ttu-id="5e579-133">Basic (nur über HTTPS).</span><span class="sxs-lookup"><span data-stu-id="5e579-133">Basic (only over https).</span></span>
-   <span data-ttu-id="5e579-134">Andere unter Windows installierte SSPs (Security Support Providers), die zusätzliche Abfrage Kapazität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e579-134">Other Security Support Providers (SSPs) installed on Windows that provide additional querying capacity.</span></span> <span data-ttu-id="5e579-135">In der Dokumentation zum [SSP Interface](../secauthn/sspi.md) SDK finden Sie Informationen zum möglichen Hinzufügen anderer SSPs.</span><span class="sxs-lookup"><span data-stu-id="5e579-135">See the [SSP Interface](../secauthn/sspi.md) SDK documentation to keep abreast of the potential addition of other SSPs.</span></span>

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="5e579-136">Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom</span><span class="sxs-lookup"><span data-stu-id="5e579-136">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="5e579-137">Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter ist für die Zuordnung der XML-Element Werte zu den Windows Shell-Systemeigenschaften zuständig, die von Windows-Anwendungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5e579-137">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span> <span data-ttu-id="5e579-138">Sie sind jedoch nicht auf die Standard Zuordnungen von RSS-oder Atom-Standardelementen beschränkt und können benutzerdefinierte XML-Elemente in den Windows-Namespace für jede der Eigenschaften einschließen.</span><span class="sxs-lookup"><span data-stu-id="5e579-138">But you are not limited to the default mappings of standard RSS or Atom elements, and can include custom XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="5e579-139">Beispielsweise können Sie eigene benutzerdefinierte XML-Elemente innerhalb des **Item** -Elements hinzufügen, um Windows zusätzliche Metadaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5e579-139">For example, you can add your own custom XML elements within the **item** element to provide additional metadata to Windows.</span></span> <span data-ttu-id="5e579-140">Sie können auch Elemente aus anderen XML-Namespaces zuordnen, z. b. iTunes.</span><span class="sxs-lookup"><span data-stu-id="5e579-140">You can also map elements from other XML namespaces, such as iTunes</span></span>

### <a name="example-of-an-rss-feed-output"></a><span data-ttu-id="5e579-141">Beispiel für eine RSS-Feed-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5e579-141">Example of an RSS Feed Output</span></span>

<span data-ttu-id="5e579-142">In der folgenden Beispielausgabe des RSS-Feeds wird ein Element zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e579-142">The following example RSS feed output returns one item.</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="5e579-143">Ausführlichere Informationen zur Eigenschaften Zuordnung finden Sie in den Abschnitten "Erweiterte Elemente in der Windows-Verbund Suche" und "benutzerdefinierte Eigenschafts Zuordnungen" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="5e579-143">For more detailed information about property mapping, see the "Extended Elements in WIndows Federated Search" and "Custom Property Mappings" sections in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="automatic-mapping-to-windows-shell-properties"></a><span data-ttu-id="5e579-144">Automatische Zuordnung zu Windows Shell-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e579-144">Automatic Mapping to Windows Shell Properties</span></span>

<span data-ttu-id="5e579-145">Innerhalb der Elemente im RSS-Feed können Sie andere XML-Elemente einschließen, die automatisch den Windows Shell-Systemeigenschaften zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5e579-145">Within the items in your RSS feed, you can choose to include other XML elements that automatically map to Windows Shell system properties.</span></span> <span data-ttu-id="5e579-146">Fügen Sie zu diesem Zweck ein Element mit dem Namen nach der Windows-shelleigenschaft ein, das dem Windows-shellsystem-Namespace vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="5e579-146">To do so, include an element named after the Windows Shell property and prefixed with the Windows Shell system namespace.</span></span> <span data-ttu-id="5e579-147">Das folgende Beispiel veranschaulicht die Namespace Deklaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` und die Einbindung eines Elements für die Eigenschaften Zuordnung `win:System.Contact.PrimaryEmailAddress` :</span><span class="sxs-lookup"><span data-stu-id="5e579-147">The following example illustrates the namespace declaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` and the inclusion of an element for the property mapping `win:System.Contact.PrimaryEmailAddress`:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



<span data-ttu-id="5e579-148">Das hier verwendete Namespace Präfix ( `"win"` ) ist ein Vorschlag. Sie können ein beliebiges Präfix verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e579-148">The namespace prefix used here (`"win"`) is a suggestion; you can use any prefix.</span></span> <span data-ttu-id="5e579-149">Allerdings müssen Sie die genauen Windows Shell-Eigenschaftsnamen verwenden und den exakten Uniform Resource Identifier (URI) einschließen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="5e579-149">However, you must use the exact Windows Shell property names, and must include the exact Uniform Resource Identifier (URI), as shown in the following example:</span></span>


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



<span data-ttu-id="5e579-150">**Informationen zu Windows Shell-System Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="5e579-150">**About Windows Shell System Properties**</span></span>

<span data-ttu-id="5e579-151">Windows definiert eine komplette Liste der [System Eigenschaften](../properties/props.md) und das Werttyp Format, das für jede Eigenschaft erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5e579-151">Windows defines a complete list of [System Properties](../properties/props.md) and the value type format required for each property.</span></span> <span data-ttu-id="5e579-152">Die Dokumentation für die Fenster shelleigenschaft [System. FileExtension](../properties/props-system-fileextension.md) gibt z. b. an, dass der Wert den führenden Punkt (". docx" und nicht "docx") enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="5e579-152">The documentation for the [System.FileExtension](../properties/props-system-fileextension.md) Window Shell property, for example, specifies that the value must contain the leading dot (".docx" and not "docx").</span></span>

<span data-ttu-id="5e579-153">**Werte für Datum und Uhrzeit**</span><span class="sxs-lookup"><span data-stu-id="5e579-153">**Date and Time Values**</span></span>

<span data-ttu-id="5e579-154">Das bevorzugte Datums-und Uhrzeit Format ist ISO-8601, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="5e579-154">The preferred date and time format is ISO-8601, as shown in the following example:</span></span>


```
2008-01-16T 19:20:30:.45+01:00
```



<span data-ttu-id="5e579-155">.NET-Entwickler sollten die DateTime-Klasse mit verwenden `ToString("R") ` , um das richtige Format auszugeben.</span><span class="sxs-lookup"><span data-stu-id="5e579-155">.NET developers should use the DateTime class with `ToString("R") `to output the correct format.</span></span>

<span data-ttu-id="5e579-156">Ausführlichere Informationen zur Eigenschaften Zuordnung finden Sie unter "Erweiterte Elemente in der Windows-Verbund Suche" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="5e579-156">For more detailed information about property mapping, see "Extended Elements in Windows Federated Search" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="understanding-how-windows-maps-items-to-file-types"></a><span data-ttu-id="5e579-157">Grundlegendes zur Zuordnung von Elementen zu Dateitypen in Windows</span><span class="sxs-lookup"><span data-stu-id="5e579-157">Understanding How Windows Maps Items to File Types</span></span>

<span data-ttu-id="5e579-158">Durch die Suche in der Windows-Explorer-Benutzeroberfläche können Benutzer Ergebnisse als Dateien behandeln, wenn ein RSS-Element auf eine remote gespeicherte Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="5e579-158">Searching within the Windows Explorer UI permits users to treat results as files when an RSS item points to a file stored remotely.</span></span> <span data-ttu-id="5e579-159">Der Benutzer kann Elemente per Drag & amp; Drop auf den Desktop verschieben, und die Windows-Explorer-Benutzeroberfläche zeigt das richtige Symbol an und stellt das entsprechende Kontextmenü bereit.</span><span class="sxs-lookup"><span data-stu-id="5e579-159">The user can drag and drop items to the desktop, and the Windows Explorer UI displays the correct icon and provides the appropriate shortcut menu.</span></span> <span data-ttu-id="5e579-160">Wenn das RSS-Element nicht auf eine remote gespeicherte Datei verweist, wird die Datei als Link behandelt, und Benutzer können Aktionen ausführen, z. b. das Erstellen einer Verknüpfung oder das Öffnen im Browser.</span><span class="sxs-lookup"><span data-stu-id="5e579-160">If the RSS item does not point to a remotely stored file, the file is treated as a link, and users can perform actions on it such as creating a shortcut or opening it in the browser.</span></span>

<span data-ttu-id="5e579-161">Im folgenden Flussdiagramm wird gezeigt, wie Windows den Dateityp eines Elements bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5e579-161">The following flowchart shows how Windows determines an item's file type.</span></span>

![Flussdiagramm, das Pfade von einem Element zu Entscheidungen anzeigt, um es als weblinktyp Element oder als Dateityp zu behandeln](images/determineanitemfiletype.png)

<span data-ttu-id="5e579-163">Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter führt die folgenden Schritte aus, um ein Element einem Dateityp zuzuordnen:</span><span class="sxs-lookup"><span data-stu-id="5e579-163">The [OpenSearch](https://github.com/dewitt/opensearch) provider performs the following steps to map an item to a file type:</span></span>

-   <span data-ttu-id="5e579-164">Identifizieren Sie, ob das Element als Datei oder Weblink behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e579-164">Identify whether the item should be treated as a file or a web link.</span></span>
-   <span data-ttu-id="5e579-165">Identifizieren Sie die korrekte zu verwendende Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="5e579-165">Identify the correct file name extension to use.</span></span>

<span data-ttu-id="5e579-166">Wenn das Element z. b. über eine Link-URL verfügt, die einen Dateisystempfad verwendet (z `file:///\\server\share\etc\item.ext` . b.), behandelt der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter den Link als Datei und bestimmt den Typ anhand der Dateinamenerweiterung, die im Pfad verwendet wird (in diesem Beispiel. ext).</span><span class="sxs-lookup"><span data-stu-id="5e579-166">For example, if the item has a link URL that uses a file system path (such as `file:///\\server\share\etc\item.ext`), the [OpenSearch](https://github.com/dewitt/opensearch) provider treats the link as a file and determines the type by the file name extension used in the path (.ext in this example).</span></span>

<span data-ttu-id="5e579-167">Wenn das Element das standardmäßige RSS-Gehäuse oder das **mediarss Media: Content** -Element verwendet, geht der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter davon aus, dass das Element eine Datei ist, und identifiziert die Dateinamenerweiterung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5e579-167">If the item uses the standard RSS enclosure or **MediaRSS media:content** element, the [OpenSearch](https://github.com/dewitt/opensearch) provider assumes that the item is a file and identifies the file name extension as follows:</span></span>

-   <span data-ttu-id="5e579-168">Wenn die Windows Shell-Eigenschaft [System. FileExtension](../properties/props-system-fileextension.md) dem Element zugeordnet wurde, verwendet der Anbieter diese Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="5e579-168">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has been mapped for the item, the provider uses that file name extension.</span></span>
-   <span data-ttu-id="5e579-169">Wenn die Windows Shell-Eigenschaft [System. FileExtension](../properties/props-system-fileextension.md) nicht zugeordnet wurde, verwendet der Anbieter das **Type** -Attribut, das im Gehäuse-oder Content-Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5e579-169">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has not been mapped, the provider uses the **Type** attribute specified in the enclosure or content element.</span></span> <span data-ttu-id="5e579-170">Dieses Element sollte eine `MIMEType` Zeichenfolge enthalten, z `"image/jpeg"` . b..</span><span class="sxs-lookup"><span data-stu-id="5e579-170">This element should contain a `MIMEType` string, such as `"image/jpeg"`.</span></span> <span data-ttu-id="5e579-171">Wenn der `MIMEType` einer Dateinamenerweiterung zugeordnet ist, die auf dem Client Computer registriert ist, wird das Element als Datei dieses Typs angesehen.</span><span class="sxs-lookup"><span data-stu-id="5e579-171">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the item is regarded as a file of that type.</span></span> <span data-ttu-id="5e579-172">Wenn der `MIMEType` auf dem Client Computer registrierte Dateinamenerweiterung nicht zugeordnet ist, wird das Element als weblinktyp behandelt.</span><span class="sxs-lookup"><span data-stu-id="5e579-172">If the `MIMEType` is not associated with a file name extension registered on the client computer, the item is treated as a web link type.</span></span> <span data-ttu-id="5e579-173">Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter versucht nicht, das **URL** -Attribut zu analysieren, um die Dateinamenerweiterung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5e579-173">The [OpenSearch](https://github.com/dewitt/opensearch) provider does not attempt to parse the **Url** attribute to locate the file name extension.</span></span>
-   <span data-ttu-id="5e579-174">Wenn `MIMEType` eine Dateinamenerweiterung zugeordnet ist, die auf dem Client Computer registriert ist, bestimmt der Anbieter, ob die Dateinamenerweiterung ein bekannter webdateityp ist (htm, HTML, ASP, aspx, PHP,. SWF,. stm).</span><span class="sxs-lookup"><span data-stu-id="5e579-174">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the provider determines whether the file name extension is a known web file type (.htm, .html, .asp, .aspx, .php, .swf, .stm).</span></span> <span data-ttu-id="5e579-175">Wenn dies der Fall ist, wird der Dateityp als weblinktyp betrachtet. Andernfalls wird Sie als Dateityp betrachtet.</span><span class="sxs-lookup"><span data-stu-id="5e579-175">If so, the file type is regarded as a web link type; otherwise, it is regarded as a file type.</span></span> <span data-ttu-id="5e579-176">Wenn dem z. b. die `MIMEType "text/html"` Dateinamenerweiterung. htm zugeordnet ist, wird dieses Element als Weblink anstelle von als htm-Dateityp betrachtet.</span><span class="sxs-lookup"><span data-stu-id="5e579-176">For example, if the `MIMEType "text/html"` is associated with the .htm file name extension, that item is regarded as a web link instead of as an .htm file type.</span></span>

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a><span data-ttu-id="5e579-177">Vermeiden potenzieller Barrieren für die Aktivierung eines Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="5e579-177">Avoiding Potential Barriers to Enabling a Data Store</span></span>

<span data-ttu-id="5e579-178">Einige Datenspeicher stellen keinen mit [OpenSearch](https://github.com/dewitt/opensearch)kompatiblen Webdienst bereit, können aber weiterhin mit der Windows-Verbund Suche verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="5e579-178">Some data stores do not provide an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service but can still be connected to Windows Federated Search.</span></span> <span data-ttu-id="5e579-179">Zu diesen Daten speichern gehören:</span><span class="sxs-lookup"><span data-stu-id="5e579-179">Such data stores include:</span></span>

-   <span data-ttu-id="5e579-180">Remote Indizes mit Authentifizierungsmethoden, die in der Windows 7-Verbund Suche nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5e579-180">Remote indexes with authentication methods that are not supported in Windows 7 Federated Search.</span></span>

    <span data-ttu-id="5e579-181">Beispiele hierfür sind die Formular basierte Authentifizierung und andere benutzerdefinierte Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="5e579-181">Examples include forms-based authentication and other custom authentication methods.</span></span>

-   <span data-ttu-id="5e579-182">Wenn ein Öffentlicher Informationsspeicher über öffentliche Web-APIs verfügt, kann jeder einen anderen Webdienst schreiben, der mit [OpenSearch](https://github.com/dewitt/opensearch)kompatibel ist, und diese APIs im Hintergrund aufruft.</span><span class="sxs-lookup"><span data-stu-id="5e579-182">If a high-value public store has public web APIs, anyone can write another web service that is [OpenSearch](https://github.com/dewitt/opensearch)-compatible and calls those APIs behind the scenes.</span></span>

    <span data-ttu-id="5e579-183">Beispiele hierfür sind die Library of Congress und die medizinischen Forschungsdatenbanken.</span><span class="sxs-lookup"><span data-stu-id="5e579-183">Examples include the Library of Congress, and medical research databases.</span></span>

-   <span data-ttu-id="5e579-184">Proprietäre Enterprise-Datenspeicher oder-Indizes sowie Legacy-Inhalts Verwaltungs Speicher, für die es möglicherweise unmöglich ist, ein Front-End zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5e579-184">Proprietary enterprise data stores or indexes, and legacy content management stores, for which it might be impossible to implement a front end.</span></span>

<span data-ttu-id="5e579-185">Es gibt jedoch Alternativen, mit denen Barrieren zum Aktivieren eines Datenspeicher vermieden werden können.</span><span class="sxs-lookup"><span data-stu-id="5e579-185">However, there are alternatives that can avoid barriers to enabling a data store.</span></span> <span data-ttu-id="5e579-186">Im folgenden sind einige dieser Alternativen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5e579-186">The following are some of those alternatives:</span></span>

<span data-ttu-id="5e579-187">**Zum Schreiben eines Webdiensts für mittlere Menschen, wenn der Webdienst für die vorhandene Datenquelle nicht geändert werden kann oder wenn der Webdienst eine benutzerdefinierte API bereitstellt:**</span><span class="sxs-lookup"><span data-stu-id="5e579-187">**To write a middle-man web service when you cannot modify the web service for the existing data source, or the web service provides a custom API:**</span></span>

1.  <span data-ttu-id="5e579-188">Schreiben eines Middle-man-Webdiensts, der eine Windows 7-Abfrage akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="5e579-188">Write a middle-man web service that can accept a Windows 7 query.</span></span>
2.  <span data-ttu-id="5e579-189">Stellen Sie eine Verbindung mit Ihrer Datenquelle her, und rufen Sie die Abfrageergebnisse ab.</span><span class="sxs-lookup"><span data-stu-id="5e579-189">Connect to your data source, and retrieve the query results.</span></span>
3.  <span data-ttu-id="5e579-190">Formatieren Sie die Ergebnisse im RSS-oder Atom-Format neu.</span><span class="sxs-lookup"><span data-stu-id="5e579-190">Reformat the results in RSS or Atom format.</span></span>
4.  <span data-ttu-id="5e579-191">Die Ergebnisse werden an den Windows 7-Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e579-191">Return the results to the Windows 7 client.</span></span>
5.  <span data-ttu-id="5e579-192">Beachten Sie, dass Sie bei Enterprise Data Services und vielen Internet Datendiensten ggf. die Benutzer Anmelde Informationen im Namen des Webdiensts übergeben müssen, um die Ergebnis Kürzung basierend auf den Berechtigungen des Benutzers durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5e579-192">Note that for enterprise data services and many Internet data services, you may need to pass the user credentials through on behalf of the web service to perform result trimming based on the user's permissions.</span></span>

<span data-ttu-id="5e579-193">**So verwenden Sie eine vorhandene Suchmaschine, wenn Sie einen öffentlichen Datenspeicher nicht aktivieren können:**</span><span class="sxs-lookup"><span data-stu-id="5e579-193">**To use an existing search engine when you cannot enable a public data store:**</span></span>

1.  <span data-ttu-id="5e579-194">Verwenden Sie eine öffentliche Suchmaschine, die [OpenSearch](https://github.com/dewitt/opensearch) mit RSS bereits unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e579-194">Use a public search engine that already supports [OpenSearch](https://github.com/dewitt/opensearch) with RSS.</span></span> <span data-ttu-id="5e579-195">Hierzu können Sie Ihren Benutzern eine OSDX-Datei mit einer URL-Vorlage bereitstellen, die die Ergebnisse auf die für Ihre bestimmte Domäne beschränkt.</span><span class="sxs-lookup"><span data-stu-id="5e579-195">You can do so by providing your users with an .osdx file that has a URL template that restricts results to only those for your specific domain.</span></span>
2.  <span data-ttu-id="5e579-196">Sehen Sie sich das folgende Beispiel einer [OpenSearch](https://github.com/dewitt/opensearch) -Beschreibung an, um nur den Hilfe Inhalt für Windows zu suchen, indem Sie eine Abfrage für Live.com verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e579-196">See the following example of an [OpenSearch](https://github.com/dewitt/opensearch) description for searching only the Help content for Windows by using a query against live.com.</span></span>

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

<span data-ttu-id="5e579-197">**So verwenden Sie einen vorhandenen Index Server, der OpenSearch unterstützt, wenn Sie proprietäre Enterprise-Datenspeicher oder-Indizes nicht aktivieren können:**</span><span class="sxs-lookup"><span data-stu-id="5e579-197">**To use an existing indexing server that supports OpenSearch when you cannot enable proprietary enterprise data stores or indexes:**</span></span>

1.  <span data-ttu-id="5e579-198">Wählen Sie einen vorhandenen Index Server aus, der [OpenSearch](https://github.com/dewitt/opensearch) zum Indizieren ihres Inhalts unterstützt, z. b. den SharePoint-Such Server.</span><span class="sxs-lookup"><span data-stu-id="5e579-198">Select an existing indexing server that supports [OpenSearch](https://github.com/dewitt/opensearch) to index your content, such as the SharePoint Search Server.</span></span>
2.  <span data-ttu-id="5e579-199">Erstellen Sie eine OSDX-Datei, die die Ergebnisse aus dem SharePoint-Index auf die von Ihrem Server beschränkt, indem Sie Ihre Schlüsselwort Syntax in der URL-Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e579-199">Create an .osdx file that restricts the results from the SharePoint index to only those from your server by using their KeyWord syntax within the URL template.</span></span>

<span data-ttu-id="5e579-200">**So schreiben Sie einen Client seitigen Datenspeicher, wenn eine serverseitige Lösung nicht funktioniert:**</span><span class="sxs-lookup"><span data-stu-id="5e579-200">**To write a client-side data store if a server-side-only solution does not work:**</span></span>

1.  <span data-ttu-id="5e579-201">Schreiben Sie eine Client seitige [OpenSearch](https://github.com/dewitt/opensearch) -Datenquelle, die sich zwischen dem Windows [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter und der externen Datenquelle befindet.</span><span class="sxs-lookup"><span data-stu-id="5e579-201">Write a client-side [OpenSearch](https://github.com/dewitt/opensearch) data source that sits between the Windows [OpenSearch](https://github.com/dewitt/opensearch) provider and the external data source.</span></span>
2.  <span data-ttu-id="5e579-202">Verwenden Sie die [iopensearchsource-Schnittstellen](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) -API im Windows SDK, um eine ordnungsgemäß konfigurierte. searchconnector-MS-Datei zu erstellen, über die Windows-Explorer Ihre Implementierung mit den Abfrage Parametern abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="5e579-202">Use the [IOpenSearchSource Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API in the Windows SDK to create an appropriately configured .searchconnector-ms file through which Windows Explorer can call your implementation with the query parameters.</span></span> <span data-ttu-id="5e579-203">Ihre Implementierung kann dann Ergebnisse im RSS-oder Atom-Format zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5e579-203">Your implementation can then return results formatted in RSS or Atom format.</span></span> <span data-ttu-id="5e579-204">Dadurch kann Ihre Implementierung benutzerdefinierte Benutzeroberfläche für die Authentifizierung bereitstellen und über die proprietäre API eine Verbindung mit der Datenquelle herstellen.</span><span class="sxs-lookup"><span data-stu-id="5e579-204">Doing so enables your implementation to provide custom authentication UI and to connect to the data source using its proprietary API.</span></span>

> [!Note]  
> <span data-ttu-id="5e579-205">Beim Öffnen einer OSDX-Datei wird eine searchconnector-MS-Datei (Search-Connector) im Verzeichnis "% User Profile%/searches" erstellt, und es wird ein Link zu dieser Datei im Verzeichnis "% User Profile%/Links" platziert.</span><span class="sxs-lookup"><span data-stu-id="5e579-205">Opening an .osdx file creates a .searchconnector-ms file (search connector) in the %userprofile%/searches directory and places a link to it in the %userprofile%/links directory.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="5e579-206">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e579-206">Additional Resources</span></span>

<span data-ttu-id="5e579-207">Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e579-207">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e579-208">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e579-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e579-209">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="5e579-209">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="5e579-210">Ersten Einstieg in die Verbund Suche in Windows</span><span class="sxs-lookup"><span data-stu-id="5e579-210">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="5e579-211">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="5e579-211">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="5e579-212">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="5e579-212">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="5e579-213">Bewährte Methoden bei der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="5e579-213">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="5e579-214">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="5e579-214">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
