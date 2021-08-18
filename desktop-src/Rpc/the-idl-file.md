---
title: Die IDL-Datei
description: Die IDL-Datei besteht aus einer oder mehreren Schnittstellendefinitionen, von denen jede über einen Header und einen Text verfügt.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f46a92fe5967dca1faeca1d658cf398fb0baf6ebd9160c3a736747de324e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924414"
---
# <a name="the-idl-file"></a>Die IDL-Datei

Die IDL-Datei besteht aus einer oder mehreren Schnittstellendefinitionen, von denen jede über einen Header und einen Text verfügt. Der -Header enthält Informationen, die für die gesamte Schnittstelle gelten, z. B. die UUID. Diese Informationen sind in eckige Klammern eingeschlossen, gefolgt von der Schlüsselwortschnittstelle **und** dem Schnittstellennamen. Der Text enthält Datentypdefinitionen und Funktionsprototypen im C-Stil, ergänzt um Attribute, die beschreiben, wie die Daten über das Netzwerk übertragen werden.

In diesem Beispiel enthält der Schnittstellenheader nur die UUID und die Versionsnummer. Die Versionsnummer stellt sicher, dass bei mehreren Versionen einer RPC-Schnittstelle nur kompatible Versionen des Clients und Servers verbunden werden.

Der Schnittstellenkörper enthält den Funktionsprototyp für **HelloProc**. In diesem Prototyp enthält der Funktionsparameter pszString die Attribute **\[** [**in und die**](/windows/desktop/Midl/in) **\]** **\[** [**Zeichenfolge**](/windows/desktop/Midl/string) **\]** . Das **\[ attribut in \]** teilt der Laufzeitbibliothek mit, dass der Parameter nur vom Client an den Server übergeben wird. Das **\[ \] Zeichenfolgenattribut** gibt an, dass der Stub den Parameter als Zeichenfolge im C-Stil behandeln soll.

Die Clientanwendung sollte die Serveranwendung herunterfahren können, daher enthält die Schnittstelle einen Prototyp für eine andere Remotefunktion,**Shutdown** , die später in diesem Tutorial implementiert wird.

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 