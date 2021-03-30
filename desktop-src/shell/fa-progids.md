---
description: Die Shell verwendet einen ProgID-Registrierungs Unterschlüssel (programmgesteuerte Bezeichner), um einer Anwendung einen Dateityp zuzuordnen und das Verhalten der Zuordnung zu steuern.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Programmgesteuerte Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993710"
---
# <a name="programmatic-identifiers"></a><span data-ttu-id="20687-103">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="20687-103">Programmatic Identifiers</span></span>

<span data-ttu-id="20687-104">Die Shell verwendet einen ProgID-Registrierungs Unterschlüssel (programmgesteuerte Bezeichner), um einer Anwendung einen Dateityp zuzuordnen und das Verhalten der Zuordnung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="20687-104">The Shell uses a programmatic identifier (ProgID) registry subkey to associate a file type with an application, and to control the behavior of the association.</span></span> <span data-ttu-id="20687-105">Die für Dateizuordnungen verwendeten ProgID-Einträge befinden sich in der Registrierung unter **HKEY \_ Classes \_ root** .</span><span class="sxs-lookup"><span data-stu-id="20687-105">The ProgID entries used for file associations are located under **HKEY\_CLASSES\_ROOT** in the registry.</span></span>

<span data-ttu-id="20687-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="20687-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="20687-107">Von Dateizuordnungen verwendete programmatische bezeichnerelemente</span><span class="sxs-lookup"><span data-stu-id="20687-107">Programmatic Identifier Elements Used by File Associations</span></span>](#programmatic-identifier-elements-used-by-file-associations)
-   [<span data-ttu-id="20687-108">Verwenden von programmatischen bezeichlern mit Versions Angabe</span><span class="sxs-lookup"><span data-stu-id="20687-108">Using Versioned Programmatic Identifiers</span></span>](#using-versioned-programmatic-identifiers)
-   [<span data-ttu-id="20687-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20687-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="20687-110">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren eines Dateityps für eine neue Anwendung](how-to-register-a-file-type-for-a-new-application.md) .</span><span class="sxs-lookup"><span data-stu-id="20687-110">For additional information, read [How To Register a File Type for a New Application](how-to-register-a-file-type-for-a-new-application.md)</span></span>

## <a name="programmatic-identifier-elements-used-by-file-associations"></a><span data-ttu-id="20687-111">Von Dateizuordnungen verwendete programmatische bezeichnerelemente</span><span class="sxs-lookup"><span data-stu-id="20687-111">Programmatic Identifier Elements Used by File Associations</span></span>

<span data-ttu-id="20687-112">Das richtige Format eines ProgID-Schlüssel namens ist " \[ *Vendor" oder "Application*" \] . \[ *Komponente* \] . \[ *Version* \] , getrennt durch Punkte und ohne Leerzeichen, wie in Word.Doc-Nummer. 6.</span><span class="sxs-lookup"><span data-stu-id="20687-112">The proper format of a ProgID key name is \[*Vendor or Application*\].\[*Component*\].\[*Version*\], separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="20687-113">Der *Versions* Anteil ist optional, wird jedoch dringend empfohlen.</span><span class="sxs-lookup"><span data-stu-id="20687-113">The *Version* portion is optional but strongly recommended.</span></span> <span data-ttu-id="20687-114">Weitere Informationen finden Sie unter [Verwenden von programmatischen bezeichlern mit Versions](#using-versioned-programmatic-identifiers)Angabe.</span><span class="sxs-lookup"><span data-stu-id="20687-114">For more information, see [Using Versioned Programmatic Identifiers](#using-versioned-programmatic-identifiers).</span></span>

<span data-ttu-id="20687-115">Ein ProgID-Unterschlüssel sollte die folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="20687-115">A ProgID subkey should include the following elements.</span></span> <span data-ttu-id="20687-116">Beachten Sie, dass für einige Zeichen folgen Daten in diesem Schlüssel eine bestimmte Formatierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="20687-116">Note that some string data in this key requires specific formatting.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20687-117">Element</span><span class="sxs-lookup"><span data-stu-id="20687-117">Element</span></span></th>
<th><span data-ttu-id="20687-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20687-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20687-119"><strong>Vorgegebene</strong></span><span class="sxs-lookup"><span data-stu-id="20687-119"><strong>(Default)</strong></span></span></td>
<td><span data-ttu-id="20687-120">Legen Sie den Standardeintrag des ProgID-unter Schlüssels auf einen anzeigen Amen für diese ProgID fest, der für den Benutzer geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="20687-120">Set the default entry of the ProgID subkey to a friendly name for that ProgID, suitable to display to the user.</span></span> <span data-ttu-id="20687-121">Die Verwendung dieses Eintrags zum Speichern des anzeigen Amens wird durch den Eintrag friendlytykame auf Systemen mit Windows 2000 oder höher als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="20687-121">The use of this entry to hold the friendly name is deprecated by the FriendlyTypeName entry on systems running Windows 2000 or later.</span></span> <span data-ttu-id="20687-122">Sie sollten diesen Wert jedoch aus Gründen der Abwärtskompatibilität festlegen.</span><span class="sxs-lookup"><span data-stu-id="20687-122">However, you should set this value for backward compatibility.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20687-123"><strong>Allowsilentdefaultübernahme</strong> (eingeführt in Windows 8)</span><span class="sxs-lookup"><span data-stu-id="20687-123"><strong>AllowSilentDefaultTakeOver</strong> (introduced in Windows 8)</span></span></td>
<td><span data-ttu-id="20687-124">Legen Sie diesen optionalen Eintrag fest, um zu signalisieren, dass Windows diese ProgID ignorieren soll, wenn ein Standard Handler für einen öffentlichen Dateityp bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="20687-124">Set this optional entry to signal that Windows should ignore this ProgID when determining a default handler for a public file type.</span></span> <span data-ttu-id="20687-125">Unabhängig davon, ob dieser Wert festgelegt ist, wird die ProgID weiterhin im openWith-Kontextmenü und Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20687-125">Regardless of whether this value is set, the ProgID continues to appear in the OpenWith shortcut menu and dialog.</span></span> <span data-ttu-id="20687-126">Dies ist ein REG_NONE Wert.</span><span class="sxs-lookup"><span data-stu-id="20687-126">This is a REG_NONE value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20687-127"><strong>Appusermodelid</strong> (eingeführt in Windows 7)</span><span class="sxs-lookup"><span data-stu-id="20687-127"><strong>AppUserModelID</strong> (introduced in Windows 7)</span></span></td>
<td><span data-ttu-id="20687-128">Legen Sie diesen optionalen Eintrag auf die explizite Anwendungs Benutzer Modell-ID (appusermodelid) der Anwendung fest, wenn die Anwendung eine explizite appusermodelid verwendet und entweder die automatisch generierten <strong>aktuellen</strong> oder <strong>häufigen</strong> Sprung Listen des Systems verwendet oder eine benutzerdefinierte Sprung Liste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="20687-128">Set this optional entry to the application's explicit Application User Model ID (AppUserModelID) if the application uses an explicit AppUserModelID and uses either the system's automatically generated <strong>Recent</strong> or <strong>Frequent</strong> Jump Lists or provides a custom Jump List.</span></span> <span data-ttu-id="20687-129">Wenn eine Anwendung eine explizite appusermodelid verwendet und diesen Wert nicht festgelegt, werden Elemente nicht in den Sprung Listen dieser Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20687-129">If an application uses an explicit AppUserModelID and does not set this value, items will not appear in that application's Jump Lists.</span></span> <span data-ttu-id="20687-130">Dies ist eine REG_SZ Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="20687-130">This is a REG_SZ string.</span></span> <span data-ttu-id="20687-131">Weitere Informationen finden Sie unter <a href="appids.md">App-Benutzer Modell-IDs (appusermudelids)</a>.</span><span class="sxs-lookup"><span data-stu-id="20687-131">For more information, see <a href="appids.md">Application User Model IDs (AppUserModelIDs)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20687-132"><strong>EditFlags</strong></span><span class="sxs-lookup"><span data-stu-id="20687-132"><strong>EditFlags</strong></span></span></td>
<td><span data-ttu-id="20687-133">Legen Sie diesen optionalen Eintrag mithilfe von Flags aus der <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>filetypeattributeflags</strong></a> -Enumeration fest.</span><span class="sxs-lookup"><span data-stu-id="20687-133">Set this optional entry using flags from the <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> enumeration.</span></span> <span data-ttu-id="20687-134">Der EditFlags-Eintrag steuert einige Aspekte der shellverarbeitung der mit dieser ProgID verknüpften Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="20687-134">The EditFlags entry controls some aspects of the Shell's handling of the file types linked to this ProgID.</span></span> <span data-ttu-id="20687-135">Sie können auch den EditFlags-Eintrag verwenden, um einzuschränken, wie stark der Benutzer bestimmte Aspekte dieser Dateitypen mithilfe des Eigenschaften Blatts einer Datei ändern kann.</span><span class="sxs-lookup"><span data-stu-id="20687-135">You can also use the EditFlags entry to limit how much the user can modify certain aspects of these file types using a file's property sheet.</span></span> <span data-ttu-id="20687-136">Die für EditFlags verwendeten <strong>filetypeattributeflags</strong> -Werte sind binäre Werte, die so entworfen wurden, dass Sie mehrere Attribute in einem bitweisen OR-Vorgang zu einem einzelnen Wert zusammenfassen können.</span><span class="sxs-lookup"><span data-stu-id="20687-136">The <strong>FILETYPEATTRIBUTEFLAGS</strong> values used for EditFlags are binary values designed so that you can combine multiple attributes into a single value in a bitwise OR operation.</span></span> <span data-ttu-id="20687-137">Dies ist ein REG_DWORD oder REG_BINARY Wert.</span><span class="sxs-lookup"><span data-stu-id="20687-137">This is a REG_DWORD or REG_BINARY value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20687-138"><strong>Friendlytyname</strong></span><span class="sxs-lookup"><span data-stu-id="20687-138"><strong>FriendlyTypeName</strong></span></span></td>
<td><span data-ttu-id="20687-139">Legen Sie diesen Eintrag auf einen anzeigen Amen für die ProgID fest, der für den Benutzer geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="20687-139">Set this entry to a friendly name for the ProgID, suitable to display to the user.</span></span> <span data-ttu-id="20687-140">Aus Konsistenz Gründen sollte diese Zeichenfolge die gleichen Daten wie der Standardeintrag für diesen ProgID-Schlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="20687-140">For consistency, this string should contain the same data as the Default entry for this ProgID key.</span></span> <span data-ttu-id="20687-141">Dieser Eintrag kann entweder eine REG_SZ oder eine REG_EXPAND_SZ Zeichenfolge sein, muss jedoch als indirekte Zeichenfolge (ein voll qualifizierter Dateiname und Ressourcen Wert mit vorangestelltem @-Symbol) formatiert sein, z.b. <em>@% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="20687-141">This entry can be either a REG_SZ or REG_EXPAND_SZ string, but it must be formatted as an indirect string (a fully qualified file name and resource value preceded by the @ symbol), for instance <em>@%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20687-142"><strong>InfoTip</strong></span><span class="sxs-lookup"><span data-stu-id="20687-142"><strong>InfoTip</strong></span></span></td>
<td><span data-ttu-id="20687-143">Legen Sie diesen Eintrag auf eine kurze Hilfe Meldung fest, die von der Shell für diese ProgID angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="20687-143">Set this entry to a brief help message that the Shell displays for this ProgID.</span></span> <span data-ttu-id="20687-144">Der infotip-Eintrag wird in einem Mouseover-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20687-144">The InfoTip entry displays in a mouse-over dialog box.</span></span> <span data-ttu-id="20687-145">Bei diesem Wert kann es sich entweder um eine REG_SZ oder REG_EXPAND_SZ Zeichenfolge handeln, aber wie friendlytytzame, muss er als indirekte Zeichenfolge formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="20687-145">This value can be either a REG_SZ or REG_EXPAND_SZ string but, like FriendlyTypeName, it must be formatted as an indirect string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20687-146"><strong>Curver</strong></span><span class="sxs-lookup"><span data-stu-id="20687-146"><strong>CurVer</strong></span></span></td>
<td><span data-ttu-id="20687-147">Legen Sie den (Standard-) Eintrag dieses unter Schlüssels auf die aktuelle Version dieser ProgID fest.</span><span class="sxs-lookup"><span data-stu-id="20687-147">Set the (Default) entry of this subkey to the most current version of this ProgID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="20687-148">Sie sollten die Verwendung von " <strong>Cursor</strong>" vermeiden, es sei denn, Sie haben parallele Anwendungsversionen, d. h. mehrere Versionen, die auf demselben System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="20687-148">Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20687-149"><strong>DefaultIcon</strong>.</span><span class="sxs-lookup"><span data-stu-id="20687-149"><strong>DefaultIcon</strong>.</span></span></td>
<td><span data-ttu-id="20687-150">Legen Sie den (Standard-) Eintrag dieses unter Schlüssels auf das Standard Symbol fest, das für die mit dieser ProgID verknüpften Dateitypen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="20687-150">Set the (Default) entry of this subkey to the default icon that you want to display for file types associated with this ProgID.</span></span> <span data-ttu-id="20687-151">Dieser Wert kann entweder eine REG_SZ oder eine REG_EXPAND_SZ Zeichenfolge sein, muss jedoch als voll qualifizierter Dateiname mit dem zugehörigen Ressourcen Wert bereitgestellt werden, z.b. <em>% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="20687-151">This value can be either a REG_SZ or REG_EXPAND_SZ string, but it must be provided as a fully qualified file name with its attendant resource value, for instance <em>%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="20687-152">Im folgenden Beispiel für einen Registrierungsschlüssel wird ein Schlüsselknoten für die Datei Zuordnungs ProgID veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="20687-152">The following registry key example illustrates a file association ProgID key node:</span></span>

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a><span data-ttu-id="20687-153">Verwenden von programmatischen bezeichlern mit Versions Angabe</span><span class="sxs-lookup"><span data-stu-id="20687-153">Using Versioned Programmatic Identifiers</span></span>

<span data-ttu-id="20687-154">Eine mit Versions Angabe versehene ProgID ist eine, deren Version in Ihrem Namen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="20687-154">A versioned ProgID is one whose version is indicated in its name.</span></span> <span data-ttu-id="20687-155">Dies geschieht in der Regel, indem Sie dem Namen einen Zeitraum und die Versionsnummer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="20687-155">You typically do this by adding a period and the version number to the name.</span></span> <span data-ttu-id="20687-156">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="20687-156">For example:</span></span>

-   <span data-ttu-id="20687-157">Word.Doc.6</span><span class="sxs-lookup"><span data-stu-id="20687-157">Word.Document.6</span></span>
-   <span data-ttu-id="20687-158">Word.Doc.8</span><span class="sxs-lookup"><span data-stu-id="20687-158">Word.Document.8</span></span>

<span data-ttu-id="20687-159">Dabei handelt es sich um versionierte ProgIDs mit den Versionen 6 und 8.</span><span class="sxs-lookup"><span data-stu-id="20687-159">These are versioned ProgIDs, with versions 6 and 8 respectively.</span></span> <span data-ttu-id="20687-160">Wenn Sie über eine parallele Anwendung verfügen, d. h. eine, die mehrere Versionen der Anwendung gleichzeitig installiert unterstützt, verwenden Sie die von currver und Versions unabhängigen ProgIDs.</span><span class="sxs-lookup"><span data-stu-id="20687-160">If you have a side-by-side application, that is, one that supports multiple versions of your application installed at the same time, then use CurVer and Version Independent ProgIDs.</span></span> <span data-ttu-id="20687-161">Andernfalls sollten die Dienst-und Versions unabhängigen ProgIDs vermieden werden, da Sie zu Ineffizienz führen.</span><span class="sxs-lookup"><span data-stu-id="20687-161">Otherwise, CurVer and Version Independent ProgIDs should be avoided because they will lead to inefficiency.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20687-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20687-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20687-163">Registrieren eines Dateityps für eine neue Anwendung</span><span class="sxs-lookup"><span data-stu-id="20687-163">How To Register a File Type for a New Application</span></span>](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[<span data-ttu-id="20687-164">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="20687-164">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="20687-165">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="20687-165">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="20687-166">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="20687-166">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="20687-167">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="20687-167">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="20687-168">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="20687-168">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="20687-169">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="20687-169">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="20687-170">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="20687-170">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="20687-171">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="20687-171">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 




