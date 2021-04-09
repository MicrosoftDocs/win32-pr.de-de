---
description: Für Benutzer auf der ganzen Welt ist die Texteingabe Teil eines modernen Computer Erlebnisses, für Blogs, Kommentare, Tweets, Instant Messaging oder andere Arten von Texteingaben. In Windows 8 ist die Rechtschreibprüfung integriert, um Steuerelemente zu bearbeiten.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Informationen zur Rechtschreibprüfungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866375"
---
# <a name="about-the-spell-checking-api"></a><span data-ttu-id="dcf90-104">Informationen zur Rechtschreibprüfungs-API</span><span class="sxs-lookup"><span data-stu-id="dcf90-104">About the Spell Checking API</span></span>

<span data-ttu-id="dcf90-105">Für Benutzer auf der ganzen Welt ist die Texteingabe Teil eines modernen Computer Erlebnisses, für Blogs, Kommentare, Tweets, Instant Messaging oder andere Arten von Texteingaben.</span><span class="sxs-lookup"><span data-stu-id="dcf90-105">For users worldwide, textual input is part of a modern computing experience, for blogging, commenting, tweeting, instant messaging, or any other kind of text typing.</span></span> <span data-ttu-id="dcf90-106">In Windows 8 ist die Rechtschreibprüfung integriert, um Steuerelemente zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="dcf90-106">In Windows 8, spell checking is built-in to edit controls.</span></span>

<span data-ttu-id="dcf90-107">Entwickler können die Rechtschreibprüfungs-API in ihren Apps verwenden, um verfügbare Rechtschreib Überprüfungs Dienste zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="dcf90-107">Developers can use the spell checking API in their apps to consume available spell checking services.</span></span> <span data-ttu-id="dcf90-108">Entwickler können auch Rechtschreibprüfungen erstellen, die zu Anbietern werden und in das Windows-Rechtschreib Prüfungs Framework integriert sind.</span><span class="sxs-lookup"><span data-stu-id="dcf90-108">Developers can also create spell checkers that become providers and are integrated into the Windows spell checking framework.</span></span>

<span data-ttu-id="dcf90-109">Die Rechtschreibprüfungs-API ist für die Verwendung durch professionelle C/C++-Entwickler von Windows Component Object Model-Apps (com) konzipiert.</span><span class="sxs-lookup"><span data-stu-id="dcf90-109">The Spell Checking API is designed for use by professional C/C++ developers of Windows Component Object Model (COM) apps.</span></span> <span data-ttu-id="dcf90-110">Die Rechtschreibprüfungs-API wird nicht für die Verwendung in einem Windows-oder ASP.net-Dienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcf90-110">The Spell Checking API is not supported for use in a Windows or ASP.NET service.</span></span>

## <a name="versioning"></a><span data-ttu-id="dcf90-111">Versionskontrolle</span><span class="sxs-lookup"><span data-stu-id="dcf90-111">Versioning</span></span>

<span data-ttu-id="dcf90-112">Die Rechtschreibprüfungs-API ist ab Windows 8 oder Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dcf90-112">The Spell Checking API is available beginning with the Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="dcf90-113">Zukünftige Ergänzungen der API werden durch das Erstellen neuer Schnittstellen behandelt, die mithilfe von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf den vorhandenen festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="dcf90-113">Future additions to the API will be handled by creating new interfaces that can be determined using [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the existing ones.</span></span>

## <a name="interfaces"></a><span data-ttu-id="dcf90-114">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dcf90-114">Interfaces</span></span>

<span data-ttu-id="dcf90-115">Alle Schnittstellen müssen freigegeben werden, wenn Sie nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcf90-115">All interfaces must be released when they are no longer used.</span></span> <span data-ttu-id="dcf90-116">Alle zurückgegebenen **LPWSTR** -Zeichen folgen (und **lpolestr** -Elemente aus [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) müssen mit " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " freigegeben werden, wenn Sie nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcf90-116">All returned (out parameter) **LPWSTR** strings (and **LPOLESTR** items from [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) must be released with [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when no longer used.</span></span>

## <a name="error-handling"></a><span data-ttu-id="dcf90-117">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="dcf90-117">Error handling</span></span>

<span data-ttu-id="dcf90-118">Fehler werden als **HRESULT** s zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dcf90-118">Errors are returned as **HRESULT** s.</span></span> <span data-ttu-id="dcf90-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) und [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) werden in dieser API nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcf90-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) and [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) are not supported in this API.</span></span> <span data-ttu-id="dcf90-120">Fehler können mit Ausnahme falscher Argumente nicht besonders handlungsfähig sein.</span><span class="sxs-lookup"><span data-stu-id="dcf90-120">Errors are not particularly actionable except for incorrect arguments.</span></span>

<span data-ttu-id="dcf90-121">Standard-RPC-Fehlercodes können von jedem API-Aufruf zurückgegeben werden, da Sie außerhalb des Prozesses sind.</span><span class="sxs-lookup"><span data-stu-id="dcf90-121">Standard RPC error codes may be returned by any of the API calls because they are out-of-proc.</span></span> <span data-ttu-id="dcf90-122">Es gelten Standard-RPC-Timeouts.</span><span class="sxs-lookup"><span data-stu-id="dcf90-122">Standard RPC timeouts apply.</span></span>

## <a name="security"></a><span data-ttu-id="dcf90-123">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="dcf90-123">Security</span></span>

<span data-ttu-id="dcf90-124">Die Rechtschreibprüfungs-API lädt möglicherweise externen Code (Rechtschreibprüfung-Anbieter).</span><span class="sxs-lookup"><span data-stu-id="dcf90-124">The Spell Checking API may load external code (spell check providers).</span></span> <span data-ttu-id="dcf90-125">Dieser Code wird außerhalb der proc-Prozedur und in einem eingeschränkten Sicherheitskontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcf90-125">It will run this code out-of-proc and under a restricted security context.</span></span>

## <a name="dictionary-files"></a><span data-ttu-id="dcf90-126">Wörterbuchdateien</span><span class="sxs-lookup"><span data-stu-id="dcf90-126">Dictionary files</span></span>

<span data-ttu-id="dcf90-127">Die benutzerspezifischen Wörterbücher für eine Sprache, die den Inhalt der hinzugefügten, ausgeschlossenen und automatisch korrekten Wortlisten enthalten, befinden sich unter% APPDATA% \\ Microsoft \\ Spelling \\ *<language tag>* .</span><span class="sxs-lookup"><span data-stu-id="dcf90-127">The user-specific dictionaries for a language, which hold the content for the Added, Excluded, and AutoCorrect word lists, are located under %AppData%\\Microsoft\\Spelling\\*<language tag>*.</span></span> <span data-ttu-id="dcf90-128">Die Dateinamen sind Default. dic (Added), Default. exc (ausgeschlossen) und default. ACL (AutoCorrect).</span><span class="sxs-lookup"><span data-stu-id="dcf90-128">The filenames are default.dic (Added), default.exc (Excluded) and default.acl (AutoCorrect).</span></span> <span data-ttu-id="dcf90-129">Die Dateien sind UTF-16-Le-Klartext, das mit der entsprechenden Byte Reihenfolge Markierung (BOM) beginnen muss.</span><span class="sxs-lookup"><span data-stu-id="dcf90-129">The files are UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM).</span></span> <span data-ttu-id="dcf90-130">Jede Zeile enthält ein Wort (in der Liste hinzugefügter und ausgeschlossener Wörter) oder ein Auto korrektes Paar mit den Wörtern, die durch einen senkrechten Strich (" \| ") getrennt sind (in der Liste der AutoKorrektur-Wörter).</span><span class="sxs-lookup"><span data-stu-id="dcf90-130">Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("\|") (in the AutoCorrect word list).</span></span> <span data-ttu-id="dcf90-131">Andere im Verzeichnis vorhandene. dic-, EXC-und ACL-Dateien werden vom Rechtschreib Überprüfungs Dienst erkannt und den Benutzer Wortlisten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dcf90-131">Other .dic, .exc, and .acl files present in the directory will be detected by the spell checking service and added to the user word lists.</span></span> <span data-ttu-id="dcf90-132">Diese Dateien gelten als schreibgeschützt und werden nicht durch die Rechtschreibprüfungs-API geändert.</span><span class="sxs-lookup"><span data-stu-id="dcf90-132">These files are considered to be read-only and are not modified by the spell checking API.</span></span>

## <a name="installing-a-spell-checking-provider"></a><span data-ttu-id="dcf90-133">Installieren eines Rechtschreib Prüfungs Anbieters</span><span class="sxs-lookup"><span data-stu-id="dcf90-133">Installing a spell checking provider</span></span>

<span data-ttu-id="dcf90-134">Bei der Installation eines Rechtschreib Prüfungs Anbieters müssen alle verwendeten Dateien an einem Speicherort abgelegt werden, der Lesezugriff auf die sid ([Sicherheits](../secauthz/security-identifiers.md)-ID) "alle Anwendungspakete" zulässt.</span><span class="sxs-lookup"><span data-stu-id="dcf90-134">The installation of a spell checking provider must place all the files it uses in a location that allows read access from the SID ([security identifier](../secauthz/security-identifiers.md)) "ALL APPLICATION PACKAGES".</span></span> <span data-ttu-id="dcf90-135">Die Installation in einem Ordner unter "Programmdateien" funktioniert gut.</span><span class="sxs-lookup"><span data-stu-id="dcf90-135">Installing it in a folder under "Program Files" works well.</span></span> <span data-ttu-id="dcf90-136">Außerdem muss der Anbieter einige Schlüssel in der Registrierung festlegen, damit er für die Rechtschreibprüfungs-API angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dcf90-136">Also, the provider must set some keys in the registry for it to appear to the spell checking API.</span></span> <span data-ttu-id="dcf90-137">Dies kann entweder in der HKEY \_ Current User-Struktur \_ oder in der HKEY \_ Local Machine Hive erfolgen, \_ je nachdem, ob Sie nur für den aktuellen Benutzer oder für alle Benutzer installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dcf90-137">It can be in either the HKEY\_CURRENT\_USER hive or the HKEY\_LOCAL\_MACHINE hive depending on whether it should install only for the current user or all users.</span></span>


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



<span data-ttu-id="dcf90-138">Das Beispiel für den [Rechtschreib Prüfungs Anbieter](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) enthält ein Beispiel für die Registrierung, die zum Installieren eines Anbieters erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dcf90-138">The [spell checking provider sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) provides an example of the registration needed to install a provider.</span></span>

<span data-ttu-id="dcf90-139">Wenn Sie neue Optionen für die Rechtschreibprüfung für einen Rechtschreibprüfungs-Anbieter erstellen, finden Sie unter [**ioptiondescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) Hinweise zum benennen.</span><span class="sxs-lookup"><span data-stu-id="dcf90-139">If you are creating new spell checking options for a spell checking provider, see [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) for guidance on naming.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcf90-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dcf90-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcf90-141">API-Referenz zur Rechtschreibprüfung</span><span class="sxs-lookup"><span data-stu-id="dcf90-141">Spell Checking API Reference</span></span>](spell-checker-api-reference.md)
</dt> <dt>

[<span data-ttu-id="dcf90-142">Beispiel für Rechtschreibprüfung (Client)</span><span class="sxs-lookup"><span data-stu-id="dcf90-142">Spell checking client sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[<span data-ttu-id="dcf90-143">Beispiel für Rechtschreib Prüfungs Anbieter</span><span class="sxs-lookup"><span data-stu-id="dcf90-143">Spell checking provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[<span data-ttu-id="dcf90-144">**Ioptiondescription:: ID**</span><span class="sxs-lookup"><span data-stu-id="dcf90-144">**IOptionDescription::Id**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[<span data-ttu-id="dcf90-145">**IEnumString**</span><span class="sxs-lookup"><span data-stu-id="dcf90-145">**IEnumString**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

<span data-ttu-id="dcf90-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="dcf90-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> </dl>

 

 
