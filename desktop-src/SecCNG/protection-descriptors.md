---
description: Eine Schutzbeschreibungsregelzeichenfolge enthält eine sequenzielle Liste mit mindestens einer Schutzvorrichtung.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Schutzdeskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99d4ec8de08ad2f657d2b3ac1992ce6e399ede277f8fde3e12f0732571b01a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907252"
---
# <a name="protection-descriptors"></a>Schutzdeskriptoren

Eine Schutzbeschreibungsregelzeichenfolge enthält eine sequenzielle Liste mit mindestens einer Schutzvorrichtung. Es muss mindestens eine Schutzvorrichtung geben. Wenn es mehrere gibt, müssen die Schutzvorrichtungen in der Zeichenfolge durch **AND** oder **OR getrennt werden.** Diese Werte müssen groß sein. Die folgende Syntax zeigt das Zeichenfolgenformat eines Schutzdeskriptors.


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



Schutzdeskriptoren können derzeit für die folgenden Autorisierungstypen definiert werden:

-   Eine Gruppe in einer Active Directory-Gesamtstruktur.
-   Ein Satz von Webanmeldeinformationen.
-   Ein Zertifikat im Zertifikatspeicher des Benutzers.

Beispiele für Schutzdeskriptor-Regelzeichenfolgen für eine Active Directory-Gruppe sind:

-   "SID=S-1-5-21-4392301 AND SID=S-1-5-21-3101812"
-   "SDDL=O:S-1-5-5-0-290724G:SYD:(A;; CCDC;;; S-1-5-5-0-290724)(A;;D C;;; WD)"
-   "LOCAL=user"
-   "LOCAL=machine"

Beispiele für Schutzdeskriptor-Regelzeichenfolgen für einen Satz von Webanmeldeinformationen sind:

-   "WEBCREDENTIALS=MyPasswordName"
-   "WEBCREDENTIALS=MyPasswordName,myweb.com"

Beispiele für Schutzdeskriptor-Regelzeichenfolgen für ein Zertifikat sind:

-   "CERTIFICATE=HashID:sha1 \_ hash \_ of \_ certificate"
-   "CERTIFICATE=CertBlob:base64String"

Der von Ihnen angegebenen Schutzdeskriptor bestimmt automatisch, welcher Schlüsselschutzanbieter verwendet wird. Weitere Informationen finden Sie unter [Schutzanbieter.](protection-providers.md)

Beachten Sie, dass die linke Seite des Gleichheitszeichens (=) **SID,** **SDDL,** **LOCAL,** **WEBCREDENTIALS** oder **CERTIFICATE sein muss.** Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Sie müssen eine Regelzeichenfolge (oder einen Anzeigenamen, der einer Regelzeichenfolge zugeordnet ist) angeben, wenn Sie die [**NCryptCreateProtectionDescriptor-Funktion**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) aufrufen. Alternativ können Sie der Regelzeichenfolge einen Anzeigenamen zuordnen und beides mithilfe der [**NCryptRegisterProtectionDescriptorName-Funktion**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) registrieren, da die Verwendung und Merken von Schutzdeskriptor-Regelzeichenfolgen etwas umständlich ist. Anschließend können Sie den Anzeigenamen in **NCryptCreateProtectionDescriptor verwenden.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Schutzanbieter](protection-providers.md)
</dt> </dl>

 

 



