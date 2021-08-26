---
title: Versionsthematik für RPC und COM
description: Versionierungsthematik für RPC (Remote Procedure Call) und COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- Remoteprozeduraufruf RPC , bewährte Methoden, Versionszuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3681ce1290b7653c28b12c09c93d21de3052e0e6137ed5c6f906afd42f8d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016380"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>Versionsthematik für RPC und COM

Nur zwei vollständig närrische Methoden unterstützen neue Funktionen ohne Risiko von Kabelkompatibilitätsproblemen:

-   Ändern Sie die Schnittstellenversion gemäß den Regeln. dadurch wird verhindert, dass neue Clients mit einem alten Server kommunizieren, und ein alter Client kann die Kommunikation mit dem neuen Server verhindern. Dies wird weiter unten in diesem Abschnitt erläutert.
-   Führen Sie eine andere Schnittstelle ein, die mit der neuen Funktionalität zu tun hat.

Eine RPC-Standardschnittstelle wird durch eine Kombination aus GUID und Versionsnummer identifiziert. eine COM-Schnittstelle wird durch ihre GUID identifiziert. Die Version besteht aus Haupt- und Nebenteilen. Bei Standardschnittstellen mit derselben GUID und unterschiedlichen Versionsnummern ist eine Verbindung nur möglich, wenn die Hauptversion identisch ist und der Client nicht höher als die Nebenversion des Servers ist.

Dies hat zur Folge, dass das Ändern der RPC-Schnittstellen-GUID die Wire-Kompatibilität unterbricht, während das Ändern des Schnittstellennamens nicht erfolgt.

In RPC Standard ist ein Pfad für Upgrades und Erweiterungen klar definiert und erfordert im Grunde, dass neue Methoden nur am Ende der Schnittstelle hinzugefügt werden und neue Typen nur in den neuen Methoden verwendet werden. Wenn solche Ergänzungen erforderlich sind, muss die Nebenversion erhöht werden. Jede andere Änderung erfordert eine Änderung der Hauptversion, da die Client- und Serversoftware im Kabel nicht kompatibel wäre. Durch Die Einhaltung dieser Regeln wird sichergestellt, dass beide Seiten vollständig kompatibel sind, wenn eine Verbindung zwischen einem neuen Client und einem alten Server besteht (oder umgekehrt).

Für eine COM-Schnittstelle kann das Versionsattribut nicht verwendet werden. Das Erstellen neuer Schnittstellen und das Erben von den alten Schnittstellen entspricht der Bearbeitung der Version in RPC. In der Regel besteht der beste Ansatz in COM darin, eine neue Schnittstelle für die erweiterte Funktionalität zu erstellen. Eine Entsprechung der Nebenversion ist die neue Schnittstelle, die von der alten erbt. Das Ändern alter Methoden oder alter Datentypen erfordert eine völlig neue COM-Schnittstelle– eine Schnittstelle, die nicht von der alten erbt.

Für COM ist die [**QueryInterface-Funktion**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) eine bewährte Methode, um zu überprüfen, ob ein Server eine Schnittstelle unterstützt. Daher können die Situationen, in denen ein Client mit einer alten oder einer neuen Version einer Schnittstelle kommunizieren kann, einfach gelöst werden.

 

 