---
title: Die versionierungstheorie für RPC und com
description: Versionierungstheorie für Remote Prozedur Aufruf (RPC) und com.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- Remote Prozedur Aufruf RPC, Best Practices, Versionierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b23c91bf69fbc3c4f72366b80812fd54330d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102118"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>Die versionierungstheorie für RPC und com

Nur zwei vollständig narrensicher-Methoden unterstützen neue Funktionen ohne das Risiko von Problemen bei der Netzwerkkompatibilität:

-   Ändern Sie die Schnittstellen Version gemäß den Regeln. Dadurch wird verhindert, dass neue Clients mit einem alten Server kommunizieren, und es wird möglicherweise verhindert, dass ein Alter Client mit dem neuen Server kommuniziert. Dies wird weiter unten in diesem Abschnitt erläutert.
-   Führen Sie eine andere Schnittstelle ein, die die neue Funktionalität behandelt.

Eine standardmäßige RPC-Schnittstelle wird durch eine Kombination aus GUID und Versionsnummer identifiziert. eine COM-Schnittstelle wird durch ihre GUID identifiziert. Die-Version besteht aus Haupt-und Nebenkomponenten. Bei Standardschnittstellen mit derselben GUID und verschiedenen Versionsnummern ist nur eine Verbindung möglich, wenn die Hauptversion identisch ist, und der Client ist nicht höher als die neben Version des Servers.

Dies hat zur Folge, dass das Ändern der RPC-Schnittstellen-GUID die Netzwerkkompatibilität unterbricht, während das Ändern des Schnittstellen namens nicht erfolgt.

In Standard-RPC ist ein Pfad für Upgrades und Erweiterungen gut definiert und erfordert im Grunde, dass neue Methoden nur am Ende der-Schnittstelle hinzugefügt werden, und neue Typen nur in den neuen Methoden verwendet werden. Wenn solche Ergänzungen erforderlich sind, muss die neben Version erweitert werden. Jede andere Änderung erfordert eine Änderung in der Hauptversion, weil die Client-und Server Software bei der Übertragung nicht kompatibel wäre. Wenn diese Regeln eingehalten werden, wird sichergestellt, dass beide Seiten vollständig kompatibel sind, wenn eine Verbindung zwischen einem neuen Client und einem alten Server besteht oder umgekehrt.

Für eine COM-Schnittstelle kann das Versions Attribut nicht verwendet werden. Das Erstellen neuer Schnittstellen und das Erben von den alten Schnittstellen entspricht der Bearbeitung der Version in RPC. Der beste Ansatz für com besteht in der Regel darin, eine neue Schnittstelle für die erweiterte Funktionalität zu erstellen. Eine Entsprechung der neben Version ist die neue Schnittstelle, die von der alten-Schnittstelle erbt. Um alte Methoden oder alte Datentypen zu ändern, ist eine völlig neue COM-Schnittstelle erforderlich – eine Schnittstelle, die nicht von der alten Methode erbt.

Bei com ist die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Funktion eine bewährte Methode, um zu überprüfen, ob ein Server eine Schnittstelle unterstützt. Daher kann die Situation, in der ein Client mit einer alten oder einer neuen Version einer Schnittstelle kommunizieren kann, problemlos aufgelöst werden.

 

 