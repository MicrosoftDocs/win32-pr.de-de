---
title: Steuern von Geräten
description: UPnP-basierte Geräte werden von den Diensten gesteuert, die sie verfügbar machen.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410818552f1f6563b28fcb963fcfca5c9b3067973e325adfd66ede5bffaedb75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999630"
---
# <a name="controlling-devices"></a>Steuern von Geräten

UPnP-basierte Geräte werden von den Diensten gesteuert, die sie verfügbar machen. Ein UPnP-Dienst ist die kleinste steuerbare Entität in der UPnP-Architektur. Geräte machen einen Dienst für jede primäre Funktion verfügbar, die sie ausführen. Komplexe Geräte bestehen in der Regel aus mehreren einfachen Diensten und anderen Geräten.

Ein Dienst besteht aus einer Reihe von Zustandsvariablen und einer Reihe von Aktionen, die eine Anwendung aufrufen kann, die für diese Zustandsvariablen verwendet werden. In der Steuerungspunkt-API mit UPnP-Technologie werden Dienste durch **Dienstobjekte** dargestellt, die die [**IUPnPService-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) verfügbar machen.

Ein Diensttyp definiert die Zustandsvariablen und Aktionen, die von einem bestimmten Dienst unterstützt werden. Beispielsweise definiert der Diensttyp für einen Uhrdienst **GetTime-** und **SetTime-Aktionen** zusammen mit einer **Time-Statusvariablen.**

Eine Dienst-ID unterscheidet mehrere allgemeine Diensttypen innerhalb eines einzelnen Geräts. Beispielsweise können zwei Uhrdienste in einer Weckeruhr sein, einer für die reguläre Uhr und der andere für den Alarm. Es muss eine Möglichkeit geben, zwischen den beiden Diensten zu unterscheiden, die identische Diensttypen haben. Die Dienst-ID bietet eine eindeutige Möglichkeit, eine Instanz eines Diensttyps zu identifizieren. Anschließend wird diese Dienst-ID für den Zugriff auf den richtigen Dienst aus der [**IUPnPServices-Sammlung**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) verwendet, da der Diensttyp kein eindeutiger Bezeichner ist. Die [**IUPnPService-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) ermöglicht es Anwendungen auch, eine Rückruffunktion beim Dienstobjekt zu registrieren. Wenn sich der Wert der Zustandsvariablen eines Diensts ändert, ruft das Dienstobjekt den registrierten Rückruf auf, um die Anwendung über die Änderung zu benachrichtigen. Das UPnP-Framework ruft diesen Rückruf auch auf, um Anwendungen zu benachrichtigen, wenn eine Dienstinstanz nicht mehr verfügbar ist. Der Dienst kann aus verschiedenen Gründen nicht mehr verfügbar sein, einschließlich vorübergehender Netzwerkfehler.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Abrufen von Dienstobjekten](obtaining-service-objects.md)
-   [Registrieren eines Rückrufs](registering-a-callback.md)
-   [Abfragen von Zustandsvariablen](querying-state-variables.md)
-   [Aufrufen von Aktionen](invoking-actions.md)

 

 




