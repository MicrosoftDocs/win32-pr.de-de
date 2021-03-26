---
description: Ein Zuordnungs Array ist eine geordnete Liste von Registrierungsstellen, die zum Speichern von Informationen zu einem Elementtyp verwendet werden, einschließlich Handlern, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs.
title: Zuordnungs Arrays
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128888"
---
# <a name="association-arrays"></a><span data-ttu-id="ba86c-103">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="ba86c-103">Association Arrays</span></span>

<span data-ttu-id="ba86c-104">Ein Zuordnungs Array ist eine geordnete Liste von Registrierungsstellen, die zum Speichern von Informationen zu einem Elementtyp verwendet werden, einschließlich Handlern, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs.</span><span class="sxs-lookup"><span data-stu-id="ba86c-104">An association array is an ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="ba86c-105">Die Shell verwendet Zuordnungs Arrays, um einen vordefinierten Satz von Registrierungs Speicherorten abzufragen, die möglicherweise Informationen über ein shellelement enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba86c-105">The Shell uses association arrays to query a predefined set of registry locations that might contain information about a Shell item.</span></span>

<span data-ttu-id="ba86c-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="ba86c-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ba86c-107">Informationen zu Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="ba86c-107">About Association Arrays</span></span>](#about-association-arrays)
-   [<span data-ttu-id="ba86c-108">Abfragen von Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="ba86c-108">Querying Association Arrays</span></span>](#querying-association-arrays)
-   [<span data-ttu-id="ba86c-109">Arbeiten mit Zuordnungs Arrays für eine bestimmte shelldatenquelle</span><span class="sxs-lookup"><span data-stu-id="ba86c-109">Working with Association Arrays for a Particular Shell Data Source</span></span>](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [<span data-ttu-id="ba86c-110">Arrays der Shell-Datenquellen Zuordnung</span><span class="sxs-lookup"><span data-stu-id="ba86c-110">Shell Data Source Association Arrays</span></span>](#shell-data-source-association-arrays)
-   [<span data-ttu-id="ba86c-111">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba86c-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="ba86c-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba86c-112">Related topics</span></span>](#related-topics)

## <a name="about-association-arrays"></a><span data-ttu-id="ba86c-113">Informationen zu Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="ba86c-113">About Association Arrays</span></span>

<span data-ttu-id="ba86c-114">Ein Zuordnungs Array ist eine geordnete Liste von Registrierungsstellen, die Informationen zu einem Elementtyp enthalten, einschließlich Handlern, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs.</span><span class="sxs-lookup"><span data-stu-id="ba86c-114">An association array is an ordered list of registry locations that contain information about an item type, including handlers, verbs, and other attributes such as the icon and display name of the type.</span></span> <span data-ttu-id="ba86c-115">Diese Informationen zum Elementtyp können auf unterschiedlichen Genauigkeits Graden registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ba86c-115">This information about the item type can be registered at varying levels of specificity.</span></span> <span data-ttu-id="ba86c-116">Beispielsweise können Sie ein Verb registrieren, das nur für einen bestimmten Dateityp (z. b.. jpg) oder für alle Elemente mit dem gleichen System. Kind (z. b. System. Kind = Bild) oder für alle Elemente angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ba86c-116">For example, you can register a verb that will show up only for a specific file type (such as .jpg), or for all items with the same System.Kind (for example, System.kind = picture), or for all items.</span></span>

<span data-ttu-id="ba86c-117">Die Shell verwendet Zuordnungs Arrays, um einen vordefinierten Satz von Registrierungs Speicherorten abzufragen, die möglicherweise Informationen über das Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba86c-117">The Shell uses association arrays to query a predefined set of registry locations that might potentially contain information about the item.</span></span> <span data-ttu-id="ba86c-118">Die Association Array-APIs können verwendet werden, um aus dem Registrierungs Unterschlüssel einen einzelnen Wert abzurufen, der die angeforderten Informationen enthält. dieser Wert stammt aus dem ersten Eintrag im Array, der ihn bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ba86c-118">The association array APIs can be used to retrieve from the registry subkey a single value that contains the requested information, with that value coming from the first entry in the array that provides it.</span></span> <span data-ttu-id="ba86c-119">Beispielsweise wird der Standard Symbolwert auf diese Weise abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba86c-119">For example, the default icon value is retrieved this way.</span></span> <span data-ttu-id="ba86c-120">Das Association-Array kann auch verwendet werden, um einen Satz von Werten abzurufen, die in den Registrierungs unter Schlüsseln gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ba86c-120">The association array can also be used to retrieve a set of values that are stored in the registry subkeys.</span></span> <span data-ttu-id="ba86c-121">Beispielsweise wird die Liste der Verben aus den Verben erstellt, die unter allen unter Schlüsseln registriert sind.</span><span class="sxs-lookup"><span data-stu-id="ba86c-121">For example, the list of verbs is built from those verbs that are registered under all the subkeys.</span></span>

<span data-ttu-id="ba86c-122">Nachdem die Shell einen vordefinierten Satz von Registrierungs Speicherorten für Informationen über ein shellelement abgefragt hat, werden die Registrierungs Orte von der spezifischsten Position bis zum allgemeinsten in ein Array eingefügt.</span><span class="sxs-lookup"><span data-stu-id="ba86c-122">After the Shell queries a predefined set of registry locations for information about a Shell item, it puts the registry locations into an array in order from the most specific location to the most general.</span></span>

<span data-ttu-id="ba86c-123">Da Zuordnungs Arrays geordnete Listen sind, stellen Sie Anwendungsentwicklern einen Mechanismus zum Hinzufügen von Informationen zur Registrierung zur Verfügung, die für einen bestimmten Elementtyp zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba86c-123">Because association arrays are ordered lists, they provide application developers with a mechanism for adding information to the registry that will be returned for a specific type of item.</span></span> <span data-ttu-id="ba86c-124">Ebenso ermöglichen Zuordnungs Arrays Anwendungsentwicklern das Hinzufügen von Informationen zur Registrierung für eine bestimmte Gruppe von Elementen, wenn diese Elemente an einem allgemeineren Speicherort registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ba86c-124">Likewise, association arrays permit application developers to add information to the registry for a specific group of items when those items are registered at a more general location.</span></span> <span data-ttu-id="ba86c-125">Diese Logik informiert Sie über den am besten geeigneten Speicherort in der Registrierung, um Informationen zu shellelementen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ba86c-125">This logic informs your decision about the most appropriate location in the registry to store information about Shell items.</span></span>

<span data-ttu-id="ba86c-126">In einem standardmäßigen Windows-System weist eine JPG-Datei das folgende Zuordnungs Array auf:</span><span class="sxs-lookup"><span data-stu-id="ba86c-126">On a default Windows system a .jpg file has the following association array:</span></span>

-   <span data-ttu-id="ba86c-127">**HKEY \_ Klassen \_** Stamm- \\ **jpgfile**</span><span class="sxs-lookup"><span data-stu-id="ba86c-127">**HKEY\_CLASSES\_ROOT**\\**jpgfile**</span></span>
-   <span data-ttu-id="ba86c-128">**HKEY \_ Klassen \_** Stamm \\ **systemfilezuordnungen** \\ **. jpg**</span><span class="sxs-lookup"><span data-stu-id="ba86c-128">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.jpg**</span></span>
-   <span data-ttu-id="ba86c-129">**HKEY \_ Klassen \_** Stamm \\ **Bild**</span><span class="sxs-lookup"><span data-stu-id="ba86c-129">**HKEY\_CLASSES\_ROOT**\\**image**</span></span>
-   <span data-ttu-id="ba86c-130">**HKEY \_ Klassen \_** Stamm \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="ba86c-130">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="ba86c-131">_ *HKEY- \_ Klassen \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="ba86c-131">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>

<span data-ttu-id="ba86c-132">Informationen zum Registrieren von Zuordnungs Arrays finden Sie unter [Anwendungs Registrierung](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="ba86c-132">For information on registering association arrays, see [Application Registration](app-registration.md).</span></span>

## <a name="querying-association-arrays"></a><span data-ttu-id="ba86c-133">Abfragen von Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="ba86c-133">Querying Association Arrays</span></span>

<span data-ttu-id="ba86c-134">Es gibt Shell-APIs zum Abrufen von Informationen aus einem Bereich von Registrierungs unter Schlüsseln, vom spezifischsten Registrierungs Unterschlüssel zu einer übergeordneten Menge der Informationen für alle Registrierungs Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="ba86c-134">There are Shell APIs to retrieve information from a range of registry subkeys, from the most specific registry subkey to a superset of the information across all registry subkeys.</span></span>

<span data-ttu-id="ba86c-135">Die häufigste Verwendung eines Zuordnungs Arrays besteht darin, einen einzelnen Wert abzufragen, den die Shell aus dem spezifischsten Element im Array zurückgibt, das über die angeforderten Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="ba86c-135">The most common use of an association array is to query for a single value that the Shell returns from the most specific element in the array that has the requested information.</span></span> <span data-ttu-id="ba86c-136">Das folgende Codebeispiel zeigt, wie Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="ba86c-136">The following code example shows how to do that.</span></span>


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



<span data-ttu-id="ba86c-137">Die folgenden APIs können zum Abfragen eines Zuordnungs Arrays oder zum Erstellen eines Zuordnungs Array- [**iqueryassociation**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Objekts verwendet werden, das abgefragt werden kann:</span><span class="sxs-lookup"><span data-stu-id="ba86c-137">The following APIs can be used to query an association array or to construct an association array [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) object that can be queried:</span></span>

-   <span data-ttu-id="ba86c-138">[**Assoccreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (vor Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="ba86c-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prior to Windows Vista)</span></span>
-   [<span data-ttu-id="ba86c-139">**Assockreateforclasses**</span><span class="sxs-lookup"><span data-stu-id="ba86c-139">**AssocCreateForClasses**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [<span data-ttu-id="ba86c-140">**Assocquerystring**</span><span class="sxs-lookup"><span data-stu-id="ba86c-140">**AssocQueryString**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a><span data-ttu-id="ba86c-141">Arbeiten mit Zuordnungs Arrays für eine bestimmte shelldatenquelle</span><span class="sxs-lookup"><span data-stu-id="ba86c-141">Working with Association Arrays for a Particular Shell Data Source</span></span>

<span data-ttu-id="ba86c-142">Jede shelldatenquelle definiert das Zuordnungs Array für ihre Elemente.</span><span class="sxs-lookup"><span data-stu-id="ba86c-142">Each Shell data source defines the association array for its items.</span></span> <span data-ttu-id="ba86c-143">Die Definition eines Zuordnungs Arrays ist in der Regel eine Funktion des Elementtyps.</span><span class="sxs-lookup"><span data-stu-id="ba86c-143">Defining an association array is usually a function of the type of item.</span></span> <span data-ttu-id="ba86c-144">Die Implementierer von shelldatenquellen müssen die Zuordnungs Arrays definieren und dokumentieren, damit Anwendungen das Verhalten dieser Typen, z. b. das Registrieren von Verben oder anderen Informationen, erweitern können.</span><span class="sxs-lookup"><span data-stu-id="ba86c-144">Shell data source implementers should define and document the association arrays to enable applications to extend the behavior of those types, such as for registering verbs or other information.</span></span> <span data-ttu-id="ba86c-145">Anwendungen können das Verhalten von Elementen erweitern, basierend auf dem Hinzufügen von Daten zu den unter Schlüsseln des Assoziations Arrays, z. b. Hinzufügen von Verben für Elemente</span><span class="sxs-lookup"><span data-stu-id="ba86c-145">Applications can extend the behavior of items based on adding data to the association array subkeys, such as adding verbs for items.</span></span>

<span data-ttu-id="ba86c-146">Die Dateisystem-Datenquelle erstellt ein Zuordnungs Array für Dateien, die auf den folgenden Registrierungs unter Schlüsseln und speziellen ProgIDs basieren:</span><span class="sxs-lookup"><span data-stu-id="ba86c-146">The file system data source builds an association array for files based on the following registry subkeys and special ProgIDs:</span></span>

-   <span data-ttu-id="ba86c-147">Wenn die Datei eine registrierte ProgID hat, wird die Stamm-ProgID der **HKEY- \_ Klassen \_** \\  verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba86c-147">If the file has a registered ProgID, **HKEY\_CLASSES\_ROOT**\\*ProgID* is used.</span></span> <span data-ttu-id="ba86c-148">Andernfalls wird der Stamm der **HKEY- \_ Klassen \_**" \\ **Unknown** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba86c-148">Otherwise **HKEY\_CLASSES\_ROOT**\\**Unknown** is used.</span></span>
-   <span data-ttu-id="ba86c-149">Die Dateinamenerweiterung wird unter **HKEY \_ Classes \_ root** \\ **systemfileassociations** \\ *. FileExtension* unter Key registriert.</span><span class="sxs-lookup"><span data-stu-id="ba86c-149">The file name extension is registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ *.fileExtension* subkey.</span></span>
-   <span data-ttu-id="ba86c-150">In der folgenden Tabelle sind spezielle ProgIDs aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba86c-150">Special ProgIDs are shown in the following table.</span></span> 

    | <span data-ttu-id="ba86c-151">Besondere ProgID</span><span class="sxs-lookup"><span data-stu-id="ba86c-151">Special progID</span></span>                                    | <span data-ttu-id="ba86c-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba86c-152">Description</span></span>                   |
    |---------------------------------------------------|-------------------------------|
    | <span data-ttu-id="ba86c-153">**HKEY \_ Klassen \_** Stamm \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="ba86c-153">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>                   | <span data-ttu-id="ba86c-154">Alle Dateien (nicht-Ordner)</span><span class="sxs-lookup"><span data-stu-id="ba86c-154">All files (non-folders)</span></span>       |
    | <span data-ttu-id="ba86c-155">_ *HKEY- \_ Klassen \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="ba86c-155">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span> | <span data-ttu-id="ba86c-156">Dateien und Dateisystem Ordner</span><span class="sxs-lookup"><span data-stu-id="ba86c-156">Files and file system folders</span></span> |
    | <span data-ttu-id="ba86c-157">**HKEY \_ Klassen \_** Stamm \\ **Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="ba86c-157">**HKEY\_CLASSES\_ROOT**\\**Directory**</span></span>            | <span data-ttu-id="ba86c-158">Dateisystem Ordner</span><span class="sxs-lookup"><span data-stu-id="ba86c-158">File system folders</span></span>           |
    | <span data-ttu-id="ba86c-159">**HKEY \_ Klassen \_** Stamm \\ **Ordner**</span><span class="sxs-lookup"><span data-stu-id="ba86c-159">**HKEY\_CLASSES\_ROOT**\\**Folder**</span></span>               | <span data-ttu-id="ba86c-160">Shellcontainer</span><span class="sxs-lookup"><span data-stu-id="ba86c-160">Shell containers</span></span>              |

    

     

### <a name="shell-data-source-association-arrays"></a><span data-ttu-id="ba86c-161">Arrays der Shell-Datenquellen Zuordnung</span><span class="sxs-lookup"><span data-stu-id="ba86c-161">Shell Data Source Association Arrays</span></span>

<span data-ttu-id="ba86c-162">In der folgenden Liste sind einige der Arrays für die Shell-Datenspeicher Zuordnung dargestellt, die für die in diesem Thema beschriebenen Zwecke verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="ba86c-162">The following list represents some of the Shell data store association arrays that can be used for the purposes described in this topic:</span></span>

-   <span data-ttu-id="ba86c-163">**HKEY \_ Klassen \_** Stamm \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="ba86c-163">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="ba86c-164">_ *HKEY- \_ Klassen \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="ba86c-164">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>
-   <span data-ttu-id="ba86c-165">**HKEY \_ Klassen \_** StammKind.Doc-Enumerationselement \\ \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ba86c-165">**HKEY\_CLASSES\_ROOT**\\**Kind.Document**</span></span>
-   <span data-ttu-id="ba86c-166">**HKEY \_ Klassen \_** Stamm \\ **Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="ba86c-166">**HKEY\_CLASSES\_ROOT**\\**Results**</span></span>
-   <span data-ttu-id="ba86c-167">**HKEY \_ Klassen \_** Stamm \\ **systemfilezuordnungen** \\ **. docx**</span><span class="sxs-lookup"><span data-stu-id="ba86c-167">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.docx**</span></span>
-   <span data-ttu-id="ba86c-168">**HKEY \_ Klassen \_** StammWord.Doc-Enumerationselement \\ **. 12**</span><span class="sxs-lookup"><span data-stu-id="ba86c-168">**HKEY\_CLASSES\_ROOT**\\**Word.Document.12**</span></span>

<span data-ttu-id="ba86c-169">Arrays der Shell-Datenquellen Zuordnung, die für dbfolder (ein shelldatenspeicher, der Elemente in Suchergebnissen und Abfrage basierten Sichten darstellt) verwendet werden können, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba86c-169">Shell data source association arrays that can be used for DBFolder (a Shell data store that represents items in search results and query-based views) are as follows:</span></span>

-   <span data-ttu-id="ba86c-170">Laufwerke</span><span class="sxs-lookup"><span data-stu-id="ba86c-170">Drives</span></span>
-   <span data-ttu-id="ba86c-171">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ba86c-171">Network</span></span>
-   <span data-ttu-id="ba86c-172">Regitems</span><span class="sxs-lookup"><span data-stu-id="ba86c-172">RegItems</span></span>
-   <span data-ttu-id="ba86c-173">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="ba86c-173">Examples:</span></span>
    -   <span data-ttu-id="ba86c-174">ContentView</span><span class="sxs-lookup"><span data-stu-id="ba86c-174">ContentView</span></span>
    -   <span data-ttu-id="ba86c-175">Verben</span><span class="sxs-lookup"><span data-stu-id="ba86c-175">Verbs</span></span>

<span data-ttu-id="ba86c-176">Andere allgemeine Zuordnungs Arrays enthalten Ordner und Drucker.</span><span class="sxs-lookup"><span data-stu-id="ba86c-176">Other common association arrays include Folder and Printers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba86c-177">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba86c-177">Additional Resources</span></span>

-   <span data-ttu-id="ba86c-178">Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="ba86c-178">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba86c-179">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba86c-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba86c-180">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="ba86c-180">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="ba86c-181">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="ba86c-181">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="ba86c-182">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="ba86c-182">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="ba86c-183">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="ba86c-183">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="ba86c-184">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="ba86c-184">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="ba86c-185">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="ba86c-185">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="ba86c-186">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ba86c-186">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="ba86c-187">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="ba86c-187">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> </dl>

 

 
