---
description: Abrufen und Festlegen von Gebiets Schema Informationen
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Abrufen und Festlegen von Gebiets Schema Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346300"
---
# <a name="retrieving-and-setting-locale-information"></a><span data-ttu-id="28983-103">Abrufen und Festlegen von Gebiets Schema Informationen</span><span class="sxs-lookup"><span data-stu-id="28983-103">Retrieving and Setting Locale Information</span></span>

<span data-ttu-id="28983-104">Die Anwendung muss in der Lage sein, bestimmte Informationen zu verfügbaren Gebiets Schemata [und Sprachen](locales-and-languages.md)abzurufen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="28983-104">The application must be able to retrieve and set specific information about available [locales and languages](locales-and-languages.md).</span></span> <span data-ttu-id="28983-105">Jedes Element von Gebiets Schema Informationen, z. b. der Name eines bestimmten Wochentags oder das Zeichen, das als Dezimaltrennzeichen verwendet wird, verfügt über eine entsprechende Konstante.</span><span class="sxs-lookup"><span data-stu-id="28983-105">Each element of locale information, such as the name of a particular day of the week or the character used as a decimal separator, has a corresponding constant.</span></span> <span data-ttu-id="28983-106">Die verfügbaren Konstanten werden in den Gebiets Schema [Informations Konstanten](locale-information-constants.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="28983-106">The available constants are defined in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="28983-107">Die Gebiets Schema Informationen werden von Ihrer Anwendung immer als eine mit NULL endenden Zeichenfolge gespeichert und manipuliert.</span><span class="sxs-lookup"><span data-stu-id="28983-107">Your application always stores and manipulates locale information as a null-terminated string.</span></span> <span data-ttu-id="28983-108">Binäre Daten sind nicht zulässig, und alle numerischen Werte müssen als Text angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="28983-108">No binary data is allowed, and any numeric values must be specified as text.</span></span> <span data-ttu-id="28983-109">Jede Art von Informationen hat ein bestimmtes Format.</span><span class="sxs-lookup"><span data-stu-id="28983-109">Each type of information has a particular format.</span></span> <span data-ttu-id="28983-110">Außerdem werden mehrere Typen miteinander verknüpft, sodass durch das Ändern eines Typs auch der Wert des anderen Typs geändert wird.</span><span class="sxs-lookup"><span data-stu-id="28983-110">Also, several types are linked together so that changing one type changes the value of the other type as well.</span></span>

<span data-ttu-id="28983-111">Zum Abrufen von Gebiets Schema Informationen Ruft die Anwendung [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) mit der Konstante auf, die den erforderlichen Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="28983-111">To retrieve locale information, the application calls [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with the constant that corresponds to the required information.</span></span> <span data-ttu-id="28983-112">Die Anwendung kann [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) aufrufen, um ein Element mit Gebiets Schema Informationen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="28983-112">The application can call [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) to set an item of locale information.</span></span>

> [!Note]  
> <span data-ttu-id="28983-113">Obwohl ein Gebiets Schema [Bezeichner](locale-identifiers.md) unterstützt werden kann, ist er nicht für die Verwendung durch eine Anwendung verfügbar, es sei denn, das entsprechende Gebiets Schema ist ebenfalls installiert.</span><span class="sxs-lookup"><span data-stu-id="28983-113">Although a [locale identifier](locale-identifiers.md) might be supported, it is not available for use by an application unless the corresponding locale is also installed.</span></span>

 

<span data-ttu-id="28983-114">Da die meisten Gebiets Schema Informations Konstanten sich gegenseitig ausschließen, kann jeweils nur ein Typ von Informationen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="28983-114">Since most locale information constants are mutually exclusive, only one type of information can be handled at a time.</span></span> <span data-ttu-id="28983-115">Die Ausnahmen für diese Regel sind [locale \_ \_ \_ ACP](locale-use-cp-acp.md), locale [ \_ Return \_ Number](locale-return-constants.md)und [locale \_ nouseroverride](locale-nouseroverride.md), die mit anderen Konstanten kombiniert werden können, die eine Binärdatei oder verwenden.</span><span class="sxs-lookup"><span data-stu-id="28983-115">The exceptions to this rule are [LOCALE\_USE\_CP\_ACP](locale-use-cp-acp.md), [LOCALE\_RETURN\_NUMBER](locale-return-constants.md), and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md), which can be combined with other constants using a binary OR.</span></span>

> [!Caution]  
> <span data-ttu-id="28983-116">Es wird dringend davon abgeraten, Gebiets Schema \_ nominserüberschreibung zu verwenden, da die Benutzereinstellungen deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="28983-116">Use of LOCALE\_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</span></span>

 

<span data-ttu-id="28983-117">Wie eine Reihe von Anwendungen, z. b. Microsoft Active Directory, kann Ihre Anwendung ihre Zeichen folgen in einer sortierbaren Datenbank beibehalten.</span><span class="sxs-lookup"><span data-stu-id="28983-117">Like a number of applications, for example Microsoft Active Directory, your application can maintain its strings in a sortable database.</span></span> <span data-ttu-id="28983-118">Weitere Informationen finden Sie unter [Handling Sortieren in Ihren Anwendungen](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="28983-118">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28983-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28983-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28983-120">Verwenden der Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="28983-120">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="28983-121">Gebiets Schema Informations Konstanten</span><span class="sxs-lookup"><span data-stu-id="28983-121">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="28983-122">Behandeln von Sortierungen in Ihren Anwendungen</span><span class="sxs-lookup"><span data-stu-id="28983-122">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="28983-123">Arbeiten mit benutzerdefinierten Gebiets Schemas</span><span class="sxs-lookup"><span data-stu-id="28983-123">Working with Custom Locales</span></span>](working-with-custom-locales.md)
</dt> </dl>

 

 



