---
title: Die IDL-Datei
description: Die IDL-Datei besteht aus einer oder mehreren Schnittstellendefinitionen, die jeweils über einen Header und einen Text verfügen.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473293"
---
# <a name="the-idl-file"></a>Die IDL-Datei

Die IDL-Datei besteht aus einer oder mehreren Schnittstellendefinitionen, die jeweils über einen Header und einen Text verfügen. Der-Header enthält Informationen, die für die gesamte Schnittstelle gelten, z. b. die UUID. Diese Informationen werden in eckige Klammern eingeschlossen, gefolgt von der-Schlüsselwort **Schnittstelle** und dem Schnittstellennamen. Der Text enthält Datentyp Definitionen im C-Stil und Funktionsprototypen, ergänzt mit Attributen, die beschreiben, wie die Daten über das Netzwerk übertragen werden.

In diesem Beispiel enthält der Schnittstellen Header nur die UUID und die Versionsnummer. Durch die Versionsnummer wird sichergestellt, dass bei mehreren Versionen einer RPC-Schnittstelle nur kompatible Versionen des Clients und des Servers verbunden werden.

Der Schnittstellen Text enthält den Funktionsprototyp für **helloproc**. In diesem Prototyp weist der Funktionsparameter pszstring die Attribute **\[** [**in**](/windows/desktop/Midl/in) **\]** und der **\[** [**Zeichenfolge**](/windows/desktop/Midl/string)auf **\]** . Das **\[ in \]** -Attribut teilt der Lauf Zeit Bibliothek mit, dass der-Parameter nur vom Client an den Server übergeben wird. Das **\[ String \]** -Attribut gibt an, dass der Stub den-Parameter als Zeichenfolge im C-Format behandeln soll.

Die Client Anwendung sollte die Serveranwendung Herunterfahren können, sodass die-Schnittstelle einen Prototyp für eine andere Remote Funktion,**herunter** fahren, enthält, die später in diesem Tutorial implementiert wird.

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

 

 