---
description: Die automatische Vervollständigung erweitert Zeichen folgen, die teilweise in einem Bearbeitungs Steuerelement eingegeben wurden, in vollständige Zeichen folgen.
title: Verwenden von Auto Vervollständigen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977424"
---
# <a name="using-autocomplete"></a><span data-ttu-id="a7192-103">Verwenden von Auto Vervollständigen</span><span class="sxs-lookup"><span data-stu-id="a7192-103">Using Autocomplete</span></span>

<span data-ttu-id="a7192-104">Die automatische Vervollständigung erweitert Zeichen folgen, die teilweise in einem [Bearbeitungs Steuer](/windows/desktop/Controls/edit-controls) Element eingegeben wurden, in vollständige Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="a7192-104">Autocompletion expands strings that have been partially entered in an [edit control](/windows/desktop/Controls/edit-controls) into complete strings.</span></span> <span data-ttu-id="a7192-105">Wenn ein Benutzer beispielsweise die Eingabe einer URL in das Address Edit-Steuerelement startet, das in der Windows Internet Explorer-Symbolleiste eingebettet ist, erweitert die automatische Vervollständigung die Zeichenfolge in eine oder mehrere vollständige URL-Optionen, die mit der vorhandenen partiellen Zeichenfolge konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="a7192-105">For example, when a user starts to enter a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URL options that are consistent with the existing partial string.</span></span> <span data-ttu-id="a7192-106">Eine partielle URL-Zeichenfolge, z. b. "MIC", kann auf " https://www.microsoft.com " oder "" erweitert werden https://www.microsoft.com/windows .</span><span class="sxs-lookup"><span data-stu-id="a7192-106">A partial URL string such as "mic" might be expanded to "https://www.microsoft.com" or "https://www.microsoft.com/windows".</span></span> <span data-ttu-id="a7192-107">Die automatische Vervollständigung wird in der Regel mit Bearbeitungs Steuerelementen oder mit Steuerelementen verwendet, die ein eingebettetes Bearbeitungs Steuerelement wie das [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) -Steuerelement aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a7192-107">Autocompletion is typically used with edit controls or with controls that have an embedded edit control, such as the [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) control.</span></span>

## <a name="adding-autocomplete-functionality-to-your-application"></a><span data-ttu-id="a7192-108">Hinzufügen von Auto Vervollständigen-Funktionen zu Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="a7192-108">Adding Autocomplete Functionality to Your Application</span></span>

<span data-ttu-id="a7192-109">Eine Anwendung kann einem Bearbeitungs Steuerelement auf zwei Arten eine Auto Vervollständigen-Funktionalität hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="a7192-109">An application can add autocomplete functionality to an edit control in two ways:</span></span>

-   <span data-ttu-id="a7192-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) ist eine einfache Funktion, mit der ein Dateipfad oder eine URL automatisch vervollständigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7192-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) is a simple function that can autocomplete a file path or URL.</span></span>
-   <span data-ttu-id="a7192-111">Die [**iautocomplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) -Schnittstelle wird durch das Auto Vervollständigen-Objekt (CLSID \_ Auto Vervollständigen) verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a7192-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) interface is exposed by the autocomplete object (CLSID\_AutoComplete).</span></span> <span data-ttu-id="a7192-112">Sie ermöglicht es Anwendungen, das-Objekt zu initialisieren, zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a7192-112">It allows applications to initialize, enable, and disable the object.</span></span> <span data-ttu-id="a7192-113">**Iautocomplete** ermöglicht mehr Kontrolle über Auto Vervollständigen-Quellen, einschließlich der Möglichkeit, eine benutzerdefinierte Quelle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a7192-113">**IAutoComplete** allows more control over autocomplete sources, including the ability to add a custom source.</span></span> <span data-ttu-id="a7192-114">Im restlichen Teil dieses Themas wird die Verwendung von **iautocomplete** erläutert.</span><span class="sxs-lookup"><span data-stu-id="a7192-114">The remainder of this topic discusses the use of **IAutoComplete**.</span></span> <span data-ttu-id="a7192-115">Weitere Informationen finden [Sie unter Manuelles Aktivieren von AutoComplete](how-to-enable-autocomplete-manually.md) für bestimmte Verwendungs Beispiele.</span><span class="sxs-lookup"><span data-stu-id="a7192-115">See [How To Enable Autocomplete Manually](how-to-enable-autocomplete-manually.md) for specific usage examples.</span></span>

## <a name="autocomplete-modes"></a><span data-ttu-id="a7192-116">Auto Vervollständigen-Modi</span><span class="sxs-lookup"><span data-stu-id="a7192-116">Autocomplete Modes</span></span>

<span data-ttu-id="a7192-117">Wenn Sie [**iautocomplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)verwenden, kann die automatische Vervollständigung die abgeschlossene Zeichenfolge in zwei Modi anzeigen: AutoAppend und AutoVorschlagen.</span><span class="sxs-lookup"><span data-stu-id="a7192-117">When using [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), autocompletion can display the completed string in two modes: autoappend and autosuggest.</span></span> <span data-ttu-id="a7192-118">Die Modi sind unabhängig. Sie können entweder oder beides aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a7192-118">The modes are independent; you can enable either or both.</span></span> <span data-ttu-id="a7192-119">Um den Modus anzugeben, geben Sie [**IAutoComplete2:: \* toptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)an.</span><span class="sxs-lookup"><span data-stu-id="a7192-119">To specify the mode, call [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span></span>

<dl> <dt>

<span data-ttu-id="a7192-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Automatisch anfügen</span><span class="sxs-lookup"><span data-stu-id="a7192-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span></span>
</dt> <dd>

<span data-ttu-id="a7192-121">Im AutoAppend-Modus fügt die automatische Vervollständigung den Rest der wahrscheinlichsten Kandidaten Zeichenfolge an die vorhandenen Zeichen an, wobei die angefügten Zeichen hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="a7192-121">In autoappend mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters.</span></span> <span data-ttu-id="a7192-122">Wenn der Benutzer weiterhin Zeichen eingibt, werden diese der vorhandenen partiellen Zeichenfolge hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a7192-122">If the user continues to enter characters, they are added to the existing partial string.</span></span> <span data-ttu-id="a7192-123">Wenn der Benutzer ein Zeichen hinzufügt, das mit dem nächsten markierten Zeichen identisch ist, wird die Hervorhebung für dieses Zeichen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a7192-123">If the user adds a character that is identical to the next highlighted character, the highlighting for that character is turned off.</span></span> <span data-ttu-id="a7192-124">Die restlichen Zeichen werden weiterhin hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a7192-124">The remaining characters will still be highlighted.</span></span> <span data-ttu-id="a7192-125">Wenn der Benutzer ein Zeichen hinzufügt, das nicht mit dem nächsten markierten Zeichen identisch ist, versucht die automatische Vervollständigung, eine neue Kandidaten Zeichenfolge auf der Grundlage der größeren partiellen Zeichenfolge zu generieren, und fügt den Rest der neuen Kandidaten Zeichenfolge der aktuellen partiellen Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="a7192-125">If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string and appends the remainder of the new candidate string to the current partial string.</span></span> <span data-ttu-id="a7192-126">Wenn keine Kandidaten Zeichenfolge gefunden werden kann, werden nur die typisierten Zeichen angezeigt, und das Bearbeitungsfeld verhält sich wie ohne die automatische Vervollständigung.</span><span class="sxs-lookup"><span data-stu-id="a7192-126">If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion.</span></span> <span data-ttu-id="a7192-127">Dieser Prozess wird fortgesetzt, bis der Benutzer eine Zeichenfolge annimmt.</span><span class="sxs-lookup"><span data-stu-id="a7192-127">This process continues until the user accepts a string.</span></span>

</dd> <dt>

<span data-ttu-id="a7192-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>-Vorschlags Suche</span><span class="sxs-lookup"><span data-stu-id="a7192-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest</span></span>
</dt> <dd>

<span data-ttu-id="a7192-129">Im Auto vorschlagen-Modus zeigt die automatische Vervollständigung eine Dropdown Liste mit einer oder mehreren vorgeschlagenen vollständigen Zeichen folgen unterhalb des Bearbeitungs Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="a7192-129">In autosuggest mode, autocompletion displays a drop-down list, with one or more suggested complete strings, beneath the edit control.</span></span> <span data-ttu-id="a7192-130">Der Benutzer kann eine der vorgeschlagenen Zeichen folgen auswählen oder mit der Eingabe fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a7192-130">The user can select one of the suggested strings or continue typing.</span></span> <span data-ttu-id="a7192-131">Wenn die Typisierung durchlaufen wird, kann die Dropdown Liste basierend auf der aktuellen partiellen Zeichenfolge geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a7192-131">As typing progresses, the drop-down list might be modified based on the current partial string.</span></span> <span data-ttu-id="a7192-132">Wenn Sie das Flag für die ACO- \_ Suche in [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)festlegen, stellt Auto Vervollständigen unten in der Dropdown Liste eine Option für die Suche nach der aktuellen Teil Zeichenfolge bereit.</span><span class="sxs-lookup"><span data-stu-id="a7192-132">If you set the ACO\_SEARCH flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), autocomplete provides an option, at the bottom of the drop-down list, to search for the current partial string.</span></span> <span data-ttu-id="a7192-133">Diese Option wird auch dann angezeigt, wenn keine empfohlenen Zeichen folgen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a7192-133">This option is displayed even if there are no suggested strings.</span></span> <span data-ttu-id="a7192-134">Wenn der Benutzer die Suchoption auswählt, sollte Ihre Anwendung eine Suchmaschine starten, um den Benutzer zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a7192-134">If the user selects the search option, your application should launch a search engine to assist the user.</span></span>

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a><span data-ttu-id="a7192-135">Verwenden vordefinierter Auto Vervollständigen-Quellen</span><span class="sxs-lookup"><span data-stu-id="a7192-135">Using Predefined Autocomplete Sources</span></span>

<span data-ttu-id="a7192-136">Die automatische Vervollständigung hängt von der Quelle ab, die Ihr Zeichen folgen zur Verfügung stellt, die mit der Teil Zeichenfolge des Benutzers verglichen werden</span><span class="sxs-lookup"><span data-stu-id="a7192-136">Autocompletion depends on having a source that provides it with strings to match against the user's partial string.</span></span> <span data-ttu-id="a7192-137">Sie haben die Möglichkeit, eine benutzerdefinierte Auto Vervollständigen-Quelle bereitzustellen, aber einige der gängigsten Quellen werden vom System bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a7192-137">You have the option of providing a custom autocomplete source, but several of the most common sources are provided by the system.</span></span>

<dl> <dt>

<span data-ttu-id="a7192-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID- \_ aclhistory</span><span class="sxs-lookup"><span data-stu-id="a7192-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID\_ACLHistory</span></span>
</dt> <dd>

<span data-ttu-id="a7192-139">Eine Auto Vervollständigen-Quelle, die mit der URL-Liste in der Verlaufs Liste des Benutzers übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a7192-139">An autocomplete source that matches against the URL list in the user's History list.</span></span>

</dd> <dt>

<span data-ttu-id="a7192-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID- \_ aclmru</span><span class="sxs-lookup"><span data-stu-id="a7192-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID\_ACLMRU</span></span>
</dt> <dd>

<span data-ttu-id="a7192-141">Eine Auto Vervollständigen-Quelle, die mit der URL-Liste in der Liste der zuletzt verwendeten Benutzer übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a7192-141">An autocomplete source that matches against the URL list in the user's Recently Used list.</span></span>

</dd> <dt>

<span data-ttu-id="a7192-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID- \_ aclistisf</span><span class="sxs-lookup"><span data-stu-id="a7192-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID\_ACListISF</span></span>
</dt> <dd>

<span data-ttu-id="a7192-143">Eine Auto Vervollständigen-Quelle, die mit Elementen im Shellnamespace übereinstimmt: Dateien auf dem Computer des Benutzers sowie Elemente in virtuellen Ordnern, z. b. in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="a7192-143">An autocomplete source that matches against items in the Shell namespace: files on the user's computer as well as items in virtual folders such as Control Panel.</span></span>

</dd> </dl>

<span data-ttu-id="a7192-144">Es gibt Situationen, in denen Sie anstelle der sofortigen Freigabe der Ressourcen die Schnittstellen Zeiger auf die verschiedenen an AutoComplete beteiligten Objekte beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="a7192-144">There are occasions when, rather than immediately freeing the resources, you might want to retain the interface pointers to the various objects involved in autocomplete.</span></span> <span data-ttu-id="a7192-145">Dies ist insbesondere dann der Fall, wenn Sie das Auto Vervollständigen-Verhalten dynamisch anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="a7192-145">In particular, this is done when you want to adjust the autocomplete behavior dynamically.</span></span> <span data-ttu-id="a7192-146">Die häufigste Instanz dieses Vorgangs tritt auf, wenn das CLSID- \_ aclistisf-Objekt verwendet wird, das automatisch vom Shell-Namespace vervollständigt wird und die Option ([**aclo \_ CurrentDir**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) der Auflistung aus dem aktuellen Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="a7192-146">The most common instance of this occurs when using the CLSID\_ACListISF object, which autocompletes from the Shell namespace and has the option ([**ACLO\_CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) of enumerating from the current directory as well.</span></span> <span data-ttu-id="a7192-147">Wenn Sie z. b. zu einem neuen Ordner navigieren, ändert Internet Explorer das aktuelle Verzeichnis der Adressleiste, sodass die Einstellungen dynamisch geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a7192-147">For example, when you navigate to a new folder, Internet Explorer changes the Address bar's current directory and therefore the settings need to be changed dynamically.</span></span> <span data-ttu-id="a7192-148">Es gibt zwei Möglichkeiten, das Verzeichnis anzugeben, das vom CLSID- \_ aclistisf-Objekt als Aktuelles Verzeichnis behandelt werden soll:</span><span class="sxs-lookup"><span data-stu-id="a7192-148">There are two ways to specify the directory that the CLSID\_ACListISF object should treat as the current directory:</span></span>

-   <span data-ttu-id="a7192-149">[**Ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) gibt das Verzeichnis über eine [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)an.</span><span class="sxs-lookup"><span data-stu-id="a7192-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifies the directory through an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span></span>
-   <span data-ttu-id="a7192-150">[**Icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) gibt das Verzeichnis über eine Pfad Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="a7192-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifies the directory through a path string.</span></span>

<span data-ttu-id="a7192-151">Gehen Sie wie folgt vor, dass **PAL** ein Zeiger auf die [**iaclist**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) -Schnittstelle eines CLSID- \_ aclistisf-Objekts ist:</span><span class="sxs-lookup"><span data-stu-id="a7192-151">In the following, assume that **pal** is a pointer to the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) interface of a CLSID\_ACListISF object:</span></span>

-   <span data-ttu-id="a7192-152">Verwenden von " [**ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)":</span><span class="sxs-lookup"><span data-stu-id="a7192-152">Using [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span></span>

    <span data-ttu-id="a7192-153">Um dem CLSID- \_ aclistisf-Objekt mitzuteilen, dass eine bestimmte [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) als Aktuelles Verzeichnis behandelt werden soll, können Sie die [**ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) -Schnittstelle des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7192-153">To tell the CLSID\_ACListISF object that a particular [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) should be treated as the current directory, you can use the object's [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) interface.</span></span> <span data-ttu-id="a7192-154">Da eine **itemittel List** auf einen virtuellen Ordner verweisen kann, ist diese Methode flexibler als die Verwendung von [**icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span><span class="sxs-lookup"><span data-stu-id="a7192-154">Since an **ITEMIDLIST** can refer to a virtual folder, this method is more flexible than using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span></span>

    <span data-ttu-id="a7192-155">Beachten Sie, dass in den folgenden Beispielen die vorlagenbasierte QueryInterface-Schnittstelle verwendet wird, die eine vereinfachte Parameterliste zulässt.</span><span class="sxs-lookup"><span data-stu-id="a7192-155">Note that the following examples use the templatized QueryInterface, which allows for a simplified parameter list.</span></span>

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   <span data-ttu-id="a7192-156">Verwenden von [**icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span><span class="sxs-lookup"><span data-stu-id="a7192-156">Using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span></span>

    <span data-ttu-id="a7192-157">Um dem CLSID- \_ aclistisf-Objekt einen Pfad als Aktuelles Verzeichnis zu übergeben, können Sie die [**icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) -Schnittstelle des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7192-157">To give the CLSID\_ACListISF object a path as the current directory, you can use the object's [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) interface.</span></span>

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
