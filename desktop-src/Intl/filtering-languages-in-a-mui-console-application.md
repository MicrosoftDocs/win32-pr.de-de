---
description: Eine MUI-Konsolenanwendung kann entweder Systemeinstellungen oder anwendungsspezifische Einstellungen für die Sprachen der Benutzeroberfläche unterstützen. In diesem Thema wird das Filtern von Sprachen für diese Art von Anwendung erläutert.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtern von Sprachen in einer MUI-Konsolenanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865503"
---
# <a name="filtering-languages-in-a-mui-console-application"></a><span data-ttu-id="670ed-104">Filtern von Sprachen in einer MUI-Konsolenanwendung</span><span class="sxs-lookup"><span data-stu-id="670ed-104">Filtering Languages in a MUI Console Application</span></span>

<span data-ttu-id="670ed-105">Eine MUI-Konsolenanwendung kann entweder Systemeinstellungen oder anwendungsspezifische Einstellungen für die Sprachen der Benutzeroberfläche unterstützen.</span><span class="sxs-lookup"><span data-stu-id="670ed-105">A MUI console application can support either system settings or application-specific settings for its user interface languages.</span></span> <span data-ttu-id="670ed-106">In diesem Thema wird das Filtern von Sprachen für diese Art von Anwendung erläutert.</span><span class="sxs-lookup"><span data-stu-id="670ed-106">This topic discusses the filtering of languages for this type of application.</span></span>

## <a name="limit-the-languages-to-display"></a><span data-ttu-id="670ed-107">Einschränken der anzuzeigenden Sprachen</span><span class="sxs-lookup"><span data-stu-id="670ed-107">Limit the Languages to Display</span></span>

<span data-ttu-id="670ed-108">Anders als bei einem grafischen Fenster können in der Windows-Konsole [komplexe Skripts](uniscribe-glossary.md)wie Arabisch, Hebräisch, Persian, Hindi, Urdu, Thai und viele andere nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="670ed-108">Unlike a graphical window, the Windows console cannot display [complex scripts](uniscribe-glossary.md), such as Arabic, Hebrew, Persian, Hindi, Urdu, Thai, and many others.</span></span> <span data-ttu-id="670ed-109">Daher können viele Benutzeroberflächen Sprachen unter keinen Umständen von der Konsole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="670ed-109">Therefore, many user interface languages cannot be displayed by the console under any circumstances.</span></span>

<span data-ttu-id="670ed-110">In der Konsole können nur Zeichen von der einzelnen [OEM-Codepage](code-pages.md) angezeigt werden, die der aktuellen Sprache für nicht-Unicode-Anwendungen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="670ed-110">The console can display only characters from the single [OEM code page](code-pages.md) associated with the current language for non-Unicode applications.</span></span> <span data-ttu-id="670ed-111">Für jede OEM-Codepage wird von der Konsole eine bestimmte Schriftart verwendet, und dies kann keine vollständige Abdeckung für diese Codepage bieten.</span><span class="sxs-lookup"><span data-stu-id="670ed-111">For each OEM code page, the console uses a particular font, and this might not provide full coverage for that code page.</span></span>

<span data-ttu-id="670ed-112">In diesen Konsolen bezogenen Einschränkungen wird die Anzahl der Benutzeroberflächen Sprachen reduziert, die von der-Konsole auf einem bestimmten Computer angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="670ed-112">These console-related limitations reduce the number of user interface languages that the console can display on a particular computer.</span></span> <span data-ttu-id="670ed-113">Wenn z. b. die aktuelle Sprache für nicht-Unicode-Anwendungen Japanisch ist und der Benutzer versucht, deutschen Text in der Konsole anzuzeigen, werden Zeichen mit Umschlag Zeichen nicht ordnungsgemäß angezeigt.</span><span class="sxs-lookup"><span data-stu-id="670ed-113">For example, if the current language for non-Unicode applications is Japanese and the user tries to display German text in the console, characters with umlauts do not display correctly.</span></span> <span data-ttu-id="670ed-114">Wenn die aktuelle Sprache für nicht-Unicode-Anwendungen Deutsch ist und der Benutzer japanischen Text in der-Konsole anzeigen möchte, sind die Ergebnisse weitaus schlechter, und der Text wird fast unverständlich.</span><span class="sxs-lookup"><span data-stu-id="670ed-114">If the current language for non-Unicode applications is German and the user wants to display Japanese text in the console, the results are much worse, rendering the text almost incomprehensible.</span></span>

> [!Note]  
> <span data-ttu-id="670ed-115">Beachten Sie beim Bereitstellen von Konsolen Unterstützung für Ihre MUI-Anwendungen, dass die Konsole nur eingeschränkte Unterstützung für [Eingabemethoden-Editoren](input-method-manager.md)bietet.</span><span class="sxs-lookup"><span data-stu-id="670ed-115">When providing console support for your MUI applications, remember that the console provides only limited support for [input method editors](input-method-manager.md).</span></span>

 

## <a name="set-the-language-for-console-output"></a><span data-ttu-id="670ed-116">Festlegen der Sprache für die Konsolenausgabe</span><span class="sxs-lookup"><span data-stu-id="670ed-116">Set the Language for Console Output</span></span>

<span data-ttu-id="670ed-117">Unter Windows Vista und höher legt eine Konsolenanwendung die Sprache fest, damit die Konsolen Anzeige durch Aufrufen von [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="670ed-117">On Windows Vista and later, a console application sets the language to support the console display by calling [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="670ed-118">In diesem Befehl übergibt die Anwendung den MUI \_ \_ -Konsolen Filter im *dwFlags* -Parameter und **null** für *pwszlanguagesbuffer*.</span><span class="sxs-lookup"><span data-stu-id="670ed-118">In this call, the application passes MUI\_CONSOLE\_FILTER in the *dwFlags* parameter and **NULL** for *pwszLanguagesBuffer*.</span></span> <span data-ttu-id="670ed-119">Eine Alternative besteht darin, [**setthreaduilanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) mit dem sprach Bezeichner 0 (null) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="670ed-119">An alternative is to call [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span> <span data-ttu-id="670ed-120">Diese Einstellung bewirkt, dass die Funktion die Sprache auswählt, die die Konsolen Anzeige am besten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="670ed-120">This setting causes the function to select the language that best supports the console display.</span></span>

<span data-ttu-id="670ed-121">Unter Windows XP kann die Anwendung nur die Sprache für die Konsolenausgabe festlegen, indem [**setthreaduilanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) mit dem sprach Bezeichner 0 (null) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="670ed-121">On Windows XP, the application can only set the language for console output by calling [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="670ed-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="670ed-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="670ed-123">Festlegen der Einstellungen für die Anwendungs Sprache</span><span class="sxs-lookup"><span data-stu-id="670ed-123">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> </dl>

 

 
