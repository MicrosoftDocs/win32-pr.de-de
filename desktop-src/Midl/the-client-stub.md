---
title: Der Clientstub
description: Das Client-Stub-Modul stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Punkte auf dem Client bereit.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- Mittel l und RPC-Mittell, Schnittstellen, Clientstub
- Schnittstellen-Mittell
- Schnittstellen, Mittel l, Mittel l und RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310728"
---
# <a name="the-client-stub"></a>Der Clientstub

Das Client-Stub-Modul stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Punkte auf dem Client bereit.

Wenn die Client Anwendung eine Remote Prozedur aufruft, wird der zugehörige-Befehl zuerst an die Ersatz Routine in der Client-Stub-Datei weitergeleitet. Die Client-Stub-Routine führt die folgenden Funktionen aus:

-   Marshalls-Argumente. Der Client-Stub verpackt Eingabeargumente in ein Formular, das an den Server übermittelt werden kann.
-   Ruft die Client Lauf Zeit Bibliothek auf, um Argumente an den Remote Adressraum zu übertragen, und ruft die Remote Prozedur im Server Adressbereich auf.
-   Gibt Ausgabe Argumente aus. Der Client-Stub entpackt Ausgabe Argumente und kehrt zum Aufrufer zurück.

Der-Compilerschalter [**/Client**](-client.md), [**/cstub**](-cstub.md)und [**/out**](-out.md) wirkt sich auf die Client-Stub-Datei aus.

 

 




