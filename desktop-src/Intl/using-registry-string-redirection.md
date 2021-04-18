---
description: Die Speicherung von hart codierten Zeichen folgen in der Registrierung ist Teil eines Lokalisierungs Modells vor Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Verwenden von Registrierungs Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351589"
---
# <a name="using-registry-string-redirection"></a><span data-ttu-id="ee01a-103">Verwenden von Registrierungs Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="ee01a-103">Using Registry String Redirection</span></span>

<span data-ttu-id="ee01a-104">Die Speicherung von hart codierten Zeichen folgen in der Registrierung ist Teil eines Lokalisierungs Modells vor Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee01a-104">Storage of hard-coded strings in the registry is part of a pre-Windows Vista localization model.</span></span> <span data-ttu-id="ee01a-105">Sie wird von MUI nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-105">It is not supported by MUI.</span></span> <span data-ttu-id="ee01a-106">Im aktuellen Modell wird die Benutzeroberfläche für das Betriebssystem in sprachspezifischen Ressourcen Dateien oberhalb einer sprach neutralen Basis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-106">In the current model, the user interface for the operating system runs in language-specific resource files on top of a language-neutral base.</span></span> <span data-ttu-id="ee01a-107">Die Komponenten des Betriebssystems verwenden die Registrierung auf sprachneutrale Weise.</span><span class="sxs-lookup"><span data-stu-id="ee01a-107">The components of the operating system use the registry in a language-neutral manner.</span></span>

<span data-ttu-id="ee01a-108">MUI verwendet nur umgeleitete Registrierungs Zeichenfolgen, die von Win32 PE-Ressourcen in der Ressourcen Datei der Basis Sprache definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ee01a-108">MUI uses only redirected registry strings defined by Win32 PE resources in the base language resource file.</span></span> <span data-ttu-id="ee01a-109">Die Umleitung wird separat definiert, z. b. in einer INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="ee01a-109">Redirection is defined separately, for example, in an .inf file.</span></span> <span data-ttu-id="ee01a-110">Diese Art von Speicher ermöglicht es dem Ressourcen Lader, beim Laden von Ressourcen Modulen automatisch die richtigen Sprachressourcen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-110">This type of storage allows the resource loader to select the correct language resources automatically during resource module loading.</span></span>

> [!Note]  
> <span data-ttu-id="ee01a-111">Dieses Thema bezieht sich nur auf Win32 PE-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-111">This topic pertains only to Win32 PE resources.</span></span> <span data-ttu-id="ee01a-112">Bei Verwendung von nicht-Win32 PE-Ressourcen müssen Sie ggf. eine angepasste Registrierung für die Registrierungs Zeichenfolge bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-112">If using non-Win32 PE resources, you must provide customized registry string redirection, if required.</span></span>

 

## <a name="create-a-language-neutral-resource"></a><span data-ttu-id="ee01a-113">Erstellen einer Language-Neutral Ressource</span><span class="sxs-lookup"><span data-stu-id="ee01a-113">Create a Language-Neutral Resource</span></span>

<span data-ttu-id="ee01a-114">Eine MUI-Anwendung, die unter Windows Vista und höher ausgeführt wird, verwendet eine sprachneutrale Zeichen folgen Ressource, um den Zugriff auf sprachspezifische Zeichen folgen zuzulassen, die in einer Zeichen folgen Ressourcen Tabelle gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ee01a-114">A MUI application running on Windows Vista and later uses a language-neutral string resource to allow access to language-specific strings stored in a string resource table.</span></span> <span data-ttu-id="ee01a-115">Anwendungscode, der diese Werte aus der Registrierung liest, wird im Abschnitt Laden eines Language-Neutral Registrierungs Werts untersuchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee01a-115">Application code that reads these values from the registry is described in the Load a Language-Neutral Registry Value section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="ee01a-116">Die Daten für einen sprach neutralen Registrierungs Wert haben das Format " `@<PE-path>,-<stringID>[;<comment>]` ", wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="ee01a-116">The data for a language-neutral registry value has the format "`@<PE-path>,-<stringID>[;<comment>]`", where:</span></span>

-   <span data-ttu-id="ee01a-117">*PE-Path* gibt den Pfad der ausführbaren Datei an.</span><span class="sxs-lookup"><span data-stu-id="ee01a-117">*PE-path* specifies the path of the executable.</span></span> <span data-ttu-id="ee01a-118">Sie können den Pfad mithilfe einer Umgebungsvariablen, z. b .% Program Files%, angeben, um die Bereitstellung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-118">You can specify the path using an environment variable, such as %ProgramFiles%, to support deployment.</span></span> <span data-ttu-id="ee01a-119">Eine Alternative zum Erstellen des Zeichen folgen Verweises besteht darin, die Dateipfad Informationen auszulassen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-119">An alternative for making your string reference is to leave out the file path information.</span></span> <span data-ttu-id="ee01a-120">In diesem Fall muss Ihre Anwendung über eine bestimmte Möglichkeit verfügen, z. b. einen anderen Registrierungs Wert, um Ihr eigenes Installationsverzeichnis zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="ee01a-120">In this case, your application must have some means, for example, another registry value, to communicate its own install directory.</span></span>
-   <span data-ttu-id="ee01a-121">*stringID* gibt den numerischen Ressourcen Bezeichner der relevanten Zeichen folgen Ressource an, die wie jede andere lokalisierbare Zeichen folgen Ressource implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee01a-121">*stringID* specifies the numeric resource identifier of the relevant string resource, which is implemented just like any other localizable string resource.</span></span>
-   <span data-ttu-id="ee01a-122">der *Kommentar* gibt optionale Informationen zum Debuggen oder zur besseren Lesbarkeit des Registrierungs Werts an.</span><span class="sxs-lookup"><span data-stu-id="ee01a-122">*comment* specifies optional information for debugging or readability of the registry value.</span></span> <span data-ttu-id="ee01a-123">Die Registrierungs-API-Funktionen ignorieren den Kommentar beim Laden der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ee01a-123">The registry API functions ignore the comment when loading the string.</span></span>

> [!Note]  
> <span data-ttu-id="ee01a-124">Die Daten für den Registrierungs Wert machen keinen expliziten Verweis auf die sprachspezifische Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="ee01a-124">The data for the registry value makes no explicit reference to the language-specific resource file.</span></span> <span data-ttu-id="ee01a-125">Die richtige Datei wird zur Laufzeit basierend auf den aktuellen Spracheinstellungen der Benutzeroberfläche festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-125">The correct file is determined at runtime, based on the current user interface language preferences.</span></span>

 

<span data-ttu-id="ee01a-126">Ein Registrierungs Wert wird ohne Leerzeichen zwischen "," und "-" eingegeben.</span><span class="sxs-lookup"><span data-stu-id="ee01a-126">A registry value is entered without a space between the "," and "-".</span></span> <span data-ttu-id="ee01a-127">Ein korrekter Registrierungs Wert lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ee01a-127">A correct registry value is:</span></span>

`shell32.dll,-22912`

<span data-ttu-id="ee01a-128">Ein falscher Registrierungs Wert ist:</span><span class="sxs-lookup"><span data-stu-id="ee01a-128">An incorrect registry value is:</span></span>

`shell32.dll, -22912`

<span data-ttu-id="ee01a-129">Ein Beispiel aus Windows Vista ist der Registrierungs Wert mit den folgenden Daten:</span><span class="sxs-lookup"><span data-stu-id="ee01a-129">An example from Windows Vista is the registry value with the following data:</span></span>

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a><span data-ttu-id="ee01a-130">Erstellen von Ressourcen für Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="ee01a-130">Create Resources for Shortcut Strings</span></span>

<span data-ttu-id="ee01a-131">Wenn die MUI-Anwendung den Namen in der shellbenutzerschnittstelle anzeigt, wird für das Anwendungssymbol eine infotip-Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-131">When the MUI application displays its name in the shell user interface, an InfoTip string is displayed for the application icon.</span></span> <span data-ttu-id="ee01a-132">Sie sollten Zeichen folgen Ressourcen für den anzeigen amen der Anwendung und die zugehörige infotip-Zeichenfolge für jede unterstützte Sprache erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-132">You should create string resources for your application display name and associated InfoTip string for each supported language.</span></span> <span data-ttu-id="ee01a-133">Wenn die Ressourcen bereit sind, kann Ihre Anwendung die Zeichen folgen verwenden, wie im Abschnitt Verwenden der Shell-API zum Laden von Verknüpfungs Zeichenfolgen aus dem Registrierungs Abschnitt untersuchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee01a-133">When the resources are ready, your application can use the strings as described in the Use Shell API to Load Shortcut Strings from the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a><span data-ttu-id="ee01a-134">Vorbereiten von Ressourcen für eine Verknüpfung, die mit Windows Installer erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="ee01a-134">Prepare Resources for a Shortcut Created with Windows Installer</span></span>

<span data-ttu-id="ee01a-135">Wenn Sie Windows Installer (MSI) verwenden, um eine Verknüpfung zu erstellen, enthalten Zeichen folgen Ressourcen den anzeigen Amen und die Beschreibung der Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="ee01a-135">If you use Windows Installer (MSI) to create a shortcut, string resources include shortcut display name and description.</span></span> <span data-ttu-id="ee01a-136">In der [MSI](../msi/shortcut-table.md)-Verknüpfungs Tabelle wird auf die Ressourcen-DLL in den entsprechenden Spalten verwiesen, und die Ressourcen Bezeichner für den Kontext anzeigen Amen und die Beschreibung werden in den entsprechenden Spalten des Ressourcen Bezeichners verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee01a-136">In the [MSI shortcut table](../msi/shortcut-table.md), the resource DLL is referenced in the appropriate columns and the resource identifiers for your shortcut display name and description are used in the corresponding resource identifier columns.</span></span>

<span data-ttu-id="ee01a-137">Damit die Anwendungs Verknüpfung ordnungsgemäß mit der MUI-Ressourcen Technologie funktioniert, sollten Sie die folgenden Punkte beachten, wenn Sie die Verknüpfungs Zeichenfolgen vorbereiten:</span><span class="sxs-lookup"><span data-stu-id="ee01a-137">So that the application shortcut works properly with MUI resource technology, keep the following points in mind when preparing the shortcut strings:</span></span>

-   <span data-ttu-id="ee01a-138">Verwenden Sie entweder Umgebungsvariablen oder einen relativen Pfad, um die dll zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="ee01a-138">Use either environment variables or a relative path to register the DLL.</span></span> <span data-ttu-id="ee01a-139">Sie können @% SystemRoot% System32shell32.dll angeben, solange \\ \\ der Registrierungs Zeichenfolgentyp "reg \_ Expand SZ" lautet \_ .</span><span class="sxs-lookup"><span data-stu-id="ee01a-139">You can specify @%systemroot%\\system32\\shell32.dll as long as the registry string type is REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="ee01a-140">Der Zeichen folgen Ressourcen Bezeichner für "Text Document" in Shell32.dll ist 12345.</span><span class="sxs-lookup"><span data-stu-id="ee01a-140">The string resource identifier for "Text Document" in Shell32.dll is 12345.</span></span>
-   <span data-ttu-id="ee01a-141">Verwenden Sie keine Leerzeichen um die Symbole "," und "-".</span><span class="sxs-lookup"><span data-stu-id="ee01a-141">Do not use spaces around the "," and "-" symbols.</span></span> <span data-ttu-id="ee01a-142">Ein richtiges Beispiel ist "shell32.dll,-22912".</span><span class="sxs-lookup"><span data-stu-id="ee01a-142">A correct example is "shell32.dll,-22912".</span></span>
-   <span data-ttu-id="ee01a-143">Verwenden Sie keinen kurzen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-143">Do not use a short file name.</span></span> <span data-ttu-id="ee01a-144">Diese Art von Name funktioniert nicht mit dem Ressourcen Lade Modul.</span><span class="sxs-lookup"><span data-stu-id="ee01a-144">This type of name does not work with the resource loader.</span></span>

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a><span data-ttu-id="ee01a-145">Vorbereiten von Ressourcen für eine Verknüpfung mit dem INF-Format</span><span class="sxs-lookup"><span data-stu-id="ee01a-145">Prepare Resources for a Shortcut Using INF Format</span></span>

<span data-ttu-id="ee01a-146">Wenn Sie das INF-Dateiformat verwenden, um Verknüpfungs Zeichenfolgen zu erstellen, sollte die Ressourcen Datei die folgenden Registrierungs Einstellungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-146">If you use the INF file format to create shortcut strings, the resource file should make the following registry settings.</span></span> <span data-ttu-id="ee01a-147">Bei diesen Anweisungen wird davon ausgegangen, dass die profileitems-Syntax der Setup-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee01a-147">These instructions assume the use of the ProfileItems syntax of Setup API.</span></span>

1.  <span data-ttu-id="ee01a-148">Ändern Sie den infotip-Wert, um auf den Verweis auf die Zeichen folgen Umleitung mit dem Pfad und dem Ressourcen Bezeichner zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-148">Change the InfoTip value to point to the string redirection reference, using the path and resource identifier.</span></span>
2.  <span data-ttu-id="ee01a-149">Fügen Sie den neuen Wert displayresource unter den Profilen für die profileitems-Installation hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee01a-149">Add the new value DisplayResource under the ProfileItems installation sections.</span></span>

<span data-ttu-id="ee01a-150">Im folgenden Beispiel wird gezeigt, wie die Rechner Anwendung zum **Startmenü** hinzugefügt wird:</span><span class="sxs-lookup"><span data-stu-id="ee01a-150">The following is an example showing the addition of the Calculator application to the **Start** menu:</span></span>


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



<span data-ttu-id="ee01a-151">Verwenden Sie die unten gezeigte Syntax, wenn Sie mit INF dem **Startmenü** Elemente hinzufügen, z. b. einen Zugriffs Gruppenordner.</span><span class="sxs-lookup"><span data-stu-id="ee01a-151">Use the syntax shown below when using INF to add items, for example, an Access Group folder, to the **Start** menu.</span></span> <span data-ttu-id="ee01a-152">Diese Syntax setzt voraus, dass die \[ Unterstützung von "startmenuitems" \] von Setup verwendet wird, ähnlich der Syntax in "syssetup. inf".</span><span class="sxs-lookup"><span data-stu-id="ee01a-152">This syntax assumes the use of \[StartMenuItems\] support from Setup, similar to the syntax used in Syssetup.inf.</span></span>


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



<span data-ttu-id="ee01a-153">Legen Sie den Wert *Infotipp* auf den Zeichen folgen Verweis " `@<path>,-resID` " fest.</span><span class="sxs-lookup"><span data-stu-id="ee01a-153">Set the value *infotip* to the string reference "`@<path>,-resID`".</span></span>

<span data-ttu-id="ee01a-154">Der Anzeige Name wird durch die Werte " *ResDll* " und " *RESID* " bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-154">The display name is determined by the *resDLL* and *resID* values.</span></span> <span data-ttu-id="ee01a-155">Der Wert *RESID* gibt den Ressourcen Bezeichner für eine Zeichen folgen Ressource an, die der sprach neutralen Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee01a-155">The *resID* value specifies the resource identifier for a string resource associated with the language-neutral file.</span></span> <span data-ttu-id="ee01a-156">Der *ResDll* -Wert gibt den Pfad zu der sprach neutralen Datei an.</span><span class="sxs-lookup"><span data-stu-id="ee01a-156">The *resDLL* value specifies the path to the language-neutral file.</span></span>

## <a name="create-resources-for-friendly-document-type-names"></a><span data-ttu-id="ee01a-157">Erstellen von Ressourcen für benutzerfreundliche Dokumenttyp Namen</span><span class="sxs-lookup"><span data-stu-id="ee01a-157">Create Resources for Friendly Document Type Names</span></span>

<span data-ttu-id="ee01a-158">Sie müssen Anzeige Name-und infotip-Zeichen folgen für die Anwendung als Zeichen folgen Ressourcen implementieren.</span><span class="sxs-lookup"><span data-stu-id="ee01a-158">You must implement friendly name and InfoTip strings for your application as string resources.</span></span> <span data-ttu-id="ee01a-159">Damit benutzerfreundliche Dokumenttyp Namen auf die Sprache der Benutzeroberfläche reagieren können, muss die Anwendung die Namen mit dem Wert friendlytyid unter dem Programm Bezeichner-Schlüssel für den Dateityp registrieren.</span><span class="sxs-lookup"><span data-stu-id="ee01a-159">To allow friendly document type names to react to the user interface language, the application must register the names using the FriendlyTypeName value under the program identifier key for the file type.</span></span> <span data-ttu-id="ee01a-160">Der Standardwert für den programmbezeichnerschlüssel sollte beibehalten werden, um die Abwärtskompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="ee01a-160">The default value for the program identifier key should be retained to keep backward compatibility.</span></span> <span data-ttu-id="ee01a-161">Weitere Informationen über den Zugriff auf die Namen Ihrer Anwendung finden Sie in den Typnamen der Abfrage freundlichen Dokumente im Registrierungs Abschnitt der [Suche nach umgeleiteten](locating-redirected-strings.md)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-161">For information about accessing the names from your application, see the Query Friendly Document Type Names in the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="ee01a-162">Die jeweilige Aufgabe umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="ee01a-162">The specific work involves the following steps:</span></span>

1.  <span data-ttu-id="ee01a-163">Implementieren Sie den anzeigen Amen und die infotip-Zeichen folgen als sprachspezifische Zeichen folgen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-163">Implement the friendly name and InfoTip strings as language-specific string resources.</span></span>
2.  <span data-ttu-id="ee01a-164">Fügen Sie den Wert friendlytyadapame unter dem Dokumenttyp-Registrierungsschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee01a-164">Add the FriendlyTypeName value under the document type registry key.</span></span> <span data-ttu-id="ee01a-165">Die Daten für den Wert entsprechen dem Muster " `@<path>,-<resID>` ", wobei " *path* " angibt, dass die ausführbare Datei und die *RESID* der Ressourcen Bezeichner einer lokalisierbaren Zeichen folgen Ressource sind, die dieser ausführbaren Datei</span><span class="sxs-lookup"><span data-stu-id="ee01a-165">The data for the value follows the pattern "`@<path>,-<resID>`", where *path* indicates the executable and *resID* is the resource identifier of a localizable string resource associated with that executable.</span></span>
3.  <span data-ttu-id="ee01a-166">Geben Sie den infotip-Registrierungs Wert gemäß dem Format " `@<path>,-<resID>` " an.</span><span class="sxs-lookup"><span data-stu-id="ee01a-166">Specify the InfoTip registry value according to the format "`@<path>,-<resID>`".</span></span>

<span data-ttu-id="ee01a-167">Das folgende Beispiel zeigt die Registrierungs Einstellungen für eine txt-Datei:</span><span class="sxs-lookup"><span data-stu-id="ee01a-167">The following example shows the registry settings for a .txt file:</span></span>


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a><span data-ttu-id="ee01a-168">Bereitstellen von Ressourcen für shellverb-Aktions Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="ee01a-168">Provide Resources for Shell Verb Action Strings</span></span>

<span data-ttu-id="ee01a-169">Aktions Zeichenfolgen für bestimmte Verben (z. b. "Öffnen" und "Bearbeiten") werden im Popup Menü angezeigt, wenn der Benutzer mit der rechten Maustaste auf eine Datei in Windows-Explorer klickt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-169">Action strings for certain verbs, for example, "open" and "edit", are shown in the pop-up menu displayed when the user right-clicks a file in Windows Explorer.</span></span> <span data-ttu-id="ee01a-170">Die Anwendung muss keine Zeichen folgen für gängige Shellverben angeben, da die Shell über eigene MUI-aktivierte Standardwerte für diese Verben verfügt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-170">Your application does not have to specify strings for common shell verbs, as the shell has its own MUI-enabled defaults for these verbs.</span></span> <span data-ttu-id="ee01a-171">Sie sollten jedoch lokalisierbare Zeichen folgen Ressourcen für Zeichen folgen bereitstellen, die ungewöhnliche Verben darstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-171">However, you should provide localizable string resources for strings representing uncommon verbs.</span></span>

<span data-ttu-id="ee01a-172">Unter den Betriebssystemen vor Windows XP werden Zeichen folgen für Shellverben in der Registrierung mit der folgenden Syntax gerendert, wobei *Verb* den tatsächlichen Verb Namen angibt:</span><span class="sxs-lookup"><span data-stu-id="ee01a-172">On pre-Windows XP operating systems, strings for shell verbs in the registry are rendered using the following syntax, where *verb* specifies the actual verb name:</span></span>


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



<span data-ttu-id="ee01a-173">Hier sehen Sie ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ee01a-173">Here's an example:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



<span data-ttu-id="ee01a-174">Unter Windows XP und höher können Sie eine dereferenzierungsstufe verwenden, um eine Aktions Zeichenfolge von der Benutzeroberflächen Sprache abhängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-174">On Windows XP and later, you can use a level of indirection to make an action string depend on user interface language.</span></span> <span data-ttu-id="ee01a-175">Diese Betriebssysteme unterstützen einen MUIVerb-Wert für die Definition einer MUI-kompatiblen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ee01a-175">These operating systems support a MUIVerb value for definition of a MUI-compatible string.</span></span> <span data-ttu-id="ee01a-176">Im folgenden finden Sie ein Beispiel für einen Registrierungs Eintrag für ein ungewöhnliches Verb:</span><span class="sxs-lookup"><span data-stu-id="ee01a-176">Here's an example of a registry entry for an uncommon verb:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



<span data-ttu-id="ee01a-177">Ihre MUI-Anwendung sollte außerdem in der Lage sein, den alten Standardwert als lokalisierbare Zeichenfolge zu registrieren, wie unten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ee01a-177">Your MUI application should also be able to register the old default value as a localizable string, as shown below:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> <span data-ttu-id="ee01a-178">Die Registrierung des alten Standardwerts wird nicht empfohlen, da für Windows XP und höher unter Windows XP und höher eine andere Einrichtung als bei älteren Betriebssystemen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ee01a-178">Registration of the old default value is not recommended because it requires a different setup on Windows XP and later from the setup used on earlier operating systems.</span></span>

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a><span data-ttu-id="ee01a-179">Erstellen von Ressourcen für die Zeichen folgen Verb, Protocol und auxusertype</span><span class="sxs-lookup"><span data-stu-id="ee01a-179">Create Resources for Verb, Protocol, and AuxUserType Strings</span></span>

<span data-ttu-id="ee01a-180">Sie sollten lokalisierbare Zeichen folgen Ressourcen für Verb-, Protokoll-und auxusertype-Zeichen folgen erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-180">You should create localizable string resources for Verb, Protocol, and AuxUserType strings.</span></span> <span data-ttu-id="ee01a-181">Verwenden Sie die folgenden Registrierungs Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="ee01a-181">Use the following registry settings:</span></span>


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



<span data-ttu-id="ee01a-182">Der für LocalizedString angegebene Wert enthält oder ersetzt den Wert für *Ihr Verb*, nicht die zwei Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="ee01a-182">The value specified for LocalizedString only contains or replaces the value for *Your Verb*, not the two flag values.</span></span>

<span data-ttu-id="ee01a-183">Hier finden Sie eine Zusammenfassung, die Ihnen hilft, die richtigen Registrierungs Einstellungen sicherzustellen:</span><span class="sxs-lookup"><span data-stu-id="ee01a-183">Here is a summary to help you ensure correct registry settings:</span></span>

-   <span data-ttu-id="ee01a-184">Wenn CLSID über einen \\ eininsertable-Schlüssel der HKCR CLSID \\ {CLSID} verfügt \\ , definieren Sie den CLSID-Standardwert mithilfe von HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="ee01a-184">If CLSID has a HKCR\\CLSID\\{clsid}\\Insertable key, define the default CLSID value using HKCR\\CLSID\\{clsid}\\LocalizedString.</span></span>
-   <span data-ttu-id="ee01a-185">Wenn CLSID mindestens einen Unterschlüssel unter HKCR \\ CLSID \\ {CLSID} Verb aufweist \\ , definieren Sie jede einzelne Verb Zeichenfolge mithilfe von HKCR \\ CLSID \\ {CLSID} \\ Verb \\ xxx \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="ee01a-185">If CLSID has one or more subkeys under HKCR\\CLSID\\{clsid}\\Verb, define each individual Verb string using HKCR\\CLSID\\{clsid}\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="ee01a-186">Wenn die CLSID mindestens einen Unterschlüssel unter dem HKCR \\ {ProgID} \\ Protocol \\ stdfilebearbeitungs- \\ Verb aufweist, definieren Sie jede einzelne Verb Zeichenfolge mit dem HKCR \\ {ProgID} \\ Protocol \\ stdfilebearbeitungs \\ Verb \\ xxx \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="ee01a-186">If CLSID has one or more subkeys under HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb, define each individual Verb string using HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="ee01a-187">Wenn die CLSID mindestens einen aufgelisteten "auxusertype"-Unterschlüssel unter "HKCR \\ CLSID \\ {CLSID}" ist \\ , definieren Sie jeden "auxusertype"-Eintrag mit "HKCR \\ CLSID \\ {CLSID}" ( \\ \\ \\ LocalizedString).</span><span class="sxs-lookup"><span data-stu-id="ee01a-187">If CLSID has one or more listed AuxUserType subkeys under HKCR\\CLSID\\{clsid}\\AuxUserType, define each AuxUserType entry using HKCR\\CLSID\\{clsid}\\AuxUserType\\xxx\\LocalizedString.</span></span>

## <a name="create-a-resource-for-the-uninstall-program"></a><span data-ttu-id="ee01a-188">Erstellen einer Ressource für das Deinstallationsprogramm</span><span class="sxs-lookup"><span data-stu-id="ee01a-188">Create a Resource for the Uninstall Program</span></span>

<span data-ttu-id="ee01a-189">Um das Deinstallationsprogramm für die Anwendung zu registrieren, können Sie Registrierungs Werte im eindeutigen bezeichnerunter Schlüssel für die Anwendung unter dem Registrierungsschlüssel HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-189">To register the uninstall program for the application, you can create registry values in the unique identifier subkey for the application under the registry key HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall.</span></span> <span data-ttu-id="ee01a-190">Zu den festzulegenden Werten gehören: Display Name, Display Version, Publisher, ProductID, RegOwner, RegCompany, urlinfoabout, helptelefon, HelpLink, INSTALLLOCATION, InstallSource, InstallDate, Contact, comments, DisplayIcon, Info, urlupdateinfo.</span><span class="sxs-lookup"><span data-stu-id="ee01a-190">Values to set include: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span></span>

> [!Note]  
> <span data-ttu-id="ee01a-191">Um die MUI-Technologie für jeden Wert zu aktivieren, können Sie " \_ lokalisiert" an den Wertnamen anhängen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-191">To enable MUI technology for each value, you can append "\_Localized" to the value name.</span></span>

 

<span data-ttu-id="ee01a-192">Betriebssystemkomponenten müssen einen Wert für Display Name bereitstellen, \_ der auf eine MUI-spezifische Weise lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee01a-192">Operating system components are required to provide a value for DisplayName\_Localized in a MUI-specific way.</span></span> <span data-ttu-id="ee01a-193">Sie sollten den anzeigen Amen in einer DLL (z. b. Res.dll) als Zeichen folgen Ressource platzieren, vorausgesetzt, dass der Bezeichner 1245 lautet.</span><span class="sxs-lookup"><span data-stu-id="ee01a-193">You should place the display name in a DLL, such as Res.dll, as a string resource, assuming the identifier to be 1245.</span></span> <span data-ttu-id="ee01a-194">Anschließend kann die Anwendung den anzeigen Amen als Display Name registrieren \_ , der mit dem Wert "@ \\res.DLL,-1245" lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee01a-194">Then the application can register the display name as DisplayName\_Localized with value "@\\res.DLL,-1245".</span></span> <span data-ttu-id="ee01a-195">Alle anderen Registrierungs Einstellungen sollten unverändert beibehalten werden, einschließlich des ursprünglichen Werts für Display Name.</span><span class="sxs-lookup"><span data-stu-id="ee01a-195">All the other registry settings should be retained as they are, including the original value for DisplayName.</span></span>

## <a name="create-resources-for-sound-events"></a><span data-ttu-id="ee01a-196">Erstellen von Ressourcen für Sound Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ee01a-196">Create Resources for Sound Events</span></span>

<span data-ttu-id="ee01a-197">In Windows werden bestimmte Ereignisse mit Audiodateien verknüpft, z. b. ein neues e-Mail-Benachrichtigungs Ereignis oder ein kritischer Akku Alarm Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ee01a-197">Windows associates certain events with sound files, for example, a New Mail Notification event or a Critical Battery Alarm event.</span></span> <span data-ttu-id="ee01a-198">Die Ereignis Namen müssen von der Benutzeroberfläche angezeigt werden und müssen die Globalisierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-198">The event names must be displayed by the user interface and must support globalization.</span></span> <span data-ttu-id="ee01a-199">Daher sollten Sie eine lokalisierbare Zeichen folgen Ressource für die Beschreibung der einzelnen Ereignis Beschreibungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="ee01a-199">Therefore, you should implement a localizable string resource for the description of each event description.</span></span> <span data-ttu-id="ee01a-200">Fügen Sie zusätzlich zu dem hart codierten Standardwert einen neuen Registrierungs Wert für jeden Ereignis Namen hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee01a-200">Add a new registry value for each event name, in addition to the hard-coded default value.</span></span>

<span data-ttu-id="ee01a-201">Gehen Sie folgendermaßen vor, um ein Sound Ereignis zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="ee01a-201">Do the following to enable a sound event:</span></span>

1.  <span data-ttu-id="ee01a-202">Implementieren Sie die Beschreibung als lokalisierbare Zeichen folgen Ressource.</span><span class="sxs-lookup"><span data-stu-id="ee01a-202">Implement the description as a localizable string resource.</span></span>
2.  <span data-ttu-id="ee01a-203">Fügen Sie neben dem hart codierten Standardwert einen neuen Registrierungs Wert für den anzeigen Amen hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee01a-203">Add a new registry value for the display name, in addition to the hard-coded default value.</span></span> <span data-ttu-id="ee01a-204">Das zugehörige Registrierungs Layout wird unten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ee01a-204">The associated registry layout is shown below:</span></span>


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



<span data-ttu-id="ee01a-205">Wenn die Shell den Wert von "dispfilename" nicht finden oder abrufen kann, wird die Standardbeschreibung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee01a-205">If the shell cannot find or retrieve the value of DispFileName, it uses the default description.</span></span>

## <a name="create-resources-for-keyboard-layout-strings"></a><span data-ttu-id="ee01a-206">Erstellen von Ressourcen für Tastatur Layout-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="ee01a-206">Create Resources for Keyboard Layout Strings</span></span>

<span data-ttu-id="ee01a-207">Wenn Ihre Anwendung ein Tastaturlayout implementiert, erfordert Sie eine lokalisierbare Zeichen folgen Ressource für den Namen des Layouts für die Bildschirm Anzeige, z. b. in Listen mit Tastaturlayouts.</span><span class="sxs-lookup"><span data-stu-id="ee01a-207">If your application implements a keyboard layout, it requires a localizable string resource for the name of the layout for screen display, for example, in lists of keyboard layouts.</span></span> <span data-ttu-id="ee01a-208">Jedes Tastaturlayout verfügt über einen Registrierungsschlüssel unter HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Tastatur Layouts.</span><span class="sxs-lookup"><span data-stu-id="ee01a-208">Each keyboard layout has a registry key under HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Keyboard Layouts.</span></span>

<span data-ttu-id="ee01a-209">Zu den Werten für diesen Schlüssel gehören Layouttext, ein lesbarer Name für die Abwärtskompatibilität und layoutanzeigename.</span><span class="sxs-lookup"><span data-stu-id="ee01a-209">Among the values for that key are Layout Text, a human-readable name for backward compatibility, and Layout Display Name.</span></span> <span data-ttu-id="ee01a-210">Die für den layoutanzeigenamen angegebenen Daten sollten ein Zeichen folgen Verweis im Format " `@<path>,-resID` " sein, der auf eine lokalisierbare Zeichen folgen Ressource verweist, die dem Tastatur Layout zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee01a-210">The data supplied for Layout Display Name should be a string reference of the form "`@<path>,-resID`", referring to a localizable string resource associated with the keyboard layout.</span></span>

<span data-ttu-id="ee01a-211">Im folgenden finden Sie ein Beispiel für eine Registrierungs Einstellung für das Spanisch (Spanien)-Tastaturlayout:</span><span class="sxs-lookup"><span data-stu-id="ee01a-211">Here is an example of a registry setting for the Spanish (Spain) keyboard layout:</span></span>

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a><span data-ttu-id="ee01a-212">Darstellung der allgemeinen Dialog Felder für OLE-Einfügevorgänge</span><span class="sxs-lookup"><span data-stu-id="ee01a-212">Represent OLE Insert Object Common Dialog Strings</span></span>

<span data-ttu-id="ee01a-213">Sie können den anzeigen Amen eines OLE-einfügbar-Objekts als lokalisierbare Zeichen folgen Ressource implementieren, die dem Code zugeordnet ist, der das Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="ee01a-213">You can implement the display name of an OLE insertable object as a localizable string resource associated with the code implementing that object.</span></span> <span data-ttu-id="ee01a-214">Das [OLE-Dialogfeld "Objekt einfügen](/cpp/mfc/reference/coleinsertdialog-class) " erhält einen anzeigen Amen aus dem Registrierungsschlüssel HKCR \\ CLSID \\ { *<GUID>* }, wobei *GUID* den Klassen Bezeichner eines einfügbar OLE-Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ee01a-214">The [OLE Insert Object dialog box](/cpp/mfc/reference/coleinsertdialog-class) gets a display name from the registry key HKCR\\CLSID\\{*<GUID>*}, where *GUID* identifies the class identifier of an insertable OLE object.</span></span> <span data-ttu-id="ee01a-215">Windows Vista und höher implementieren diesen Objekttyp auf lokalisierbare Weise. dabei wird ein MUI-kompatibler Anzeige Name verwendet, der die Anpassung an die Benutzeroberflächen Sprache ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ee01a-215">Windows Vista and later implement this type of object in a localizable way, using a MUI-compliant display name that allows customization to the user interface language.</span></span> <span data-ttu-id="ee01a-216">Im Gegensatz dazu implementieren Pre-Windows Vista-Betriebssysteme den anzeigen Amen für diesen Objekttyp mit dem Standardwert des entsprechenden Registrierungsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="ee01a-216">In contrast, pre-Windows Vista operating systems implement the display name for this type of object using the default value of the corresponding registry key.</span></span> <span data-ttu-id="ee01a-217">In der Regel ist dieser Name entweder ein englischer Name (USA) oder ein Name in der Standardbenutzer Oberflächen Sprache des Systems.</span><span class="sxs-lookup"><span data-stu-id="ee01a-217">Typically this name is either an English (United States) name or a name in the system default UI language.</span></span>

> [!Note]  
> <span data-ttu-id="ee01a-218">Nicht alle Objekte, die den unter Schlüsseln des Registrierungsschlüssels entsprechen, sind Insertable.</span><span class="sxs-lookup"><span data-stu-id="ee01a-218">Not all objects that correspond to subkeys of the registry key are insertable.</span></span>

 

<span data-ttu-id="ee01a-219">Der Standardwert des Schlüssels "HKCR \\ CLSID \\ { *<GUID>* }" sollte einen lesbaren Namen aus Gründen der Abwärtskompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ee01a-219">The default value of the HKCR\\CLSID\\{*<GUID>*} key should retain a human-readable name for backward compatibility.</span></span> <span data-ttu-id="ee01a-220">Er sollte jedoch auch den Wert von LocalizedString im Format " `@<path>,-ResID` " definieren, wobei Path die ausführbare Datei identifiziert, die das Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="ee01a-220">However, it should also define the LocalizedString value, in the format "`@<path>,-ResID`", where path identifies the executable file implementing the object.</span></span> <span data-ttu-id="ee01a-221">Der Wert Resid gibt den Ressourcen Bezeichner der lokalisierbaren Zeichenfolge für den anzeigen Amen an.</span><span class="sxs-lookup"><span data-stu-id="ee01a-221">The ResID value specifies the resource identifier of the localizable string for the display name.</span></span>

<span data-ttu-id="ee01a-222">Das Registrierungs Skript für das einfügbar Media Clip-Objekt enthält z. b. die folgenden Zeilen:</span><span class="sxs-lookup"><span data-stu-id="ee01a-222">For example, the registration script for the insertable Media Clip object includes the following lines:</span></span>


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



<span data-ttu-id="ee01a-223">Die erste Zeile bietet Abwärtskompatibilität, indem eine einfache Text Zeichenfolge in der Registrierung als Standard Anzeige Name platziert wird.</span><span class="sxs-lookup"><span data-stu-id="ee01a-223">The first line provides backward compatibility by placing a simple text string in the registry as a default display name.</span></span> <span data-ttu-id="ee01a-224">Die zweite Zeile ermöglicht den Zugriff auf den MUI-kompatiblen anzeigen Amen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-224">The second line provides access to the MUI-compliant display name.</span></span> <span data-ttu-id="ee01a-225">Gibt den Zeichen folgen Bezeichner an, der in Mplay32.exe gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ee01a-225">It indicates the string identifier stored in Mplay32.exe.</span></span> <span data-ttu-id="ee01a-226">Die Zeichenfolge mit dem Bezeichner 9217 in Mplay32.exe kann den Zeichen folgen Ressourcen Werten für eine beliebige Anzahl von Sprachen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ee01a-226">The string with identifier 9217 in Mplay32.exe can be associated with string resource values for any number of languages.</span></span> <span data-ttu-id="ee01a-227">Der englische Name (USA) ist "Media Clip".</span><span class="sxs-lookup"><span data-stu-id="ee01a-227">Its English (United States) name is "Media Clip".</span></span>

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a><span data-ttu-id="ee01a-228">Erstellen von Zeichen folgen Ressourcen für die Microsoft Management Console Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="ee01a-228">Create String Resources for Microsoft Management Console Snap-Ins</span></span>

<span data-ttu-id="ee01a-229">Sie sollten für jedes MMC-Snap-in (Microsoft Management Console), das von ihrer MUI-Anwendung verwendet wird, eine lokalisierbare Zeichen folgen Ressource erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-229">You should create a localizable string resource for each Microsoft Management Console (MMC) snap-in used by your MUI application.</span></span> <span data-ttu-id="ee01a-230">Da ein Snap-in Teil einer Konsole ist, verfügt es über eine Benutzeroberfläche und muss globalisiert werden, um in mehreren Sprachen arbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="ee01a-230">Because a snap-in is part of a console, it has a user interface and must be globalized to operate in more than one language.</span></span>

<span data-ttu-id="ee01a-231">Zum größten Teil haben MMC-Snap-Ins dieselben Globalisierungs-und Lokalisierungs Probleme wie die MUI-Anwendung selbst.</span><span class="sxs-lookup"><span data-stu-id="ee01a-231">For the most part, MMC snap-ins raise the same globalization and localization issues as the MUI application itself.</span></span> <span data-ttu-id="ee01a-232">Ein MMC-Snap-in muss seinen Namen in der Registrierung für die Anzeige widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="ee01a-232">An MMC snap-in must reflect its name in the registry for display.</span></span> <span data-ttu-id="ee01a-233">Der Registrierungs Eintrag sollte sowohl einen indirekten Verweis auf eine lokalisierbare Zeichen folgen Ressource als auch eine Literalzeichenfolge für die Abwärtskompatibilität enthalten.</span><span class="sxs-lookup"><span data-stu-id="ee01a-233">The registry entry should include both an indirect reference to a localizable string resource and a literal string for backward compatibility.</span></span>

<span data-ttu-id="ee01a-234">Jedes MMC-Snap-in verfügt über einen Registrierungsschlüssel unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ MMC \\ SnapIns.</span><span class="sxs-lookup"><span data-stu-id="ee01a-234">Each MMC snap-in has a registry key under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MMC\\SnapIns.</span></span> <span data-ttu-id="ee01a-235">Zu den Werten für diesen Schlüssel gehören namestring, ein lesbarer Name für die Abwärtskompatibilität und NameStringIndirect, der einen indirekten Verweis auf eine lokalisierbare Zeichen folgen Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-235">Among the values for that key are NameString, specifying a human-readable name for backward compatibility, and NameStringIndirect, specifying an indirect reference to a localizable string resource.</span></span> <span data-ttu-id="ee01a-236">Für NameStringIndirect sollten Sie einen Zeichen folgen Verweis im Format "" bereitstellen `@<path>,-resID` , das eine lokalisierbare Zeichen folgen Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee01a-236">For NameStringIndirect, you should provide a string reference of the form "`@<path>,-resID`", representing a localizable string resource.</span></span>

<span data-ttu-id="ee01a-237">Beispielsweise können Sie die folgende Einstellung für Mymmc.dll festlegen, wobei 12345 der Bezeichner der entsprechenden Zeichen folgen Ressource mit dem lokalisierbaren Namen des Snap-Ins ist:</span><span class="sxs-lookup"><span data-stu-id="ee01a-237">For example, you might make the following setting for Mymmc.dll, where 12345 is the identifier of the corresponding string resource containing the localizable name of the snap-in:</span></span>


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



<span data-ttu-id="ee01a-238">Einige Snap-Ins registrieren andere Registrierungszeichen folgen Werte, die von MMC nicht aus der Registrierung gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="ee01a-238">Some snap-ins register other registry string values that MMC does not read from the registry.</span></span> <span data-ttu-id="ee01a-239">Weitere Informationen zur Verwendung dieser Werte finden Sie unter Registrieren von Microsoft Management Console Snap-In Zeichen folgen, die nicht aus der Registrierung gelesen wurden, beim Suchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-239">For more information about using these values, see Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

## <a name="create-string-resources-for-a-windows-service"></a><span data-ttu-id="ee01a-240">Erstellen von Zeichen folgen Ressourcen für einen Windows-Dienst</span><span class="sxs-lookup"><span data-stu-id="ee01a-240">Create String Resources for a Windows Service</span></span>

<span data-ttu-id="ee01a-241">Obwohl ein Windows-Dienst in der Regel nur wenige oder keine Benutzeroberfläche besitzt, muss er einen MUI-kompatiblen Namen anzeigen und in der Regel eine MUI-kompatible sprachspezifische Beschreibung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ee01a-241">Although a Windows service typically has little or no user interface, it must display a MUI-compliant name and usually provides a MUI-compliant language-specific description.</span></span> <span data-ttu-id="ee01a-242">Der Registrierungsschlüssel, der einen Windows-Dienst beschreibt, unterstützt nur den Display Name-Wert für den Dienstnamen und den Beschreibungs Wert für die Dienst Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="ee01a-242">The registry key that describes a Windows service supports only the DisplayName value for the service name and the Description value for the service description.</span></span>

<span data-ttu-id="ee01a-243">Die Einstellungen für den Windows-Dienst werden von der Anwendung hergestellt, wie unter Festlegen des anzeigen Amens und der Beschreibung für einen Windows-Dienst aus der Registrierung beim Suchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee01a-243">Settings for the Windows service are made from the application, as described in Set the Display Name and Description for a Windows Service from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span> <span data-ttu-id="ee01a-244">Wenn Ihre Anwendung die Registrierungs Werte für die Dienst Benutzeroberfläche nicht festgelegt hat, bleiben die Werte in der Registrierung auf Englisch festgelegt, auch wenn die Benutzeroberfläche in einer anderen Sprache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ee01a-244">If your application does not set the registry values for the service user interface, values in the registry remain set to English, even if the user interface is in another language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee01a-245">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee01a-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee01a-246">Vorbereiten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ee01a-246">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="ee01a-247">Suchen umgeleitet-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="ee01a-247">Locating Redirected Strings</span></span>](locating-redirected-strings.md)
</dt> </dl>

 

 
