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
# <a name="protection-descriptors"></a>Schutz Deskriptoren

Eine Regel Zeichenfolge für die Schutz Deskriptoren enthält eine sequenzielle Liste mit mindestens einer Schutzvorrichtung. Es muss mindestens eine Schutzvorrichtung vorhanden sein. Wenn mehr als eine vorhanden ist, müssen die Schutzvorrichtungen in der Zeichenfolge durch **and** oder **or** getrennt werden. Diese Werte müssen in Großbuchstaben geschrieben werden. Die folgende Syntax zeigt das Zeichen folgen Format eines Schutz Deskriptors.


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



Schutz Deskriptoren können derzeit für die folgenden Autorisierungs Typen definiert werden:

-   Eine Gruppe in einer Active Directory Gesamtstruktur.
-   Ein Satz von webanmelde Informationen.
-   Ein Zertifikat im Zertifikat Speicher des Benutzers.

Beispiele für Schutz Deskriptor-Regel Zeichenfolgen für eine Active Directory Gruppe:

-   "Sid = s-1-5-21-4392301 und sid = s-1-5-21-3101812"
-   "SDDL = o:s-1-5-5-0-290724g: Syd: (A;; CCDC;;; S-1-5-5-0-290724) (A;;D C;;; WD) "
-   "Local = User"
-   "Local = Machine"

Beispiele für Schutz Deskriptor-Regel Zeichenfolgen für eine Gruppe von webanmelde Informationen:

-   "Webanmelde Informationen = mypasswordname"
-   "Webanmelde Informationen = mypasswordname, myweb. com"

Beispiele für Schutz Deskriptor-Regel Zeichenfolgen für ein Zertifikat:

-   "Certificate = Hashid: SHA1- \_ Hash \_ des \_ Zertifikats"
-   "Certificate = certblob: base64String"

Der von Ihnen angegebene Schutz Deskriptor bestimmt automatisch, welcher Schlüsselschutz Anbieter verwendet wird. Weitere Informationen finden Sie unter [Schutz Anbieter](protection-providers.md).

Beachten Sie, dass auf der linken Seite des Gleichheitszeichens (=) **sid**, **SDDL**, **local**, **webanmelde** Informationen oder **Zertifikat** vorliegen muss. Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Wenn Sie die [**ncryptkreateschutzdescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) -Funktion aufrufen, müssen Sie eine Regel Zeichenfolge (oder einen anzeigen Amen, der einer Regel Zeichenfolge zugeordnet ist) angeben. Da die Verwendung von Schutz Deskriptoren-Regel Zeichenfolgen etwas umständlich ist, können Sie einen anzeigen Amen mit der Regel Zeichenfolge verknüpfen und beides mithilfe der [**ncryptregisterschutzdescriptorname**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) -Funktion registrieren. Anschließend können Sie den anzeigen Amen in **ncryptkreateschutzdescriptor** verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CNG-DPAPI](cng-dpapi.md)
</dt> <dt>

[Schutz Anbieter](protection-providers.md)
</dt> </dl>

 

 



