---
title: Der Serverstub
description: Der Serverstub stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Einstiegspunkte auf dem Server bereit.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- Mittel l-compilermittell, Mittel l-und RPC-Mittell, Schnittstellen, Serverstub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037396"
---
# <a name="the-server-stub"></a>Der Serverstub

Der Serverstub stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Einstiegspunkte auf dem Server bereit.

Wenn eine Server-Stub-Routine von der RPC-Lauf Zeit Bibliothek aufgerufen wird, führt Sie die folgenden Funktionen aus:

-   Entfernt Eingabeargumente (entpackt die Argumente aus ihren übertragenen Formaten).
-   Ruft die tatsächliche Implementierung der Prozedur auf dem Server auf.
-   Marsheit Ausgabe Argumente (verpackt die Argumente in die übertragenen Formulare).

Der-Compilerschalter [**/Server**](-server.md), [**/sstub**](-sstub.md)und [**/out**](-out.md) wirkt sich auf die Server-Stub-Datei aus.

 

 




