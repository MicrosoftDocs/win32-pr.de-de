---
description: Eine Regel Zeichenfolge für die Schutz Deskriptoren enthält eine sequenzielle Liste mit mindestens einer Schutzvorrichtung.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Schutz Deskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11814df2af5bd9abee4260f4aadab5bb74c77a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215556"
---
# <a name="protection-descriptors"></a><span data-ttu-id="a814f-103">Schutz Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="a814f-103">Protection Descriptors</span></span>

<span data-ttu-id="a814f-104">Eine Regel Zeichenfolge für die Schutz Deskriptoren enthält eine sequenzielle Liste mit mindestens einer Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="a814f-104">A protection descriptor rule string contains a sequential list of one or more protectors.</span></span> <span data-ttu-id="a814f-105">Es muss mindestens eine Schutzvorrichtung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a814f-105">There must be at least one protector.</span></span> <span data-ttu-id="a814f-106">Wenn mehr als eine vorhanden ist, müssen die Schutzvorrichtungen in der Zeichenfolge durch **and** oder **or** getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="a814f-106">If there is more than one, the protectors must be separated in the string by **AND** or **OR**.</span></span> <span data-ttu-id="a814f-107">Diese Werte müssen in Großbuchstaben geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a814f-107">These values must be capitalized.</span></span> <span data-ttu-id="a814f-108">Die folgende Syntax zeigt das Zeichen folgen Format eines Schutz Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="a814f-108">The following syntax shows the string format of a protection descriptor.</span></span>


```C++
Descriptor = [ Protector-or
              *( OR-separator Protector-or ) ]

    Protector-or = Protector-and
              *( AND-separator Protector-and )

    OR-separator = "OR"
    AND-separator = "AND"

    Protector-and = providerName EQUALS providerAttributes

    providerName = descr

    providerAttribute = string | hexstring

      ; The following characters are to be escaped when they appear
      ; in the value to be encoded: ESC, one of <escaped>, leading
      ; SHARP or SPACE, trailing SPACE, and NULL.
      string =   [ ( leadchar / pair ) [ *( stringchar / pair )
         ( trailchar / pair ) ] ]

      leadchar = LUTF1 / UTFMB
      LUTF1 = %x01-1F / %x21 / %x24-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      trailchar  = TUTF1 / UTFMB
      TUTF1 = %x01-1F / %x21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      stringchar = SUTF1 / UTFMB
      SUTF1 = %x01-21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      pair = ESC ( ESC / special / hexpair )
      special = escaped / SPACE / SHARP / EQUALS
      escaped = DQUOTE / PLUS / COMMA / SEMI / LANGLE / RANGLE
      hexstring = SHARP 1*hexpair
      hexpair = HEX HEX

      descr   = leadkeychar *keychar
      leadkeychar = ALPHA
      keychar = ALPHA / DIGIT / HYPHEN
      number  = DIGIT / ( LDIGIT 1*DIGIT )

      ALPHA   = %x41-5A / %x61-7A   ; "A"-"Z" / "a"-"z"
      DIGIT   = %x30 / LDIGIT       ; "0"-"9"
      LDIGIT  = %x31-39             ; "1"-"9"
      HEX     = DIGIT / %x41-46 / %x61-66 ; "0"-"9" / "A"-"F" / "a"-"f"

      NULL    = %x00 ; null (0)
      SPACE   = %x20 ; space (" ")
      DQUOTE  = %x22 ; quote (""")
      SHARP   = %x23 ; octothorpe (or sharp sign) ("#")
      DOLLAR  = %x24 ; dollar sign ("$")
      SQUOTE  = %x27 ; single quote ("'")
      LPAREN  = %x28 ; left paren ("(")
      RPAREN  = %x29 ; right paren (")")
      PLUS    = %x2B ; plus sign ("+")
      COMMA   = %x2C ; comma (",")
      HYPHEN  = %x2D ; hyphen ("-")
      DOT     = %x2E ; period (".")
      SEMI    = %x3B ; semicolon (";")
      LANGLE  = %x3C ; left angle bracket ("<")
      EQUALS  = %x3D ; equals sign ("=")
      RANGLE  = %x3E ; right angle bracket (">")
      ESC     = %x5C ; backslash ("\")
      USCORE  = %x5F ; underscore ("_")
      LCURLY  = %x7B ; left curly brace "{"
      RCURLY  = %x7D ; right curly brace "}"

      ; Any UTF-8 [RFC3629] encoded Unicode [Unicode] character
      UTF8    = UTF1 / UTFMB
      UTFMB   = UTF2 / UTF3 / UTF4
      UTF0    = %x80-BF
      UTF1    = %x00-7F
      UTF2    = %xC2-DF UTF0
      UTF3    = %xE0 %xA0-BF UTF0 / %xE1-EC 2(UTF0) /
                %xED %x80-9F UTF0 / %xEE-EF 2(UTF0)
      UTF4    = %xF0 %x90-BF 2(UTF0) / %xF1-F3 3(UTF0) /
                %xF4 %x80-8F 2(UTF0)

      OCTET   = %x00-FF ; Any octet (8-bit data unit)
```



<span data-ttu-id="a814f-109">Schutz Deskriptoren können derzeit für die folgenden Autorisierungs Typen definiert werden:</span><span class="sxs-lookup"><span data-stu-id="a814f-109">Protection descriptors can currently be defined for the following types of authorization:</span></span>

-   <span data-ttu-id="a814f-110">Eine Gruppe in einer Active Directory Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="a814f-110">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="a814f-111">Ein Satz von webanmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="a814f-111">A set of web credentials.</span></span>
-   <span data-ttu-id="a814f-112">Ein Zertifikat im Zertifikat Speicher des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a814f-112">A certificate in the user's certificate store.</span></span>

<span data-ttu-id="a814f-113">Beispiele für Schutz Deskriptor-Regel Zeichenfolgen für eine Active Directory Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a814f-113">Examples of protection descriptor rule strings for an Active Directory group include the following:</span></span>

-   <span data-ttu-id="a814f-114">"Sid = s-1-5-21-4392301 und sid = s-1-5-21-3101812"</span><span class="sxs-lookup"><span data-stu-id="a814f-114">"SID=S-1-5-21-4392301 AND SID=S-1-5-21-3101812"</span></span>
-   <span data-ttu-id="a814f-115">"SDDL = o:s-1-5-5-0-290724g: Syd: (A;; CCDC;;; S-1-5-5-0-290724) (A;;D C;;; WD) "</span><span class="sxs-lookup"><span data-stu-id="a814f-115">"SDDL=O:S-1-5-5-0-290724G:SYD:(A;;CCDC;;;S-1-5-5-0-290724)(A;;DC;;;WD)"</span></span>
-   <span data-ttu-id="a814f-116">"Local = User"</span><span class="sxs-lookup"><span data-stu-id="a814f-116">"LOCAL=user"</span></span>
-   <span data-ttu-id="a814f-117">"Local = Machine"</span><span class="sxs-lookup"><span data-stu-id="a814f-117">"LOCAL=machine"</span></span>

<span data-ttu-id="a814f-118">Beispiele für Schutz Deskriptor-Regel Zeichenfolgen für eine Gruppe von webanmelde Informationen:</span><span class="sxs-lookup"><span data-stu-id="a814f-118">Examples of protection descriptor rule strings for a set of web credentials include the following:</span></span>

-   <span data-ttu-id="a814f-119">"Webanmelde Informationen = mypasswordname"</span><span class="sxs-lookup"><span data-stu-id="a814f-119">"WEBCREDENTIALS=MyPasswordName"</span></span>
-   <span data-ttu-id="a814f-120">"Webanmelde Informationen = mypasswordname, myweb. com"</span><span class="sxs-lookup"><span data-stu-id="a814f-120">"WEBCREDENTIALS=MyPasswordName,myweb.com"</span></span>

<span data-ttu-id="a814f-121">Beispiele für Schutz Deskriptor-Regel Zeichenfolgen für ein Zertifikat:</span><span class="sxs-lookup"><span data-stu-id="a814f-121">Examples of protection descriptor rule strings for a certificate include the following:</span></span>

-   <span data-ttu-id="a814f-122">"Certificate = Hashid: SHA1- \_ Hash \_ des \_ Zertifikats"</span><span class="sxs-lookup"><span data-stu-id="a814f-122">"CERTIFICATE=HashID:sha1\_hash\_of\_certificate"</span></span>
-   <span data-ttu-id="a814f-123">"Certificate = certblob: base64String"</span><span class="sxs-lookup"><span data-stu-id="a814f-123">"CERTIFICATE=CertBlob:base64String"</span></span>

<span data-ttu-id="a814f-124">Der von Ihnen angegebene Schutz Deskriptor bestimmt automatisch, welcher Schlüsselschutz Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a814f-124">The protection descriptor you specify automatically determines which key protection provider is used.</span></span> <span data-ttu-id="a814f-125">Weitere Informationen finden Sie unter [Schutz Anbieter](protection-providers.md).</span><span class="sxs-lookup"><span data-stu-id="a814f-125">For more information, see [Protection Providers](protection-providers.md).</span></span>

<span data-ttu-id="a814f-126">Beachten Sie, dass auf der linken Seite des Gleichheitszeichens (=) **sid**, **SDDL**, **local**, **webanmelde** Informationen oder **Zertifikat** vorliegen muss.</span><span class="sxs-lookup"><span data-stu-id="a814f-126">Note that the left side of the equals sign (=) must be **SID**, **SDDL**, **LOCAL**, **WEBCREDENTIALS**, or **CERTIFICATE**.</span></span> <span data-ttu-id="a814f-127">Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="a814f-127">These values are not case sensitive.</span></span>

<span data-ttu-id="a814f-128">Wenn Sie die [**ncryptkreateschutzdescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) -Funktion aufrufen, müssen Sie eine Regel Zeichenfolge (oder einen anzeigen Amen, der einer Regel Zeichenfolge zugeordnet ist) angeben.</span><span class="sxs-lookup"><span data-stu-id="a814f-128">You must specify a rule string (or a display name associated with a rule string) when you call the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function.</span></span> <span data-ttu-id="a814f-129">Da die Verwendung von Schutz Deskriptoren-Regel Zeichenfolgen etwas umständlich ist, können Sie einen anzeigen Amen mit der Regel Zeichenfolge verknüpfen und beides mithilfe der [**ncryptregisterschutzdescriptorname**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) -Funktion registrieren.</span><span class="sxs-lookup"><span data-stu-id="a814f-129">Alternatively, because protection descriptor rule strings are somewhat cumbersome to use and remember, you can associate a display name with the rule string and register both by using the [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) function.</span></span> <span data-ttu-id="a814f-130">Anschließend können Sie den anzeigen Amen in **ncryptkreateschutzdescriptor** verwenden.</span><span class="sxs-lookup"><span data-stu-id="a814f-130">Then you can use the display name in **NCryptCreateProtectionDescriptor**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a814f-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a814f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a814f-132">CNG-DPAPI</span><span class="sxs-lookup"><span data-stu-id="a814f-132">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="a814f-133">Schutz Anbieter</span><span class="sxs-lookup"><span data-stu-id="a814f-133">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



