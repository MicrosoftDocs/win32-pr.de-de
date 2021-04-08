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
# <a name="the-acf-body"></a>Der ACF-Text

Der ACF-Text enthält Konfigurations Attribute, die auf Typen und Funktionen angewendet werden, die im Schnittstellen Text der IDL-Datei definiert sind. Der ACF-Textkörper kann leer sein oder die ACF-Attribute [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), Function und Parameter enthalten. Alle diese Elemente sind optional. Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben Attribute im ACF-Header.

Die ACF gibt das Verhalten auf dem lokalen Computer an und wirkt sich nicht auf die Daten aus, die über das Netzwerk übertragen werden. Es wird verwendet, um Details zu einem zu generierenden Stub anzugeben. Im DCE-Kompatibilitätsmodus ([**/OSF**](/windows/desktop/Midl/-osf)) wirkt sich die ACF nicht auf die Interaktion zwischen Stubs aus, sondern zwischen dem Stub-und dem Anwendungscode.

Ein in der ACF angegebener Parameter muss einer der in der IDL-Datei angegebenen Parameter sein. Die Reihenfolge der Spezifikation des Parameters in der ACF ist nicht signifikant, da die Übereinstimmung nach Name und nicht nach Position erfolgt. Die Parameterliste in der ACF kann leer sein, auch wenn die Parameterliste in der entsprechenden IDL-Signatur nicht ist (Dies wird jedoch nicht empfohlen). Abstrakte Deklaratoren (unbenannte Parameter) in der IDL-Datei bewirken, dass der Mittell-Compiler während der Verarbeitung der ACF Fehler meldet, da der Parameter nicht gefunden wurde.

Die ACF **include** -Direktive gibt die Header Dateien an, die im generierten Header als Teil einer standardmäßigen C- **präprozessorinclude \#** -Anweisung angezeigt werden. Das ACF- **Schlüsselwort** unterscheidet sich von einer **\# include** -Direktive. Das ACF-Schlüsselwort **include** bewirkt, dass die Zeile "**\# include** *filename*" in der generierten Header Datei angezeigt wird, während die C-sprach Direktive "**\# include** *filename*" bewirkt, dass der Inhalt der Datei in der ACF platziert wird.

Mit der ACF- [**typedef**](/windows/desktop/Midl/typedef) -Anweisung können Sie ACF-Typattribute auf Typen anwenden, die zuvor in der IDL-Datei definiert wurden. Die Syntax der ACF- **typedef** unterscheidet sich von der C- **typedef** -Syntax.

Mit den ACF-Funktions Attributen können Sie Attribute angeben, die für die Funktion als Ganzes gelten. Weitere Informationen finden Sie unter **\[** [**Code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimieren**](/windows/desktop/Midl/optimize) **\]** und **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** .

Mit den ACF-Parameter Attributen können Sie Attribute angeben, die für einzelne Parameter der Funktion gelten. Weitere Informationen finden Sie unter **\[** [**Byte \_ Anzahl**](/windows/desktop/Midl/byte-count) **\]** .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**/APP- \_ Konfiguration**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[Automatisches \_ handle\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[Ordnung\]**](../midl/code.md)
</dt> <dt>

[**\[explizites \_ handle\]**](../midl/explicit-handle.md)
</dt> <dt>

[Die IDL-Datei (Interface Definition Language)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[implizites \_ handle\]**](../midl/implicit-handle.md)
</dt> <dt>

[**darunter**](/windows/desktop/Midl/include)
</dt> <dt>

[MIDL](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[NoCode\]**](../midl/nocode.md)
</dt> <dt>

[**\[optimiert\]**](../midl/optimize.md)
</dt> <dt>

[**\[Darstellung \_ als\]**](../midl/represent-as.md)
</dt> <dt>

[**typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 