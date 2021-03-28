---
description: 'In diesem Thema wird erläutert, wie Sie ein Programm in der Windows-Registrierung als einen der folgenden Client Typen registrieren: Browser, e-Mail, Medienwiedergabe, Instant Messaging oder virtueller Computer für Java.'
title: Registrieren von Programmen mit Client Typen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869627"
---
# <a name="registering-programs-with-client-types"></a><span data-ttu-id="b8468-103">Registrieren von Programmen mit Client Typen</span><span class="sxs-lookup"><span data-stu-id="b8468-103">Registering Programs with Client Types</span></span>

<span data-ttu-id="b8468-104">In diesem Thema wird erläutert, wie Sie ein Programm in der Windows-Registrierung als einen der folgenden Client Typen registrieren: Browser, e-Mail, Medienwiedergabe, Instant Messaging oder virtueller Computer für Java.</span><span class="sxs-lookup"><span data-stu-id="b8468-104">This topic explains how to register a program in the Windows registry as one of the following client types: browser, email, media playback, instant messaging, or virtual machine for Java.</span></span>

> [!Note]  
> <span data-ttu-id="b8468-105">Diese Informationen gelten für die folgenden Betriebssysteme:</span><span class="sxs-lookup"><span data-stu-id="b8468-105">This information applies to the following operating systems:</span></span>
> 
> -   <span data-ttu-id="b8468-106">Windows 2000 Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="b8468-106">Windows 2000 Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="b8468-107">Windows 2000 Service Pack 4 (SP4)</span><span class="sxs-lookup"><span data-stu-id="b8468-107">Windows 2000 Service Pack 4 (SP4)</span></span>
> -   <span data-ttu-id="b8468-108">Windows XP Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="b8468-108">Windows XP Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="b8468-109">Windows XP Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="b8468-109">Windows XP Service Pack 2 (SP2)</span></span>
> -   <span data-ttu-id="b8468-110">Windows XP Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="b8468-110">Windows XP Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="b8468-111">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8468-111">Windows Server 2003</span></span>
> -   <span data-ttu-id="b8468-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8468-112">Windows Vista</span></span>
> -   <span data-ttu-id="b8468-113">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="b8468-113">Windows Vista Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="b8468-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b8468-114">Windows 8</span></span>

 

<span data-ttu-id="b8468-115">Das Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b8468-115">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="b8468-116">Allgemeine Registrierungs Elemente für alle Client Typen</span><span class="sxs-lookup"><span data-stu-id="b8468-116">Common Registration Elements for All Client Types</span></span>](#common-registration-elements-for-all-client-types)
    -   [<span data-ttu-id="b8468-117">Auswählen eines kanonischen Namens</span><span class="sxs-lookup"><span data-stu-id="b8468-117">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
    -   [<span data-ttu-id="b8468-118">Registrieren des anzeigen Amens eines Programms</span><span class="sxs-lookup"><span data-stu-id="b8468-118">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
    -   [<span data-ttu-id="b8468-119">Registrieren eines Programm Symbols</span><span class="sxs-lookup"><span data-stu-id="b8468-119">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
    -   [<span data-ttu-id="b8468-120">Registrieren eines geöffneten Verbs</span><span class="sxs-lookup"><span data-stu-id="b8468-120">Registering an Open Verb</span></span>](#registering-an-open-verb)
    -   [<span data-ttu-id="b8468-121">Installationsinformationen werden registriert</span><span class="sxs-lookup"><span data-stu-id="b8468-121">Registering Installation Information</span></span>](#registering-installation-information)
-   [<span data-ttu-id="b8468-122">Registrierungs Elemente für bestimmte Client Typen</span><span class="sxs-lookup"><span data-stu-id="b8468-122">Registration Elements for Specific Client Types</span></span>](#registration-elements-for-specific-client-types)
    -   [<span data-ttu-id="b8468-123">Start Menü Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-123">Start Menu Registration</span></span>](#start-menu-registration)
    -   [<span data-ttu-id="b8468-124">Mail Client Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-124">Mail Client Registration</span></span>](#mail-client-registration)
-   [<span data-ttu-id="b8468-125">Vervollständigen von Beispiel Registrierungen</span><span class="sxs-lookup"><span data-stu-id="b8468-125">Complete Sample Registrations</span></span>](#complete-sample-registrations)
    -   [<span data-ttu-id="b8468-126">Ein Beispiel Browser</span><span class="sxs-lookup"><span data-stu-id="b8468-126">A Sample Browser</span></span>](#a-sample-browser)
    -   [<span data-ttu-id="b8468-127">Beispiel-e-Mail-Browser</span><span class="sxs-lookup"><span data-stu-id="b8468-127">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
    -   [<span data-ttu-id="b8468-128">Ein Beispiel Media Player</span><span class="sxs-lookup"><span data-stu-id="b8468-128">A Sample Media Player</span></span>](#a-sample-media-player)
    -   [<span data-ttu-id="b8468-129">Ein Instant Messenger-Beispielprogramm</span><span class="sxs-lookup"><span data-stu-id="b8468-129">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
    -   [<span data-ttu-id="b8468-130">Ein Beispiel für einen virtuellen Computer für Java</span><span class="sxs-lookup"><span data-stu-id="b8468-130">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)
-   [<span data-ttu-id="b8468-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8468-131">Related topics</span></span>](#related-topics)

<span data-ttu-id="b8468-132">Dieses Thema erweitert die vorhandene Dokumentation zum Registrieren eines Programms als bestimmten Clienttyp.</span><span class="sxs-lookup"><span data-stu-id="b8468-132">This topic extends existing documentation about registering a program as a particular client type.</span></span> <span data-ttu-id="b8468-133">Links zu dieser Dokumentation finden Sie im Abschnitt Verwandte Themen.</span><span class="sxs-lookup"><span data-stu-id="b8468-133">For links to that documentation, see the Related Topics section.</span></span>

## <a name="common-registration-elements-for-all-client-types"></a><span data-ttu-id="b8468-134">Allgemeine Registrierungs Elemente für alle Client Typen</span><span class="sxs-lookup"><span data-stu-id="b8468-134">Common Registration Elements for All Client Types</span></span>

<span data-ttu-id="b8468-135">Wenn Sie ein Programm als Clienttyp registrieren, sind die meisten Registrierungseinträge unabhängig vom Clienttyp identisch.</span><span class="sxs-lookup"><span data-stu-id="b8468-135">When registering a program as a client type, most of the registry entries are the same regardless of the client type.</span></span> <span data-ttu-id="b8468-136">Einige Registrierungseinträge sind jedoch spezifisch für den Clienttyp, und Sie sind im Abschnitt [Registrierungs Elemente für bestimmte Client Typen](#registration-elements-for-specific-client-types) vermerkt.</span><span class="sxs-lookup"><span data-stu-id="b8468-136">Some registry entries, however, are specific to the client type and these are noted in the [Registration Elements for Specific Client Types](#registration-elements-for-specific-client-types) section.</span></span>

<span data-ttu-id="b8468-137">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="b8468-137">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="b8468-138">Auswählen eines kanonischen Namens</span><span class="sxs-lookup"><span data-stu-id="b8468-138">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
-   [<span data-ttu-id="b8468-139">Registrieren des anzeigen Amens eines Programms</span><span class="sxs-lookup"><span data-stu-id="b8468-139">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
-   [<span data-ttu-id="b8468-140">Registrieren eines Programm Symbols</span><span class="sxs-lookup"><span data-stu-id="b8468-140">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
-   [<span data-ttu-id="b8468-141">Registrieren eines geöffneten Verbs</span><span class="sxs-lookup"><span data-stu-id="b8468-141">Registering an Open Verb</span></span>](#registering-an-open-verb)
-   [<span data-ttu-id="b8468-142">Installationsinformationen werden registriert</span><span class="sxs-lookup"><span data-stu-id="b8468-142">Registering Installation Information</span></span>](#registering-installation-information)

> [!Note]  
> <span data-ttu-id="b8468-143">Unterschlüssel Namen, die in diesem Thema kursiv angegeben sind, sind Platzhalter für benutzerdefinierte Unterschlüssel Namen oder einen Satz möglicher Werte.</span><span class="sxs-lookup"><span data-stu-id="b8468-143">Subkey names given in italics throughout this topic are placeholders for user-defined subkey names or a set of possible values.</span></span> <span data-ttu-id="b8468-144">Vollständige Beispiele mit Beispiel Namen finden Sie im Abschnitt [vollständige Beispiel Registrierungen](#complete-sample-registrations) .</span><span class="sxs-lookup"><span data-stu-id="b8468-144">Full examples with example names in place are provided in the [Complete Sample Registrations](#complete-sample-registrations) section.</span></span>

 

<span data-ttu-id="b8468-145">Alle Clienttyp-Registrierungsinformationen werden unter dem folgenden Unterschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="b8468-145">All client type registration information is stored under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

<span data-ttu-id="b8468-146">*Clienttypname* ist einer der folgenden Unterschlüssel Namen:</span><span class="sxs-lookup"><span data-stu-id="b8468-146">*ClientTypeName* is one of the following subkey names:</span></span>

-   <span data-ttu-id="b8468-147">Startmenü Internet (für Browser)</span><span class="sxs-lookup"><span data-stu-id="b8468-147">StartMenuInternet (for browsers)</span></span>
-   <span data-ttu-id="b8468-148">E-Mail (für e-Mail)</span><span class="sxs-lookup"><span data-stu-id="b8468-148">Mail (for email)</span></span>
-   <span data-ttu-id="b8468-149">Medien (für Medienwiedergabe)</span><span class="sxs-lookup"><span data-stu-id="b8468-149">Media (for media playback)</span></span>
-   <span data-ttu-id="b8468-150">IM (für Instant Messaging)</span><span class="sxs-lookup"><span data-stu-id="b8468-150">IM (for instant messaging)</span></span>
-   <span data-ttu-id="b8468-151">JavaVM (für virtuellen Computer für Java)</span><span class="sxs-lookup"><span data-stu-id="b8468-151">JavaVM (for virtual machine for Java)</span></span>

<span data-ttu-id="b8468-152">In diesem Thema finden Sie Verweise auf ein fiktives Computerprogramm mit dem Namen "Lit View" von Litware Inc. mit einer ausführbaren Datei namens Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="b8468-152">Throughout this topic, you will note references to a fictional computer program named "Lit View" by Litware Inc., with an executable file named Litview.exe.</span></span> <span data-ttu-id="b8468-153">Dieses hypothetische Programm wird als Instant Messenger, Browser oder ein anderer Typ von Client Programm verwendet, der für die Veranschaulichung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b8468-153">This hypothetical program is used interchangeably as an instant messenger, a browser, or another type of client program as needed for illustrative purposes.</span></span>

### <a name="selecting-a-canonical-name"></a><span data-ttu-id="b8468-154">Auswählen eines kanonischen Namens</span><span class="sxs-lookup"><span data-stu-id="b8468-154">Selecting a Canonical Name</span></span>

<span data-ttu-id="b8468-155">Der Anbieter muss einen *kanonischen Namen* für das Programm auswählen.</span><span class="sxs-lookup"><span data-stu-id="b8468-155">The vendor must choose a *canonical name* for the program.</span></span> <span data-ttu-id="b8468-156">Der kanonische Name wird dem Benutzer nie angezeigt und muss daher nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-156">The canonical name is never shown to the user, so it does not need to be localized.</span></span> <span data-ttu-id="b8468-157">Der einzige Zweck besteht darin, eine eindeutige Zeichenfolge bereitzustellen, die zum Identifizieren des Programms verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8468-157">Its only purpose is to provide a unique string that can be used to identify the program.</span></span> <span data-ttu-id="b8468-158">Er ist in der Regel mit dem englischen Namen des Programms identisch, aber dies ist lediglich eine Konvention.</span><span class="sxs-lookup"><span data-stu-id="b8468-158">It is typically the same as the English name of the program, but this is merely a convention.</span></span>

<span data-ttu-id="b8468-159">Für andere Client Typen als Browser kann der kanonische Name eine beliebige Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="b8468-159">For client types other than browsers, the canonical name can be any string.</span></span> <span data-ttu-id="b8468-160">Wählen Sie einen eindeutigen Namen aus, der nicht wahrscheinlich von einem anderen Anbieter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8468-160">Choose a unique name, one that is not likely to be used by another vendor.</span></span>

<span data-ttu-id="b8468-161">Bei Browser Clients muss der kanonische Name der Name – einschließlich der Erweiterung – der zugeordneten ausführbaren Datei sein. Beispiel: "Litview.exe".</span><span class="sxs-lookup"><span data-stu-id="b8468-161">For browser clients, the canonical name must be the name—including the extension—of the associated executable; for instance, "Litview.exe".</span></span>

<span data-ttu-id="b8468-162">Im folgenden finden Sie einige Beispiele für kanonische Namen.</span><span class="sxs-lookup"><span data-stu-id="b8468-162">Here are some examples of canonical names.</span></span>

-   <span data-ttu-id="b8468-163">Iexplore.exe (Browser)</span><span class="sxs-lookup"><span data-stu-id="b8468-163">Iexplore.exe (browser)</span></span>
-   <span data-ttu-id="b8468-164">Windows Mail (e-Mail)</span><span class="sxs-lookup"><span data-stu-id="b8468-164">Windows Mail (email)</span></span>
-   <span data-ttu-id="b8468-165">Windows-Media Player (Medien)</span><span class="sxs-lookup"><span data-stu-id="b8468-165">Windows Media Player (media)</span></span>
-   <span data-ttu-id="b8468-166">Windows Messenger (Instant Messaging)</span><span class="sxs-lookup"><span data-stu-id="b8468-166">Windows Messenger (instant messaging)</span></span>

<span data-ttu-id="b8468-167">Registrieren Sie den kanonischen Namen, indem Sie wie hier gezeigt einen Unterschlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8468-167">Register the canonical name by creating a subkey as shown here.</span></span> <span data-ttu-id="b8468-168">Der Name des unter Schlüssels ist der kanonische Name.</span><span class="sxs-lookup"><span data-stu-id="b8468-168">The name of the subkey is the canonical name.</span></span> <span data-ttu-id="b8468-169">Alle Informationen im Zusammenhang mit der Registrierung dieses Programms sind unter diesem Unterschlüssel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b8468-169">All information relating to that program's registration will exist under this subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a><span data-ttu-id="b8468-170">Registrieren des anzeigen Amens eines Programms</span><span class="sxs-lookup"><span data-stu-id="b8468-170">Registering a Program's Display Name</span></span>

<span data-ttu-id="b8468-171">Der nächste Schritt bei der Registrierung besteht darin, den anzeigen amen des Programms anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b8468-171">The next step in registration is to specify the program's display name.</span></span> <span data-ttu-id="b8468-172">Sie wird als Wert unter dem kanonischen Namens Schlüssel angegeben, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8468-172">It is given as a value under the canonical name key as shown here.</span></span> <span data-ttu-id="b8468-173">Beachten Sie, dass *CanonicalName* und *clienttykame* nicht die tatsächlichen Namen der Schlüssel sind, sondern nur Platzhalter für die tatsächlichen Namen, wie z. b. die *Beleuchtung*.</span><span class="sxs-lookup"><span data-stu-id="b8468-173">Note again that *CanonicalName* and *ClientTypeName* are not the actual names of the keys, but only placeholders for the true names, such as *Lit View*.</span></span>

> [!Note]  
> <span data-ttu-id="b8468-174">Ab Windows 8 sollte der Name, der für die Registrierung für [Set Program Access und Computer Standards (SPAD)](cpl-setprogramaccess.md) und für [Standardprogramme](default-programs.md) verwendet wird, identisch sein, damit SPAD-Änderungen Standardprogramm Registrierungen auslöst.</span><span class="sxs-lookup"><span data-stu-id="b8468-174">As of Windows 8, the name used to register for [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and for [Default Programs](default-programs.md) should match in order for SPAD changes to trigger Default Programs registrations.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

<span data-ttu-id="b8468-175">Der **LocalizedString** -Wert ist eine reg \_ SZ-Zeichenfolge und besteht aus einem "at"-Zeichen (@), dem vollständigen Pfad zu einer DLL-oder exe-Datei, einem Komma, einem Minuszeichen und einer ganzen Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="b8468-175">The **LocalizedString** value is a REG\_SZ string and consists of an "at" sign (@), the full path to a .dll or .exe file, a comma, a minus sign, and a decimal integer.</span></span> <span data-ttu-id="b8468-176">Die ganzzahlige Ganzzahl ist die ID einer Zeichen folgen Ressource –, die in der DLL-oder exe-Datei enthalten ist –, deren Wert dem Benutzer als Name dieses Clients angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8468-176">The decimal integer is the ID of a string resource—contained within the .dll or .exe file—whose value is to be displayed to the user as the name of this client.</span></span> <span data-ttu-id="b8468-177">Beachten Sie, dass der Dateipfad keine Anführungszeichen erfordert, auch wenn er Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="b8468-177">Note that the file path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="b8468-178">Wenn Sie die Zeichenfolge für den anzeigen Amen auf diese Weise registrieren, kann dieselbe Registrierung für mehrere Sprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-178">Registering the display name string in this manner allows the same registration to be used for multiple languages.</span></span> <span data-ttu-id="b8468-179">Jede sprach Installation bietet eine andere Ressourcen Datei mit dem anzeigen Amen, der in derselben Ressourcen-ID gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b8468-179">Each language installation provides a different resource file with the display name stored at the same resource ID.</span></span>

<span data-ttu-id="b8468-180">Im folgenden Beispiel wird die Registrierung für ein fiktives beleuchtetes Ansichts-Instant Messaging-Programm gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8468-180">The following example shows the registration for a fictional Lit View instant messaging program.</span></span> <span data-ttu-id="b8468-181">Da es sich um ein Instant Messaging-Programm handelt, wird der Unterschlüssel " *CanonicalName* " (in diesem Fall " *lit View*") unter dem **im** -Unterschlüssel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b8468-181">Because it is an instant messaging program, the *CanonicalName* subkey (in this case *Lit View*) is stored under the **IM** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="b8468-182">Beachten Sie die Verwendung des (Standard-) Eintrags als sekundäre Deklaration des Client anzeigen Amens.</span><span class="sxs-lookup"><span data-stu-id="b8468-182">Note the use of the (Default) entry as a secondary declaration of the client's display name.</span></span> <span data-ttu-id="b8468-183">Wenn die **LocalizedString** nicht vorhanden ist, wird stattdessen der (standardmäßige) Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8468-183">If the **LocalizedString** is not present, the (Default) value is used instead.</span></span> <span data-ttu-id="b8468-184">Dies funktioniert bei allen Client Typen (Internet Browser, e-Mail-Browser, Instant Messenger und Media Players).</span><span class="sxs-lookup"><span data-stu-id="b8468-184">This works with all client types (Internet browsers, email browsers, instant messengers, and media players).</span></span> <span data-ttu-id="b8468-185">Aus Gründen der Abwärtskompatibilität mit dem [Internet Explorer-Client Registrierungs Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))sollte der (Standardwert)-Wert des unter Schlüssels " *CanonicalName* " von e-Mail-Programmen in der aktuell installierten Sprache auf den anzeigen amen des Clients festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-185">For backward compatibility with the [Internet Explorer Client Registry Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), email programs should set the (Default) value of the *CanonicalName* subkey to the client's display name in the currently installed language.</span></span>

### <a name="registering-a-programs-icon"></a><span data-ttu-id="b8468-186">Registrieren eines Programm Symbols</span><span class="sxs-lookup"><span data-stu-id="b8468-186">Registering a Program's Icon</span></span>

> [!Note]  
> <span data-ttu-id="b8468-187">Dieser Abschnitt gilt nicht für Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b8468-187">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="b8468-188">Standardmäßig enthält der obere Abschnitt des **Start** Menüs von Windows XP und Windows Vista **Internet** -und **e-Mail-** Symbole.</span><span class="sxs-lookup"><span data-stu-id="b8468-188">By default, the upper section of the Windows XP and Windows Vista **Start** menu contains **Internet** and **E-mail** icons.</span></span> <span data-ttu-id="b8468-189">Diese Symbole sind in Windows 7 und höher nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b8468-189">These icons are not present in Windows 7 and later.</span></span> <span data-ttu-id="b8468-190">Wenn für Browser-und e-Mail-Clients ein Programm als Standardwert für den Clienttyp zugewiesen ist, wird das registrierte Symbol dieses Programms für diese Einträge im **Startmenü** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8468-190">For browser and email clients, when a program is assigned as the default for their client type, that program's registered icon is displayed for those **Start** menu entries.</span></span>

<span data-ttu-id="b8468-191">Das Registrieren eines Programm Symbols ist für Browser-und e-Mail-Clients obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="b8468-191">Registering a program's icon is mandatory for browser and email clients.</span></span> <span data-ttu-id="b8468-192">Das Registrieren eines Symbols für die Medienwiedergabe, das Instant Messaging oder den virtuellen Computer für Java-Client Typen ist optional, und registrierte Symbole für diese Client Typen werden zurzeit nicht von Windows verwendet und nicht im oberen Abschnitt der **Start** Menüs von Windows XP oder Windows Vista angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8468-192">Registering an icon for the media playback, instant messaging, or virtual machine for Java client types is optional, and registered icons for those client types are not currently used by Windows and are not displayed in the upper section of the Windows XP or Windows Vista **Start** menus.</span></span>

<span data-ttu-id="b8468-193">Zum Registrieren eines Symbols für ein Client Programm fügen Sie einen **DefaultIcon** -Unterschlüssel mit einem Standardwert hinzu, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8468-193">To register an icon for a client program, add a **DefaultIcon** subkey with a default value as shown here.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

<span data-ttu-id="b8468-194">Der Wert **FilePath** ist der vollständige Pfad zu der Datei, die das Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="b8468-194">The **FilePath** value is the full path to the file that contains the icon.</span></span> <span data-ttu-id="b8468-195">Für diesen Pfad sind keine Anführungszeichen erforderlich, auch wenn er Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="b8468-195">This path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="b8468-196">Der **IconIndex** -Wert wird wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="b8468-196">The **IconIndex** value is interpreted as follows:</span></span>

-   <span data-ttu-id="b8468-197">Wenn **IconIndex** eine positive Zahl ist, wird die Zahl als Index des *NULL basierten* Arrays von Symbolen verwendet, das in der Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b8468-197">If **IconIndex** is a positive number, the number is used as the index of the *zero-based* array of icons stored in the file.</span></span> <span data-ttu-id="b8468-198">Wenn **IconIndex** z. b. 1 ist, wird das zweite Symbol aus der Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="b8468-198">For example, if **IconIndex** is 1, the second icon is loaded from the file.</span></span>
-   <span data-ttu-id="b8468-199">Wenn **IconIndex** eine negative Zahl ist, wird der absolute Wert von **IconIndex** als Ressourcen Bezeichner (anstelle des Indexes) für das Symbol verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8468-199">If **IconIndex** is a negative number, the absolute value of **IconIndex** is used as the resource identifier (rather than the index) for the icon.</span></span> <span data-ttu-id="b8468-200">Wenn **IconIndex** beispielsweise den Wert-3 hat, wird das Symbol, dessen Ressourcen Bezeichner den Wert 3 hat, aus der Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="b8468-200">For example, if **IconIndex** is -3, the icon whose resource identifier is 3 is loaded from the file.</span></span>

<span data-ttu-id="b8468-201">Das folgende Beispiel zeigt die Registrierung eines hypothetischen beleuchteten Ansichts Browsers.</span><span class="sxs-lookup"><span data-stu-id="b8468-201">The following example shows the registration of a hypothetical Lit View browser.</span></span> <span data-ttu-id="b8468-202">Das zweite Symbol, das in der Litview.exe-Datei gespeichert wird, wird als Standard verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8468-202">The second icon stored in the Litview.exe file is used as the default.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a><span data-ttu-id="b8468-203">Registrieren eines geöffneten Verbs</span><span class="sxs-lookup"><span data-stu-id="b8468-203">Registering an Open Verb</span></span>

> [!Note]  
> <span data-ttu-id="b8468-204">Dieser Abschnitt gilt nicht für Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b8468-204">This section does not apply to Windows 2000.</span></span> <span data-ttu-id="b8468-205">Der folgende Schritt ist nur für Browser-und e-Mail-Clients erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8468-205">The following step is necessary only for browser and email clients.</span></span>

 

<span data-ttu-id="b8468-206">Angenommen, ein Benutzer hat Ihr Programm als standardmäßiges Internet oder e-Mail-Programm ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b8468-206">Assume that a user has selected your program as the default Internet or email program.</span></span> <span data-ttu-id="b8468-207">Dieser Benutzer klickt im **Startmenü** von Windows XP oder Windows Vista auf das **Internet** oder das **e-Mail-** Symbol, um das Programm zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8468-207">That user clicks the **Internet** or **E-mail** icon in the Windows XP or Windows Vista **Start** menu to open the program.</span></span> <span data-ttu-id="b8468-208">An diesem Punkt wird die Befehlszeile, die wie hier gezeigt registriert ist, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8468-208">At that point, the command line registered as shown here is executed.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

<span data-ttu-id="b8468-209">Die Befehlszeile muss einen voll qualifizierten absoluten Pfad zur Datei angeben, gefolgt von optionalen Befehlszeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="b8468-209">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="b8468-210">Wenn der Eintragstyp reg \_ Expand- \_ SZ ist, können Umgebungsvariablen im Pfad verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-210">If the entry type is REG\_EXPAND\_SZ, environment variables can be used in the path.</span></span> <span data-ttu-id="b8468-211">Verwenden Sie Anführungszeichen entsprechend, um sicherzustellen, dass Leerzeichen in der Befehlszeile nicht falsch interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-211">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span> <span data-ttu-id="b8468-212">Die Befehlszeile sollte das Programm mit den entsprechenden Standardeinstellungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8468-212">The command line should execute the program with appropriate defaults.</span></span> <span data-ttu-id="b8468-213">Browser werden im Allgemeinen standardmäßig auf die Startseite des Benutzers eingestellt.</span><span class="sxs-lookup"><span data-stu-id="b8468-213">Browsers generally default to the user's home page.</span></span> <span data-ttu-id="b8468-214">E-Mail-Programme öffnen den **Posteingangs** des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b8468-214">Email programs generally open the user's **Inbox**.</span></span>

<span data-ttu-id="b8468-215">Das folgende Beispiel zeigt die Registrierung eines `open` Verbs für einen hypothetischen beleuchteten Ansichts Browser.</span><span class="sxs-lookup"><span data-stu-id="b8468-215">The following example shows the registration of an `open` verb for a hypothetical Lit View browser.</span></span> <span data-ttu-id="b8468-216">Es gibt keine Befehlszeilenoptionen an.</span><span class="sxs-lookup"><span data-stu-id="b8468-216">It specifies no command-line options.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

<span data-ttu-id="b8468-217">Beachten Sie, dass in diesem Wert Anführungszeichen um den Pfad platziert werden, da Sie eingebettete Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="b8468-217">Note that in this value, quotation marks are placed around the path because it contains embedded spaces.</span></span> <span data-ttu-id="b8468-218">Wenn Sie diese Anführungszeichen weglassen, kann dies dazu führen, dass die Befehlszeile falsch interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="b8468-218">Omitting these quotation marks could cause the command line to be misinterpreted.</span></span>

### <a name="registering-installation-information"></a><span data-ttu-id="b8468-219">Installationsinformationen werden registriert</span><span class="sxs-lookup"><span data-stu-id="b8468-219">Registering Installation Information</span></span>

> [!Note]  
> <span data-ttu-id="b8468-220">Dieser Abschnitt gilt nicht für Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b8468-220">This section does not apply to Windows Server 2003.</span></span>

 

-   [<span data-ttu-id="b8468-221">Der Befehl "neu installieren"</span><span class="sxs-lookup"><span data-stu-id="b8468-221">The Reinstall Command</span></span>](#the-reinstall-command)
-   [<span data-ttu-id="b8468-222">Befehl zum Ausblenden von Symbolen</span><span class="sxs-lookup"><span data-stu-id="b8468-222">The Hide Icons Command</span></span>](#the-hide-icons-command)
-   [<span data-ttu-id="b8468-223">Der Befehl "Symbole anzeigen"</span><span class="sxs-lookup"><span data-stu-id="b8468-223">The Show Icons Command</span></span>](#the-show-icons-command)
-   [<span data-ttu-id="b8468-224">Gruppenprogramm Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b8468-224">Group Program Configuration</span></span>](#group-program-configuration)
-   [<span data-ttu-id="b8468-225">Beispiel für eine Browser Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-225">Browser Registration Example</span></span>](#browser-registration-example)

<span data-ttu-id="b8468-226">Die Funktion, mit der der Benutzer Computer spezifische Standardprogramme auswählt, wird benannt und darauf zugegriffen, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b8468-226">The feature by which the user selects per-machine default programs is named and accessed as shown in the following table.</span></span> <span data-ttu-id="b8468-227">(In Windows Vista wurde ein neues Feature eingeführt, das **Standardprogramm wird festgelegt**, mit dem ein Benutzer benutzerspezifische Standardeinstellungen festlegen kann.)</span><span class="sxs-lookup"><span data-stu-id="b8468-227">(Windows Vista introduced a new feature, **Set your default programs**, by which a user can set per-user defaults.)</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8468-228">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b8468-228">Operating System</span></span></th>
<th><span data-ttu-id="b8468-229">Titel</span><span class="sxs-lookup"><span data-stu-id="b8468-229">Title</span></span></th>
<th><span data-ttu-id="b8468-230">Zugriffs Speicherort</span><span class="sxs-lookup"><span data-stu-id="b8468-230">Access Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8468-231">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8468-231">Windows 7</span></span></td>
<td><span data-ttu-id="b8468-232">Festlegen des Programm Zugriffs und der Standardeinstellungen des Computers</span><span class="sxs-lookup"><span data-stu-id="b8468-232">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="b8468-233"><strong>Start</strong> Menü ( <strong>Standardprogramme</strong> -Option)</span><span class="sxs-lookup"><span data-stu-id="b8468-233"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="b8468-234"><strong>Standardprogramme</strong> System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="b8468-234"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8468-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8468-235">Windows Vista</span></span></td>
<td><span data-ttu-id="b8468-236">Festlegen des Programm Zugriffs und der Standardeinstellungen des Computers</span><span class="sxs-lookup"><span data-stu-id="b8468-236">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="b8468-237"><strong>Start</strong> Menü ( <strong>Standardprogramme</strong> -Option)</span><span class="sxs-lookup"><span data-stu-id="b8468-237"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="b8468-238"><strong>Standardprogramme</strong> System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="b8468-238"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8468-239">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="b8468-239">Windows XP SP2</span></span></td>
<td><span data-ttu-id="b8468-240">Festlegen des Programm Zugriffs und der Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="b8468-240">Set Program Access and Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="b8468-241"><strong>Startmenü</strong></span><span class="sxs-lookup"><span data-stu-id="b8468-241"><strong>Start</strong> menu</span></span></li>
<li><span data-ttu-id="b8468-242">Software <strong>Hinzufügen oder entfernen</strong> System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="b8468-242"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8468-243">Windows XP SP1</span><span class="sxs-lookup"><span data-stu-id="b8468-243">Windows XP SP1</span></span></td>
<td><span data-ttu-id="b8468-244">Konfigurieren von Programmen</span><span class="sxs-lookup"><span data-stu-id="b8468-244">Configure Programs</span></span></td>
<td><ul>
<li><span data-ttu-id="b8468-245">Software <strong>Hinzufügen oder entfernen</strong> System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="b8468-245"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b8468-246">Der Einfachheit halber wird in diesem Thema der Windows 7-Titel des Features verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8468-246">For simplicity, this topic uses the Windows 7 title of the feature.</span></span> <span data-ttu-id="b8468-247">Alle Versionen der Funktion werden als SPAD bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b8468-247">All versions of the feature are popularly referred to as SPAD.</span></span>

> [!Note]  
> <span data-ttu-id="b8468-248">Wenn Sie Windows 2000 oder Windows XP ausführen, muss mindestens Windows 2000 SP3 oder Windows XP SP1 installiert sein, damit die Seite " **Programm Zugriff und Standardeinstellungen festlegen** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b8468-248">If you are running Windows 2000 or Windows XP, you must have at least Windows 2000 SP3 or Windows XP SP1 installed to see the **Set Program Access and Defaults** page.</span></span> <span data-ttu-id="b8468-249">In Windows Vista und höher sind für den Zugriff auf die Seite " **Programm Zugriff und Computer Standards festlegen** " Administrator Rechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8468-249">In Windows Vista and later, access to the **Set Program Access and Computer Defaults** page requires Administrator privileges.</span></span> <span data-ttu-id="b8468-250">Aus diesem Grund wird Entwicklern empfohlen, sich für das System Steuerungselement " [Standardprogramme festlegen](default-programs.md) " zu registrieren, damit jeder Benutzer Anwendungs Standardwerte verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="b8468-250">For this reason, developers are encouraged to register for the [Set your default programs](default-programs.md) Control Panel item so that any user can manage application defaults.</span></span>

 

<span data-ttu-id="b8468-251">Die folgende Registrierungs Struktur zeigt die Vielzahl der Informationen, die im **installinfo** -Schlüssel des Programms registriert werden müssen, damit das Programm auf der Seite **Programm Zugriff und Computer Standards festlegen** als Option für den Clienttyp angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b8468-251">The following registry tree shows the variety of information that must be registered in the program's **InstallInfo** key in order for the program to appear on the **Set Program Access and Computer Defaults** page as an option for its client type.</span></span> <span data-ttu-id="b8468-252">Diese Werte werden in den folgenden Abschnitten ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="b8468-252">Each of these values is discussed in detail in the following sections.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

<span data-ttu-id="b8468-253">Die Befehlszeile muss einen voll qualifizierten absoluten Pfad zur Datei angeben, gefolgt von optionalen Befehlszeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="b8468-253">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="b8468-254">Verwenden Sie Anführungszeichen entsprechend, um sicherzustellen, dass Leerzeichen in der Befehlszeile nicht falsch interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-254">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span>

### <a name="the-reinstall-command"></a><span data-ttu-id="b8468-255">Der Befehl "neu installieren"</span><span class="sxs-lookup"><span data-stu-id="b8468-255">The Reinstall Command</span></span>

<span data-ttu-id="b8468-256">Die im reinstallcommand-Wert deklarierte Befehlszeile für die erneute Installation wird ausgeführt, wenn der Benutzer die Seite " **Programm Zugriff und Computer Standards festlegen** " verwendet, um das Programm als Standardwert für den Clienttyp auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b8468-256">The reinstall command line declared in the ReinstallCommand value is executed when the user uses the **Set Program Access and Computer Defaults** page to select your program as the default for its client type.</span></span> <span data-ttu-id="b8468-257">In Windows Vista und höher ist für den Zugriff auf diese Seite eine Administrator Berechtigungsstufe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8468-257">In Windows Vista and later, access to this page requires an Administrator privilege level.</span></span> <span data-ttu-id="b8468-258">Wenn Sie in Windows 8 Ihre Anwendung mit dem gleichen Namen sowohl für den **Programm Zugriffs Satz als** auch für **Standardprogramme** registriert haben, werden die in **Standardprogrammen** für diese Anwendung angegebenen Standardwerte auf den aktuellen Benutzer angewendet, und der Befehl "neu installieren" wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8468-258">In Windows 8, if you have registered your application using the same name for both **Set Program Access and Computer Defaults** and **Default Programs**, the defaults specified in **Default Programs** for that application will be applied for the current user as well as running the reinstall command.</span></span>

<span data-ttu-id="b8468-259">Das Programm, das von der neu [Installationsbefehlszeile](fa-intro.md) gestartet wird, muss die Anwendung mit dem kompletten Satz von Datei-und [Protokoll](/previous-versions//aa767743(v=vs.85)) Typen verknüpfen, die die Anwendung verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b8468-259">The program launched by the reinstall command line must associate the application with the complete set of [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types the application can handle.</span></span> <span data-ttu-id="b8468-260">Alle Anwendungen müssen die Handlerfunktion im Befehl Neuinstallation einrichten.</span><span class="sxs-lookup"><span data-stu-id="b8468-260">All applications must establish handler capability in the reinstall command.</span></span> <span data-ttu-id="b8468-261">Anwendungen können den Befehl "neu installieren" verwenden, um die Funktion zu registrieren und optional den Standardstatus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b8468-261">Applications can use the reinstall command to register capability as well as optionally establish default status.</span></span> <span data-ttu-id="b8468-262">Wenn eine Anwendung sowohl den Funktions-als auch den standardhandlerstatus im installieren Sie-Befehl implementiert, sollte Sie auch alle gewünschten sichtbaren Verknüpfungen oder Verknüpfungen wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="b8468-262">When an application chooses to implement both capability and default handler status in the reinstall command, it should also reinstate any visible links or shortcuts desired.</span></span> <span data-ttu-id="b8468-263">Die sichtbaren Einstiegspunkte, die von den meisten Anwendungen ausgewählt werden, werden im [Befehl Symbole ausblenden](#the-hide-icons-command)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8468-263">The visible entry points most applications choose are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span>

> [!Note]  
> <span data-ttu-id="b8468-264">Es wird dringend empfohlen, dass Anwendungen die Verarbeitungs Funktion im Befehl "neu installieren" implementieren.</span><span class="sxs-lookup"><span data-stu-id="b8468-264">It is highly recommended that applications implement handling capability in the reinstall command.</span></span>

 

<span data-ttu-id="b8468-265">Nach Abschluss des Neuinstallations Vorgangs sollte das von der Befehlszeile für die erneute Installation gestartete Programm beendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-265">Once the reinstall process is complete, the program launched by the reinstall command line should exit.</span></span> <span data-ttu-id="b8468-266">Das entsprechende Programm sollte nicht gestartet werden. Es sollten nur Standardwerte registriert werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-266">It should not launch the corresponding program; it should merely register defaults.</span></span> <span data-ttu-id="b8468-267">Beispielsweise sollte der Befehl "neu installieren" für einen Browser nicht die Startseite des Benutzers öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8468-267">For example, the reinstall command for a browser should not open the user's home page.</span></span>

> [!Note]  
> <span data-ttu-id="b8468-268">Bei Browser-und e-Mail-Clients unter Windows XP und Windows Vista sollte sich eine Registrierung für das entsprechende Symbol am oberen Rand des Start Menüs durchführen.</span><span class="sxs-lookup"><span data-stu-id="b8468-268">For browser and email clients in Windows XP and Windows Vista, applications that choose to establish both handling capability and default status in the reinstall command should register for the corresponding icon at the top of the Start menu.</span></span> <span data-ttu-id="b8468-269">Weitere Informationen finden Sie unter [Start Menü Registrierung](#start-menu-registration) .</span><span class="sxs-lookup"><span data-stu-id="b8468-269">See [Start Menu Registration](#start-menu-registration) for additional information.</span></span>

 

### <a name="the-hide-icons-command"></a><span data-ttu-id="b8468-270">Befehl zum Ausblenden von Symbolen</span><span class="sxs-lookup"><span data-stu-id="b8468-270">The Hide Icons Command</span></span>

<span data-ttu-id="b8468-271">Die Befehlszeile, die im hideidescommand-Wert deklariert wird, wird ausgeführt, wenn der Benutzer das **Kontrollkästchen Zugriff auf dieses Programm aktivieren** auf der Seite **Programm Zugriff und Computer Standards festlegen** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8468-271">The command line declared in the HideIconsCommand value is executed when the user clears the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="b8468-272">Diese Befehlszeile muss alle Zugriffspunkte Ihres Programms ausblenden, die auf der Benutzeroberfläche sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="b8468-272">This command line must hide all of your program's access points that are visible in the user interface.</span></span> <span data-ttu-id="b8468-273">Die spezifischen Richtlinien sind das Entfernen von Verknüpfungen und Symbolen aus den folgenden Speicherorten:</span><span class="sxs-lookup"><span data-stu-id="b8468-273">The specific guidelines are to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="b8468-274">Desktop Symbole</span><span class="sxs-lookup"><span data-stu-id="b8468-274">Desktop icons</span></span>
-   <span data-ttu-id="b8468-275">Startmenü Links, einschließlich der **Start** Gruppe</span><span class="sxs-lookup"><span data-stu-id="b8468-275">Start menu links, including the **Startup** group</span></span>
-   <span data-ttu-id="b8468-276">Links für die Schnellstartleiste</span><span class="sxs-lookup"><span data-stu-id="b8468-276">Quick Launch bar links</span></span>
-   <span data-ttu-id="b8468-277">Benachrichtigungsbereich</span><span class="sxs-lookup"><span data-stu-id="b8468-277">Notification area</span></span>
-   <span data-ttu-id="b8468-278">Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="b8468-278">Shortcut menus</span></span>
-   <span data-ttu-id="b8468-279">Ordnertaskband</span><span class="sxs-lookup"><span data-stu-id="b8468-279">Folder task band</span></span>

<span data-ttu-id="b8468-280">Diese Befehlszeile muss auch automatische Aufrufe des Programms verhindern, z. b. die im Registrierungsschlüssel **Ausführen** angegebenen.</span><span class="sxs-lookup"><span data-stu-id="b8468-280">This command line must also prevent automatic invocations of the program, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="b8468-281">Es wird empfohlen, diese Richtlinien in der Anwendung zum Ausblenden des Zugriffs Rückrufs zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="b8468-281">Vendors are encouraged to implement these guidelines in the application's Hide Access callback.</span></span>

<span data-ttu-id="b8468-282">Wenn Symbole ausgeblendet werden, müssen Sie die Registrierung (Anwendungsfunktion) von Dateitypen nicht aufgeben.</span><span class="sxs-lookup"><span data-stu-id="b8468-282">You do not need to relinquish registration (application capability) of file types when icons are hidden.</span></span> <span data-ttu-id="b8468-283">Außerdem müssen Sie den Standardstatus der Anwendung für Datei-und Protokolltypen nicht aufgeben.</span><span class="sxs-lookup"><span data-stu-id="b8468-283">You also do not need to relinquish the application's default status for file and protocol types.</span></span> <span data-ttu-id="b8468-284">Dies kann zu einer ungültigen Benutzeroberfläche führen, wenn diese Typen in der Benutzeroberfläche gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-284">Doing so can lead to a bad user experience when these types are encountered in the UI.</span></span>

<span data-ttu-id="b8468-285">Nach dem erfolgreichen Ausblenden von Symbolen müssen Sie den iconsvisible-Registrierungs Wert wie folgt auf 0 aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="b8468-285">After successfully hiding icons, you must update the IconsVisible registry value to 0 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

<span data-ttu-id="b8468-286">Der iconsvisible-Eintrag ist vom Typ " **reg \_ DWORD**".</span><span class="sxs-lookup"><span data-stu-id="b8468-286">The IconsVisible entry is of type **REG\_DWORD**.</span></span>

### <a name="an-alternate-hide-icons-method-in-spad"></a><span data-ttu-id="b8468-287">Eine alternative Methode zum Ausblenden von Symbolen in SPAD</span><span class="sxs-lookup"><span data-stu-id="b8468-287">An Alternate Hide Icons Method in SPAD</span></span>

<span data-ttu-id="b8468-288">Bei einigen Legacy Anwendungen ist eine vollständige Implementierung des Ausblenden des Zugriffs möglicherweise nicht praktikabel.</span><span class="sxs-lookup"><span data-stu-id="b8468-288">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="b8468-289">Eine alternative Methode, die denselben Effekt erzielt, ist die Deinstallation der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b8468-289">An alternative method that achieves the same effect is to uninstall the application.</span></span> <span data-ttu-id="b8468-290">Der nachfolgende Abschnitt zeigt Beispiel Verhalten und Beispielcode zum Implementieren dieser Alternativen.</span><span class="sxs-lookup"><span data-stu-id="b8468-290">The section below shows example behavior and sample code to implement this alternative.</span></span> <span data-ttu-id="b8468-291">Im Allgemeinen sollten unabhängige Softwarehersteller (ISVs) diese Alternative vermeiden, da Sie Folgendes bietet:</span><span class="sxs-lookup"><span data-stu-id="b8468-291">In general, independent software vendors (ISVs) should avoid this alternative since it will:</span></span>

-   <span data-ttu-id="b8468-292">Deinstallieren Sie die Anwendung vollständig aus dem System.</span><span class="sxs-lookup"><span data-stu-id="b8468-292">Uninstall the application completely from the system.</span></span>
-   <span data-ttu-id="b8468-293">Entfernt zuvor ausgewählte Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="b8468-293">Remove previously selected defaults.</span></span>
-   <span data-ttu-id="b8468-294">Lassen Sie die Option keine Benutzeroberfläche zur erneuten Installation der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b8468-294">Leave no UI option to reinstall the application.</span></span>
-   <span data-ttu-id="b8468-295">Aktivieren Sie das Feature "Zugriff aktivieren" nicht mehr, da die Anwendung durch eine Deinstallation vollständig aus SPAD entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b8468-295">Make the enable access feature no longer available, since an uninstallation removes the application completely from SPAD.</span></span>

<span data-ttu-id="b8468-296">Die empfohlene Benutzer Darstellung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b8468-296">The recommended user experience is as follows:</span></span>

-   <span data-ttu-id="b8468-297">Wenn der Benutzer das Kontrollkästchen **Zugriff auf dieses Programm aktivieren** in SPAD deaktivieren, wird die folgende Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8468-297">When the user unchecks the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![Dialogfeld zum Ausblenden des Programm Zugriffs](images/hideaccessvista.png)

-   <span data-ttu-id="b8468-299">Wenn der Benutzer **OK** auswählt, wird das System Steuerungselement **Programme und Funktionen** gestartet, um dem Benutzer die Deinstallation der Anwendung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b8468-299">When the user selects **OK**, the **Programs and Features** Control Panel item launches to allow the user to uninstall the application.</span></span>
-   <span data-ttu-id="b8468-300">In diesem Dialogfeld sollten Windows XP-Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-300">Windows XP users should be presented with this dialog box.</span></span>

    ![entsprechendes Windows XP-Dialogfeld](images/hideaccessxp.png)

-   <span data-ttu-id="b8468-302">Wenn der Windows XP-Benutzer **OK** auswählt, wird **das System Steuerungs** Element Software gestartet, um dem Benutzer die Deinstallation der Anwendung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b8468-302">When the Windows XP user selects **OK**, the **Add or Remove Programs** Control Panel item launches to allow the user to uninstall the application.</span></span>

<span data-ttu-id="b8468-303">Der folgende Code stellt eine wiederverwendbare Implementierung für die Funktion "Zugriff ausblenden" bereit, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b8468-303">The following code provides a reusable implementation for the Hide Access feature as outlined above.</span></span> <span data-ttu-id="b8468-304">Sie kann unter Windows XP, Windows Vista und Windows 7 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-304">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a><span data-ttu-id="b8468-305">Der Befehl "Symbole anzeigen"</span><span class="sxs-lookup"><span data-stu-id="b8468-305">The Show Icons Command</span></span>

<span data-ttu-id="b8468-306">Die Befehlszeile, die im Eintrag showiconfiguration Command deklariert ist, wird ausgeführt, wenn der Benutzer das Kontrollkästchen **Zugriff auf dieses Programm aktivieren** auf der Seite **Programm Zugriff und Computer Standards festlegen** prüft.</span><span class="sxs-lookup"><span data-stu-id="b8468-306">The command line declared in the ShowIconsCommand entry is executed when the user checks the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="b8468-307">Mit dieser Befehlszeile können Sie die Zugriffspunkte Ihres Programms, einschließlich der im **Startmenü** , auf dem Desktop und in der **Start** Gruppe, sowie der normalen automatischen Aufrufe, wie z. b. der im Registrierungsschlüssel **Ausführen** angegeben, wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="b8468-307">This command line may restore your program's access points, including those in the **Start** menu, on the desktop, and in the **Startup** group, as well as normal automatic invocations, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="b8468-308">Die sichtbaren Zugriffspunkte, die für die meisten Anwendungen von Interesse sind, werden im [Befehl Symbole ausblenden](#the-hide-icons-command)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8468-308">The visible access points of interest to most applications are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span> <span data-ttu-id="b8468-309">Die Anwendung sollte keine benutzerspezifischen Standardeinstellungen ändern. Diese Änderung sollte vom Benutzer über **Standardprogramme** durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-309">The application should not change per-user defaults; that change should be done by the user through **Default Programs**.</span></span>

<span data-ttu-id="b8468-310">Nachdem Sie Ihre Symbole erfolgreich angezeigt haben, müssen Sie den iconsvisible-Registrierungs Wert auf 1 aktualisieren, wie im folgenden gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b8468-310">After successfully showing your icons, you must update the IconsVisible registry value to 1 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

<span data-ttu-id="b8468-311">Beachten Sie Folgendes: Wenn Sie den Eintrag hideiencommand verwendet haben, um eine Deinstallation der Anwendung einzugeben, wird der Eintrag showiencommand nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8468-311">Note that if you have used the HideIconsCommand entry to prompt an uninstall of the application, the ShowIconsCommand entry is of no use.</span></span> <span data-ttu-id="b8468-312">Er sollte bei der Deinstallation aus der Registrierung mit den restlichen Informationen der Anwendung entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-312">It should be removed from the registry with the rest of the application's information during the uninstall process.</span></span>

### <a name="group-program-configuration"></a><span data-ttu-id="b8468-313">Gruppenprogramm Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b8468-313">Group Program Configuration</span></span>

> [!Note]  
> <span data-ttu-id="b8468-314">Dieser Abschnitt gilt nicht für Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b8468-314">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="b8468-315">Im Rahmen der System Vorbereitung kann ein OEM eine Konfiguration einrichten, die Zugriffspunkte für den Microsoft-Browser, die e-Mail, die Medienwiedergabe, das Instant Messaging oder den virtuellen Computer für Java-Client Programme verbirgt und seine eigenen Standardprogramme angibt.</span><span class="sxs-lookup"><span data-stu-id="b8468-315">As part of system preparation, an OEM can establish a configuration that hides access points for the Microsoft browser, email, media playback, instant messaging, or virtual machine for Java client programs and specifies their own default programs.</span></span> <span data-ttu-id="b8468-316">OEMs können es Benutzern ermöglichen, ihre Computer zu einem beliebigen Zeitpunkt auf diese Standardkonfiguration zurückzusetzen, indem Sie die folgenden Registrierungs Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="b8468-316">OEMs can enable users to reset their computers at any time to this default configuration by setting the following registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

<span data-ttu-id="b8468-317">Wenn diese Schlüssel festgelegt sind, können Benutzer die OEM-Konfiguration wiederherstellen, indem Sie die Option **Computer Hersteller** auf der Seite **Programm Zugriff und Computer Standards festlegen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b8468-317">If these keys are set, users can restore the OEM configuration by selecting the **Computer Manufacturer** option on the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="b8468-318">Wenn diese Schlüssel nicht festgelegt sind, wird die Option **Computer Hersteller** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8468-318">If these keys are not set, the **Computer Manufacturer** option is not shown.</span></span>

<span data-ttu-id="b8468-319">Der **oemshowicons** -Eintrag, falls vorhanden, legt den Symbol Anzeige Status für den angegebenen Client fest, der angewendet wird, wenn der Benutzer den **Computer Hersteller** auswählt.</span><span class="sxs-lookup"><span data-stu-id="b8468-319">The **OEMShowIcons** entry, if present, sets the icon show state for the specified client that is applied if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="b8468-320">Der Wert 1 bewirkt, dass Symbole angezeigt werden, und der Wert 0 bewirkt, dass Symbole nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-320">A value of 1 causes icons to be shown, and a value of 0 causes icons to not be shown.</span></span> <span data-ttu-id="b8468-321">Wenn **oemshowicons** nicht vorhanden ist, hat die Auswahl von **Computer Hersteller** keine Auswirkung auf die Symbol Anzeige Einstellung.</span><span class="sxs-lookup"><span data-stu-id="b8468-321">If **OEMShowIcons** is absent, selecting **Computer Manufacturer** has no effect on the icon show setting.</span></span> <span data-ttu-id="b8468-322">**Oemshowicons** ist vom Typ " **reg \_ DWORD**".</span><span class="sxs-lookup"><span data-stu-id="b8468-322">**OEMShowIcons** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="b8468-323">Der **oemdefault** -Eintrag, falls vorhanden und auf 1 festgelegt, legt die OEM-Voreinstellung für den Standard Client des festgelegten Typs fest.</span><span class="sxs-lookup"><span data-stu-id="b8468-323">The **OEMDefault** entry, if present and set to 1, establishes the OEM preference for the default client of the indicated type.</span></span> <span data-ttu-id="b8468-324">Nur ein Client eines bestimmten Typs kann als OEM-Standard gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8468-324">Only one client of a particular type can be marked as the OEM default.</span></span> <span data-ttu-id="b8468-325">Wenn mehr als die Registrierung eines Clients den **oemdefault** -Eintrag enthält, werden alle ignoriert, und der aktuelle Client wird weiterhin als Standard Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8468-325">If more then one client's registration contains the **OEMDefault** entry, then all are ignored and the current client continues to be used as default client.</span></span> <span data-ttu-id="b8468-326">Wenn der **oemdefault** -Eintrag nicht vorhanden oder vorhanden und auf 0 festgelegt ist, wird der jeweilige Client nicht als Standard Client verwendet, wenn der Benutzer den **Computer Hersteller** auswählt.</span><span class="sxs-lookup"><span data-stu-id="b8468-326">If the **OEMDefault** entry is not present or is present and set to 0, then that particular client is not used as the default client if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="b8468-327">**Oemdefault** ist vom Typ " **reg \_ DWORD**".</span><span class="sxs-lookup"><span data-stu-id="b8468-327">**OEMDefault** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="b8468-328">Zusätzlich zur Option, ihre Computer auf die vom OEM festgelegte Standardkonfiguration zurückzusetzen, haben die Benutzer drei weitere Konfigurationsoptionen:</span><span class="sxs-lookup"><span data-stu-id="b8468-328">In addition to the option to reset their computers to the default configuration established by the OEM, users have three other configuration options:</span></span>

-   <span data-ttu-id="b8468-329">Legen Sie Ihren Computer auf eine Microsoft Windows-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="b8468-329">Set their computer to a Microsoft Windows configuration.</span></span> <span data-ttu-id="b8468-330">In diesem Fall wird auf der Seite **Programm Zugriff und Computer Standards festlegen** der Zugriff auf alle Microsoft-und nicht-Microsoft-Software auf dem Computer ermöglicht, der in den relevanten Produktkategorien registriert ist.</span><span class="sxs-lookup"><span data-stu-id="b8468-330">In this case, the **Set Program Access and Computer Defaults** page enables access to all Microsoft and non-Microsoft software on the computer registered in the relevant product categories.</span></span> <span data-ttu-id="b8468-331">Microsoft Windows-Programme werden als Standardoption für jede Kategorie ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b8468-331">Microsoft Windows programs are selected as the default option for each category.</span></span>
-   <span data-ttu-id="b8468-332">Legen Sie Ihren Computer auf eine nicht-Microsoft-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="b8468-332">Set their computer to a non-Microsoft configuration.</span></span> <span data-ttu-id="b8468-333">Diese Konfiguration verbirgt Zugriffspunkte (z. b. das **Startmenü** ) für Windows Internet Explorer, Windows Media Player, Windows Messenger und Microsoft Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="b8468-333">This configuration hides access points (such as the **Start** menu) to Windows Internet Explorer, Windows Media Player, Windows Messenger, and Microsoft Outlook Express.</span></span> <span data-ttu-id="b8468-334">Er ermöglicht den Zugriff auf die Software, die nicht von Microsoft ist, auf dem Computer in diesen Kategorien.</span><span class="sxs-lookup"><span data-stu-id="b8468-334">It enables access to the non-Microsoft software on the computer in these categories.</span></span> <span data-ttu-id="b8468-335">Wenn außerdem ein nicht-Microsoft-Programm in einer Kategorie verfügbar ist, wird es als Standardwert für diese Kategorie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b8468-335">Furthermore, if a non-Microsoft program is available in a category, it is set as the default for that category.</span></span> <span data-ttu-id="b8468-336">Wenn in einer Kategorie mehr als ein nicht-Microsoft-Programm verfügbar ist, wird der Benutzer aufgefordert zu entscheiden, welches nicht-Microsoft-Programm als Standard verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8468-336">If more than one non-Microsoft program is available in a category, the user is asked to choose which non-Microsoft program should be used as the default.</span></span>
-   <span data-ttu-id="b8468-337">Richten Sie eine benutzerdefinierte Konfiguration ein.</span><span class="sxs-lookup"><span data-stu-id="b8468-337">Establish a custom configuration.</span></span> <span data-ttu-id="b8468-338">Benutzer nehmen Ihre eigene Auswahl vor, um den Zugriff zu aktivieren oder zu entfernen, und kombinieren Microsoft-und nicht-Microsoft-Programme, wenn Sie passen.</span><span class="sxs-lookup"><span data-stu-id="b8468-338">Users make their own selections for enabling or removing access, mixing Microsoft and non-Microsoft programs as they see fit.</span></span> <span data-ttu-id="b8468-339">Benutzer legen Standardoptionen auf kategoriebasis fest.</span><span class="sxs-lookup"><span data-stu-id="b8468-339">Users establish default options on a category-by-category basis.</span></span>

<span data-ttu-id="b8468-340">Benutzer können jede dieser Optionen jederzeit ändern.</span><span class="sxs-lookup"><span data-stu-id="b8468-340">Users are free to change any of these options at any time.</span></span>

### <a name="browser-registration-example"></a><span data-ttu-id="b8468-341">Beispiel für eine Browser Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-341">Browser Registration Example</span></span>

<span data-ttu-id="b8468-342">Das folgende Beispiel zeigt die vollständige **installinfo** -Registrierung für einen fiktiven beleuchteten Ansichts Browser.</span><span class="sxs-lookup"><span data-stu-id="b8468-342">The following example shows the full **InstallInfo** registration for a fictional Lit View browser.</span></span> <span data-ttu-id="b8468-343">In diesem Fall ermöglichen die Befehls Zeilenschalter, dass die Litview.exe Datei alle Aktionen ausführt, die für jeden Wert erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b8468-343">In this case the command line switches allow the Litview.exe file to perform whatever actions are necessary for each value.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="b8468-344">Beachten Sie, dass die Pfade in Anführungszeichen eingefügt werden, da Sie eingebettete Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8468-344">Note that quotation marks are placed around the paths because they contain embedded spaces.</span></span>

## <a name="registration-elements-for-specific-client-types"></a><span data-ttu-id="b8468-345">Registrierungs Elemente für bestimmte Client Typen</span><span class="sxs-lookup"><span data-stu-id="b8468-345">Registration Elements for Specific Client Types</span></span>

<span data-ttu-id="b8468-346">Die folgenden Informationen finden Sie auch in den Ressourcen, die im Abschnitt Verwandte Themen am Ende dieses Themas aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="b8468-346">The following information also can be found in the resources listed in the Related Topics section at the end of this topic.</span></span>

-   [<span data-ttu-id="b8468-347">Start Menü Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-347">Start Menu Registration</span></span>](#start-menu-registration)
-   [<span data-ttu-id="b8468-348">Mail Client Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-348">Mail Client Registration</span></span>](#mail-client-registration)

### <a name="start-menu-registration"></a><span data-ttu-id="b8468-349">Start Menü Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-349">Start Menu Registration</span></span>

<span data-ttu-id="b8468-350">Unter Windows XP haben Anwendungen normalerweise standardmäßig standardmäßig auf einem Computer weiten (**HKEY \_ local \_ Machine**) und nicht in einem Benutzerbereich (**Aktueller HKEY- \_ \_ Benutzer**) registriert.</span><span class="sxs-lookup"><span data-stu-id="b8468-350">Under Windows XP, applications typically registered defaults on a machine-wide (**HKEY\_LOCAL\_MACHINE**) rather than a user (**HKEY\_CURRENT\_USER**) scope.</span></span> <span data-ttu-id="b8468-351">Mit der Einführung der Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista müssen Anwendungen, die die **Internet** **-und e-Mail-** Slots im **Startmenü** beanspruchen, den Befehl "neu installieren" im richtigen Ausführungs Kontext implementieren.</span><span class="sxs-lookup"><span data-stu-id="b8468-351">With the Windows Vista introduction of the User Account Control (UAC), applications that claim the **Internet** and **E-mail** slots in the **Start** menu must implement the reinstall command within the correct execution context.</span></span>

> [!Note]  
> <span data-ttu-id="b8468-352">Der Link für den Startmenü **-e-Mail-** Link wurde ab Windows 7 entfernt.</span><span class="sxs-lookup"><span data-stu-id="b8468-352">The Start menu **E-mail** link has been removed as of Windows 7.</span></span> <span data-ttu-id="b8468-353">Die in diesem Abschnitt erörterte Registrierung sollte jedoch weiterhin ausgeführt werden, da Sie den standardmäßigen MAPI-Client zuweist.</span><span class="sxs-lookup"><span data-stu-id="b8468-353">However, the registration discussed in this section should still be performed because it assigns the default MAPI client.</span></span>

 

<span data-ttu-id="b8468-354">Ein eingeschränkter Benutzer unter Windows XP, Windows Vista oder Windows 7 kann nicht auf SPAD zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b8468-354">A limited user on Windows XP, Windows Vista, or Windows 7 cannot access SPAD.</span></span> <span data-ttu-id="b8468-355">Aus diesem Grund wird Entwicklern empfohlen, sich für das System Steuerungselement " **Standardprogramme festlegen** " zu registrieren, sodass jeder Benutzer Standard Anwendungs Standardwerte verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="b8468-355">For this reason, developers are encouraged to register for the **Set your default programs** Control Panel item so that any user can manage per-user application defaults.</span></span>

<span data-ttu-id="b8468-356">Die in SPAD vorgenommene Auswahl wirkt sich nur auf die computerspezifischen Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="b8468-356">Selections made in SPAD should only affect per-machine settings.</span></span>

<span data-ttu-id="b8468-357">Legen Sie den Registrierungs Wert wie folgt fest.</span><span class="sxs-lookup"><span data-stu-id="b8468-357">Set the registry value as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> <span data-ttu-id="b8468-358">**Die folgenden Informationen gelten nur für Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="b8468-358">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="b8468-359">Wenn die Registrierung des Standardwerts auf Computer Ebene unter HKEY \_ local \_ Machine, wie oben gezeigt, erfolgreich ist, sollte die Anwendung den Wert löschen, der dem Standardeintrag unter dem folgenden Unterschlüssel zugewiesen ist:</span><span class="sxs-lookup"><span data-stu-id="b8468-359">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the value assigned to the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> <span data-ttu-id="b8468-360">Wenn die Registrierung des Standardwerts auf Computer Ebene unter HKEY \_ local \_ Machine, wie oben gezeigt, fehlschlägt, in der Regel, weil der Benutzer nicht über Schreibberechtigungen für den Unterschlüssel verfügt, sollte die Anwendung den folgenden Wert festlegen:</span><span class="sxs-lookup"><span data-stu-id="b8468-360">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above fails, usually because the user does not have write permission to the subkey, the application should set the following value:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> <span data-ttu-id="b8468-361">Dadurch wird der kanonische Name nur für den aktuellen Benutzer registriert, nicht für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b8468-361">This registers the canonical name only for the current user, not for all users.</span></span>

 

<span data-ttu-id="b8468-362">Nach dem Aktualisieren der Registrierungsschlüssel sollte das Programm die [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht mit **wParam** = 0 und **LPARAM** übertragen, um das \\ \\ Betriebssystem zu benachrichtigen, dass sich der Standard Client geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b8468-362">After updating the registry keys, the program should broadcast the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with **wParam** = 0 and **lParam** pointing to the null-terminated string "Software\\Clients\\**ClientTypeName**" to notify the operating system that the default client has changed.</span></span>

### <a name="mail-client-registration"></a><span data-ttu-id="b8468-363">Mail Client Registrierung</span><span class="sxs-lookup"><span data-stu-id="b8468-363">Mail Client Registration</span></span>

<span data-ttu-id="b8468-364">Bei einem e-Mail-Client muss das Programm unter dem Stamm-mailto-Schlüssel der **HKEY- \_ Klassen \_** über registrierte Einstellungen verfügen, um \\  URLs zu verwenden, die das `mailto` Protokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8468-364">For a mail client, the program needs to have registered settings under the **HKEY\_CLASSES\_ROOT**\\**mailto** key in order to service URLs that use the `mailto` protocol.</span></span> <span data-ttu-id="b8468-365">Legen Sie Werte und Schlüssel fest, die diese Einstellungen unter dem folgenden Schlüssel widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="b8468-365">Set values and keys that mirror those settings under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

<span data-ttu-id="b8468-366">Diese Registrierungs Hierarchie ersetzt die vorhandene `mailto` Registrierungs Hierarchie, die unter **HKEY \_ Classes \_ root** \\ **mailto** gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="b8468-366">This registry hierarchy replaces the existing `mailto` registry hierarchy found at **HKEY\_CLASSES\_ROOT**\\**mailto**.</span></span> <span data-ttu-id="b8468-367">Die Hierarchie bleibt unverändert, nur der Speicherort wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="b8468-367">The hierarchy remains the same, only the location has changed.</span></span> <span data-ttu-id="b8468-368">Das Format dieser Hierarchie ist auf MSDN unter [asynchroner austauschbarer Protokoll Übersichten und Tutorials](/previous-versions//aa767913(v=vs.85))dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="b8468-368">The format of this hierarchy is documented on MSDN under [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)).</span></span> <span data-ttu-id="b8468-369">In der Regel `mailto` wird das Protokoll für ein Programm und nicht für ein asynchrones Protokoll registriert. in diesem Fall gilt die Dokumentation zum [Registrieren einer Anwendung in einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8468-369">Typically, the `mailto` protocol is registered to a program rather than an asynchronous protocol, in which case the documentation on [Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) applies.</span></span>

<span data-ttu-id="b8468-370">Das folgende Beispiel zeigt den `mailto` Abschnitt der Registrierung für einen `mailto` Handler, der für ein Programm registriert ist.</span><span class="sxs-lookup"><span data-stu-id="b8468-370">The following example shows the `mailto` section of the registration for a `mailto` handler registered to a program.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

<span data-ttu-id="b8468-371">Der EditFlags-Registrierungs Wert ist in den [Dateitypen](fa-file-types.md) im Abschnitt "Definieren von Dateityp Attributen" dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="b8468-371">The EditFlags registry value is documented in [File Types](fa-file-types.md) in the section titled "Defining File Type Attributes."</span></span>

## <a name="complete-sample-registrations"></a><span data-ttu-id="b8468-372">Vervollständigen von Beispiel Registrierungen</span><span class="sxs-lookup"><span data-stu-id="b8468-372">Complete Sample Registrations</span></span>

<span data-ttu-id="b8468-373">In den folgenden Beispielen werden die kompletten Registrierungsanforderungen für die verschiedenen Client Typen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b8468-373">The following examples are provided to show the complete registration requirements for the various client types.</span></span>

-   [<span data-ttu-id="b8468-374">Ein Beispiel Browser</span><span class="sxs-lookup"><span data-stu-id="b8468-374">A Sample Browser</span></span>](#a-sample-browser)
-   [<span data-ttu-id="b8468-375">Beispiel-e-Mail-Browser</span><span class="sxs-lookup"><span data-stu-id="b8468-375">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
-   [<span data-ttu-id="b8468-376">Ein Beispiel Media Player</span><span class="sxs-lookup"><span data-stu-id="b8468-376">A Sample Media Player</span></span>](#a-sample-media-player)
-   [<span data-ttu-id="b8468-377">Ein Instant Messenger-Beispielprogramm</span><span class="sxs-lookup"><span data-stu-id="b8468-377">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
-   [<span data-ttu-id="b8468-378">Ein Beispiel für einen virtuellen Computer für Java</span><span class="sxs-lookup"><span data-stu-id="b8468-378">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a><span data-ttu-id="b8468-379">Ein Beispiel Browser</span><span class="sxs-lookup"><span data-stu-id="b8468-379">A Sample Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a><span data-ttu-id="b8468-380">Beispiel-e-Mail-Browser</span><span class="sxs-lookup"><span data-stu-id="b8468-380">A Sample Mail Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a><span data-ttu-id="b8468-381">Ein Beispiel Media Player</span><span class="sxs-lookup"><span data-stu-id="b8468-381">A Sample Media Player</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a><span data-ttu-id="b8468-382">Ein Instant Messenger-Beispielprogramm</span><span class="sxs-lookup"><span data-stu-id="b8468-382">A Sample Instant Messenger Program</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a><span data-ttu-id="b8468-383">Ein Beispiel für einen virtuellen Computer für Java</span><span class="sxs-lookup"><span data-stu-id="b8468-383">A Sample Virtual Machine for Java</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="b8468-384">*Die hier dargestellten Beispiel Unternehmen, Organisationen, Produkte, Domänen Namen, e-Mail-Adressen, Logos, Personen, Orte und Ereignisse sind frei erfunden. Keine Zuordnung zu echten Unternehmen, Organisationen, Produkten, Domänen Namen, e-Mail-Adressen, Logos, Personen, stellen oder Ereignissen ist beabsichtigt oder sollte abgeleitet werden.*</span><span class="sxs-lookup"><span data-stu-id="b8468-384">*The example companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted herein are fictitious. No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.*</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8468-385">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8468-385">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8468-386">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="b8468-386">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="b8468-387">Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü</span><span class="sxs-lookup"><span data-stu-id="b8468-387">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
</dt> <dt>

<span data-ttu-id="b8468-388">[Internet Explorer-Client Registrierungs Layout (siehe Abschnitt "Definitionen von Client Registrierungs Schlüsseln")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8468-388">[Internet Explorer Client Registry Layout (see the "Client Registry Key Definitions" section)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b8468-389">[Asynchrone austauschbare Protokoll Übersichten und Tutorials](/previous-versions//aa767913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8468-389">[Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b8468-390">[Registrieren einer Anwendung in einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8468-390">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>
</dt> </dl>

 

 
