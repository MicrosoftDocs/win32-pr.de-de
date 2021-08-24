---
title: Nachteile
description: Nachteile
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b9d41a632c202a25c3383ffb2d1069505c0dc988651e9fc886cfeecca5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501114"
---
# <a name="disadvantages"></a>Nachteile

Prozessin-Process-Server bieten den Vorteil der Geschwindigkeit und Größe eines Objekthandlers mit der Bearbeitungsfunktion eines lokalen Servers. Warum würden Sie sich also jemals dafür entscheiden, Ihre OLE-Anwendung als lokalen Server und nicht als Prozessserver zu implementieren? Es gibt mehrere Gründe:

-   Sicherheit. Nur auf einem lokalen Server ist der Adressraum von dem des Clients isoliert. Ein Prozessserver teilt den Adressraum und den Prozesskontext des Clients und kann daher bei Fehlern oder böswilliger Programmierung weniger robust sein.
-   Granularität. Ein lokaler Server kann mehrere Instanzen seines Objekts auf vielen verschiedenen Clients hosten und den Serverzustand zwischen Objekten auf mehreren Clients auf eine Weise freigeben, die schwierig oder unmöglich wäre, wenn er als Prozessserver implementiert wird, bei dem es sich einfach um eine dll handelt, die in jeden Client geladen wird.
-   Kompatibilität. Wenn Sie sich für die Implementierung eines In-Process-Servers entscheiden, geben Sie die Kompatibilität mit OLE 1 auf, die solche Server nicht unterstützt. Dies ist für viele Entwickler kein Aspekt, aber wenn dies der Fall ist, ist dies von entscheidender Bedeutung.
-   Unfähigkeit, Links zu unterstützen. Ein Prozessserver kann nicht als Linkquelle dienen. Da eine DLL nicht allein ausgeführt werden kann, kann sie kein Dateiobjekt erstellen, mit dem verknüpft werden soll.

Trotz dieser Nachteile kann ein In-Process-Server eine hervorragende Wahl für seine Geschwindigkeit und Größe sein – wenn er all Ihre anderen Anforderungen erfüllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorteile](advantages.md)
</dt> <dt>

[In-Process-Server](in-process-servers.md)
</dt> </dl>

 

 




