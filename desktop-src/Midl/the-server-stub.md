---
title: Der Serverstub
description: Der Serverstub stellt Ersatzeinstiegspunkte auf dem Server für jeden der in der Eingabe-IDL-Datei definierten Vorgänge bereit.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL-Compiler MIDL, MIDL und RPC MIDL, Schnittstellen, Serverstub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfc940ebbd90e4e028ce96dc3b5c47eb15179d41cfbd064cd235e87192822f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559900"
---
# <a name="the-server-stub"></a>Der Serverstub

Der Serverstub stellt Ersatzeinstiegspunkte auf dem Server für jeden der in der Eingabe-IDL-Datei definierten Vorgänge bereit.

Wenn eine Serverstubroutine von der RPC-Laufzeitbibliothek aufgerufen wird, führt sie die folgenden Funktionen aus:

-   Entmarshalseingabeargumente (entpackt die Argumente aus ihren übertragenen Formaten).
-   Ruft die tatsächliche Implementierung der Prozedur auf dem Server auf.
-   Marshallt Ausgabeargumente (packt die Argumente in die übertragenen Formulare).

Die MIDL-Compilerschalter [**/server,**](-server.md) [**/sstub**](-sstub.md)und [**/out**](-out.md) wirken sich auf die Serverstubdatei aus.

 

 




