---
title: Der Clientstub
description: Das Clientstubmodul stellt Ersatzeinstiegspunkte auf dem Client für jeden der in der Eingabe-IDL-Datei definierten Vorgänge bereit.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL und RPC MIDL, Schnittstellen, Clientstub
- Schnittstellen MIDL
- Schnittstellen MIDL, MIDL und RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c718f0910c2e6834c93409b6d8cd4969e3d2bbe9c53c65821dc0fe0eb19ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146223"
---
# <a name="the-client-stub"></a>Der Clientstub

Das Clientstubmodul stellt Ersatzeinstiegspunkte auf dem Client für jeden der in der Eingabe-IDL-Datei definierten Vorgänge bereit.

Wenn die Clientanwendung die Remoteprozedur aufruft, wird der Aufruf zuerst an die Ersatzroutine in der Clientstubdatei durchgeführt. Die Clientstubroutine führt die folgenden Funktionen aus:

-   Marshallt Argumente. Der Clientstub verpackt Eingabeargumente in ein Formular, das an den Server übertragen werden kann.
-   Ruft die Clientlaufzeitbibliothek auf, um Argumente an den Remoteadressraum zu übertragen, und ruft die Remoteprozedur im Serveradressraum auf.
-   Unmarshals-Ausgabeargumente. Der Clientstub entpackt Ausgabeargumente und kehrt zum Aufrufer zurück.

Die MIDL-Compilerschalter [**/client,**](-client.md) [**/cstub**](-cstub.md)und [**/out**](-out.md) wirken sich auf die Clientstubdatei aus.

 

 




