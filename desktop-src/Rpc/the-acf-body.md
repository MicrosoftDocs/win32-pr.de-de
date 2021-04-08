---
title: Der ACF-Text
description: Der ACF-Text enthält Konfigurations Attribute, die auf Typen und Funktionen angewendet werden, die im Schnittstellen Text der IDL-Datei definiert sind.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104039755"
---
# <a name="the-acf-body"></a><span data-ttu-id="2ed0b-103">Der ACF-Text</span><span class="sxs-lookup"><span data-stu-id="2ed0b-103">The ACF Body</span></span>

<span data-ttu-id="2ed0b-104">Der ACF-Text enthält Konfigurations Attribute, die auf Typen und Funktionen angewendet werden, die im Schnittstellen Text der IDL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-104">The ACF body contains configuration attributes that apply to types and functions defined in the interface body of the IDL file.</span></span> <span data-ttu-id="2ed0b-105">Der ACF-Textkörper kann leer sein oder die ACF-Attribute [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), Function und Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-105">The body of the ACF can be empty or it can contain ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), function, and parameter attributes.</span></span> <span data-ttu-id="2ed0b-106">Alle diese Elemente sind optional.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-106">All of these items are optional.</span></span> <span data-ttu-id="2ed0b-107">Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben Attribute im ACF-Header.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-107">Attributes applied to individual types and functions in the ACF body override attributes in the ACF header.</span></span>

<span data-ttu-id="2ed0b-108">Die ACF gibt das Verhalten auf dem lokalen Computer an und wirkt sich nicht auf die Daten aus, die über das Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-108">The ACF specifies behavior on the local computer and does not affect the data transmitted over the network.</span></span> <span data-ttu-id="2ed0b-109">Es wird verwendet, um Details zu einem zu generierenden Stub anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-109">It is used to specify details of a stub to be generated.</span></span> <span data-ttu-id="2ed0b-110">Im DCE-Kompatibilitätsmodus ([**/OSF**](/windows/desktop/Midl/-osf)) wirkt sich die ACF nicht auf die Interaktion zwischen Stubs aus, sondern zwischen dem Stub-und dem Anwendungscode.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-110">In DCE-compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), the ACF does not affect interaction between stubs, but between the stub and application code.</span></span>

<span data-ttu-id="2ed0b-111">Ein in der ACF angegebener Parameter muss einer der in der IDL-Datei angegebenen Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-111">A parameter specified in the ACF must be one of the parameters specified in the IDL file.</span></span> <span data-ttu-id="2ed0b-112">Die Reihenfolge der Spezifikation des Parameters in der ACF ist nicht signifikant, da die Übereinstimmung nach Name und nicht nach Position erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-112">The order of specification of the parameter in the ACF is not significant because the matching is by name, not by position.</span></span> <span data-ttu-id="2ed0b-113">Die Parameterliste in der ACF kann leer sein, auch wenn die Parameterliste in der entsprechenden IDL-Signatur nicht ist (Dies wird jedoch nicht empfohlen).</span><span class="sxs-lookup"><span data-stu-id="2ed0b-113">The parameter list in the ACF can be empty, even when the parameter list in the corresponding IDL signature is not (but this is not recommended).</span></span> <span data-ttu-id="2ed0b-114">Abstrakte Deklaratoren (unbenannte Parameter) in der IDL-Datei bewirken, dass der Mittell-Compiler während der Verarbeitung der ACF Fehler meldet, da der Parameter nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-114">Abstract declarators (unnamed parameters) in the IDL file cause the MIDL compiler to report errors while processing the ACF because the parameter is not found.</span></span>

<span data-ttu-id="2ed0b-115">Die ACF **include** -Direktive gibt die Header Dateien an, die im generierten Header als Teil einer standardmäßigen C- **präprozessorinclude \#** -Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-115">The ACF **include** directive specifies the header files to appear in the generated header as part of a standard C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="2ed0b-116">Das ACF- **Schlüsselwort** unterscheidet sich von einer **\# include** -Direktive.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-116">The ACF keyword **include** differs from an **\#include** directive.</span></span> <span data-ttu-id="2ed0b-117">Das ACF-Schlüsselwort **include** bewirkt, dass die Zeile "**\# include** *filename*" in der generierten Header Datei angezeigt wird, während die C-sprach Direktive "**\# include** *filename*" bewirkt, dass der Inhalt der Datei in der ACF platziert wird.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-117">The ACF keyword **include** causes the line "**\#include** *filename*" to appear in the generated header file, while the C-language directive "**\#include** *filename*" causes the contents of that file to be placed in the ACF.</span></span>

<span data-ttu-id="2ed0b-118">Mit der ACF- [**typedef**](/windows/desktop/Midl/typedef) -Anweisung können Sie ACF-Typattribute auf Typen anwenden, die zuvor in der IDL-Datei definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-118">The ACF [**typedef**](/windows/desktop/Midl/typedef) statement lets you apply ACF type attributes to types previously defined in the IDL file.</span></span> <span data-ttu-id="2ed0b-119">Die Syntax der ACF- **typedef** unterscheidet sich von der C- **typedef** -Syntax.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-119">The ACF **typedef** syntax differs from the C **typedef** syntax.</span></span>

<span data-ttu-id="2ed0b-120">Mit den ACF-Funktions Attributen können Sie Attribute angeben, die für die Funktion als Ganzes gelten.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-120">The ACF function attributes let you specify attributes that apply to the function as a whole.</span></span> <span data-ttu-id="2ed0b-121">Weitere Informationen finden Sie unter **\[** [**Code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimieren**](/windows/desktop/Midl/optimize) **\]** und **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2ed0b-121">For more information, see **\[**[**code**](/windows/desktop/Midl/code)**\]**, **\[**[**optimize**](/windows/desktop/Midl/optimize)**\]**, and **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]**.</span></span>

<span data-ttu-id="2ed0b-122">Mit den ACF-Parameter Attributen können Sie Attribute angeben, die für einzelne Parameter der Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-122">The ACF parameter attributes let you specify attributes that apply to individual parameters of the function.</span></span> <span data-ttu-id="2ed0b-123">Weitere Informationen finden Sie unter **\[** [**Byte \_ Anzahl**](/windows/desktop/Midl/byte-count) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2ed0b-123">For more information, see **\[**[**byte\_count**](/windows/desktop/Midl/byte-count)**\]**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ed0b-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ed0b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed0b-125">**/APP- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="2ed0b-125">**/app\_config**</span></span>](/windows/desktop/Midl/-app-config)
</dt> <dt>

[<span data-ttu-id="2ed0b-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="2ed0b-126">**/osf**</span></span>](/windows/desktop/Midl/-osf)
</dt> <dt>

<span data-ttu-id="2ed0b-127">[**\[Automatisches \_ handle\]**](../midl/auto-handle.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-127">[**\[auto\_handle\]**](../midl/auto-handle.md)</span></span>
</dt> <dt>

<span data-ttu-id="2ed0b-128">[**\[Ordnung\]**](../midl/code.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-128">[**\[code\]**](../midl/code.md)</span></span>
</dt> <dt>

<span data-ttu-id="2ed0b-129">[**\[explizites \_ handle\]**](../midl/explicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-129">[**\[explicit\_handle\]**](../midl/explicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2ed0b-130">Die IDL-Datei (Interface Definition Language)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-130">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
</dt> <dt>

<span data-ttu-id="2ed0b-131">[**\[implizites \_ handle\]**](../midl/implicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-131">[**\[implicit\_handle\]**](../midl/implicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2ed0b-132">**darunter**</span><span class="sxs-lookup"><span data-stu-id="2ed0b-132">**include**</span></span>](/windows/desktop/Midl/include)
</dt> <dt>

[<span data-ttu-id="2ed0b-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="2ed0b-133">midl</span></span>](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

<span data-ttu-id="2ed0b-134">[**\[NoCode\]**](../midl/nocode.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-134">[**\[nocode\]**](../midl/nocode.md)</span></span>
</dt> <dt>

<span data-ttu-id="2ed0b-135">[**\[optimiert\]**](../midl/optimize.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-135">[**\[optimize\]**](../midl/optimize.md)</span></span>
</dt> <dt>

<span data-ttu-id="2ed0b-136">[**\[Darstellung \_ als\]**](../midl/represent-as.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-136">[**\[represent\_as\]**](../midl/represent-as.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2ed0b-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="2ed0b-137">**typedef**</span></span>](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 