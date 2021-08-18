---
title: Der ACF-Text
description: Der ACF-Text enthält Konfigurationsattribute, die für Typen und Funktionen gelten, die im Schnittstellentext der IDL-Datei definiert sind.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1446b4f0e14849832766bc512a95d0ae0aeb249cebd814314b617ffa1e1125e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924620"
---
# <a name="the-acf-body"></a>Der ACF-Text

Der ACF-Text enthält Konfigurationsattribute, die für Typen und Funktionen gelten, die im Schnittstellentext der IDL-Datei definiert sind. Der Textkörper des ACF kann leer sein, oder er kann [**ACF-Attribute,**](/windows/desktop/Midl/include) [**typedef,**](/windows/desktop/Midl/typedef)function und parameter enthalten. Alle diese Elemente sind optional. Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben Attribute im ACF-Header.

Der ACF gibt das Verhalten auf dem lokalen Computer an und wirkt sich nicht auf die über das Netzwerk übertragenen Daten aus. Es wird verwendet, um Details eines zu generierenden Stubs anzugeben. Im DCE-Kompatibilitätsmodus ([**/osf**](/windows/desktop/Midl/-osf)) wirkt sich der ACF nicht auf die Interaktion zwischen Stubs, sondern zwischen dem Stub und dem Anwendungscode aus.

Ein im ACF angegebener Parameter muss einer der in der IDL-Datei angegebenen Parameter sein. Die Reihenfolge der Spezifikation des Parameters im ACF ist nicht von Bedeutung, da der Abgleich nach Name und nicht nach Position erfolgt. Die Parameterliste im ACF kann leer sein, auch wenn die Parameterliste in der entsprechenden IDL-Signatur nicht ist (dies wird jedoch nicht empfohlen). Abstrakte Deklaratoren (unbenannte Parameter) in der IDL-Datei bewirken, dass der MIDL-Compiler Fehler während der Verarbeitung des ACF meldet, da der Parameter nicht gefunden wird.

Die ACF **include-Direktive** gibt die Headerdateien an, die im generierten Header als Teil einer standardmäßigen C-Präprozessor-Include-Anweisung angezeigt werden sollen. **\#** Das ACF-Schlüsselwort **include** unterscheidet sich von einer **\# include-Anweisung.** Das ACF-Schlüsselwort **include** bewirkt, dass die Zeile "**\# include** *filename*" in der generierten Headerdatei angezeigt wird, während die C-Sprachdirektive "**\# include** *filename*" bewirkt, dass der Inhalt dieser Datei im ACF platziert wird.

Mit der [**TypeDef-Anweisung**](/windows/desktop/Midl/typedef) von ACF können Sie ACF-Typattribute auf Typen anwenden, die zuvor in der IDL-Datei definiert wurden. Die **ACF-Typdefinitionssyntax** unterscheidet sich von der **C-Typedef-Syntax.**

Mit den ACF-Funktionsattributen können Sie Attribute angeben, die für die gesamte Funktion gelten. Weitere Informationen finden Sie unter **\[** [**code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimize**](/windows/desktop/Midl/optimize) **\]** und **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** .

Mit den ACF-Parameterattributen können Sie Attribute angeben, die für einzelne Parameter der Funktion gelten. Weitere Informationen finden Sie unter **\[** [**\_ Byteanzahl.**](/windows/desktop/Midl/byte-count) **\]**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_/app-Konfiguration**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[Automatisches \_ Handle\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[Code\]**](../midl/code.md)
</dt> <dt>

[**\[Explizites \_ Handle\]**](../midl/explicit-handle.md)
</dt> <dt>

[Die IDL-Datei (Interface Definition Language)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[Implizites \_ Handle\]**](../midl/implicit-handle.md)
</dt> <dt>

[**include**](/windows/desktop/Midl/include)
</dt> <dt>

[Midl](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[nocode\]**](../midl/nocode.md)
</dt> <dt>

[**\[Optimieren\]**](../midl/optimize.md)
</dt> <dt>

[**\[darstellen \_ als\]**](../midl/represent-as.md)
</dt> <dt>

[**Typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 