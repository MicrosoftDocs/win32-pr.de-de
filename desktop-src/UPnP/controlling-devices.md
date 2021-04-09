---
title: Steuern von Geräten
description: UPnP-basierte Geräte werden von den Diensten gesteuert, die Sie verfügbar machen.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a72a4ffdf91bca358124dbb0a0d95ff9a61e30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856648"
---
# <a name="controlling-devices"></a>Steuern von Geräten

UPnP-basierte Geräte werden von den Diensten gesteuert, die Sie verfügbar machen. Ein UPnP-Dienst ist die kleinste steuerbare Entität in der UPnP-Architektur. Geräte machen einen Dienst für jede primäre Funktion verfügbar, die Sie ausführen. Komplexe Geräte bestehen in der Regel aus mehreren einfachen Diensten und anderen Geräten.

Ein Dienst besteht aus einem Satz von Zustandsvariablen und einer Reihe von Aktionen, die eine Anwendung aufrufen kann, die diese Zustandsvariablen verarbeiten. In der Steuerungspunkt-API mit der UPnP-Technologie werden Dienste von **Dienst** Objekten dargestellt, die die [**iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) -Schnittstelle verfügbar machen.

Ein Diensttyp definiert die Zustandsvariablen und Aktionen, die von einem bestimmten Dienst unterstützt werden. Der Diensttyp für einen Takt Dienst definiert z. b. **GetTime** -und **setTime** -Aktionen sowie eine **Zeit** Zustands Variable.

Eine Dienst-ID unterscheidet mehrere allgemeine Dienst Typen innerhalb eines einzelnen Geräts. Es können z. b. zwei Uhr-Dienste in einer Alarm-Uhr vorhanden sein, eine für die reguläre Uhr und die andere für den Alarm. Es muss eine Möglichkeit geben, zwischen den beiden Diensten zu unterscheiden, die identische Dienst Typen aufweisen. Die Dienst-ID bietet eine einzigartige Möglichkeit, eine Instanz eines Dienst Typs zu identifizieren. Anschließend wird diese Dienst-ID verwendet, um auf den richtigen Dienst aus der [**iupnpservices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) -Auflistung zuzugreifen, da der Diensttyp kein eindeutiger Bezeichner ist. Die [**iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) -Schnittstelle ermöglicht Anwendungen auch das Registrieren einer Rückruffunktion mit dem Dienst Objekt. Wenn sich der Wert der Zustandsvariablen eines dienstanders ändert, ruft das Dienst Objekt den registrierten Rückruf auf, um die Anwendung über die Änderung zu benachrichtigen. Das UPnP-Framework ruft diesen Rückruf auch auf, um Anwendungen zu benachrichtigen, wenn eine Dienst Instanz nicht mehr verfügbar ist. Der Dienst kann aus einer Vielzahl von Gründen nicht verfügbar werden, einschließlich vorübergehender Netzwerkfehler.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Abrufen von Dienst Objekten](obtaining-service-objects.md)
-   [Registrieren eines Rückrufs](registering-a-callback.md)
-   [Abfragen von Zustandsvariablen](querying-state-variables.md)
-   [Aufrufen von Aktionen](invoking-actions.md)

 

 




