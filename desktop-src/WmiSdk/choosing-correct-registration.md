---
description: WMI unterstützt unterschiedliche Threadingmodelle, je nachdem, wie der Anbieter gehostet wird, und dem Typ der Anbieterfunktionalität, z. B. Klasse oder Eigenschaft.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Auswählen der richtigen Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3e9a252e9013e828f5dc2c6e4c7228919d0834d0edb3da5f699cbe0306a38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131802"
---
# <a name="choosing-correct-registration"></a>Auswählen der richtigen Registrierung

WMI unterstützt unterschiedliche Threadingmodelle, je nachdem, wie der Anbieter gehostet wird, und dem Typ der Anbieterfunktionalität, z. B. [Klasse](writing-a-class-provider.md) oder [Eigenschaft.](writing-a-property-provider.md) Entkoppelte [*Anbieter unterstützen*](gloss-d.md) beispielsweise nicht alle Arten von Anbieterfunktionen. Weitere Informationen zu verschiedenen Hostingmodellen und deren Konfiguration finden Sie unter [Hosting und Sicherheit für Anbieter.](provider-hosting-and-security.md)

## <a name="in-process-providers"></a>In-Process Anbieter

In-Process-Anbieter werden in einem freigegebenen Hostprozess ausgeführt, Wmiprvse.exe. Die meisten Prozessanbietertypen verwenden das MTA-Modell (Multithread-Apartment).

Das MTA-Modell wird für die folgenden Arten von Anbieterfunktionen unterstützt:

-   [Klassenanbieter](writing-a-class-provider.md)
-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methodenanbieter](writing-a-method-provider.md)
-   [Eigenschaftenanbieter](writing-a-property-provider.md)
-   [Ereignisanbieter](writing-an-event-provider.md)
-   [Ereignisverbraucheranbieter](writing-an-event-consumer-provider.md)

Das Sta-Modell (Singlethreaded Apartment) wird für einige Arten von Anbieterfunktionen unterstützt:

-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methodenanbieter](writing-a-method-provider.md)
-   [Ereignisanbieter](writing-an-event-provider.md)
-   [Ereignisverbraucheranbieter](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Out-of-Process-Anbieter

Anbieter, die auf einem anderen freigegebenen Diensthost gehostet werden, unterstützen die folgenden Anbieterfunktionen:

-   [Klassenanbieter](writing-a-class-provider.md)
-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methodenanbieter](writing-a-method-provider.md)
-   [Eigenschaftenanbieter](writing-a-property-provider.md)
-   [Ereignisanbieter](writing-an-event-provider.md)
-   [Ereignisverbraucheranbieter](writing-an-event-consumer-provider.md)

Weitere Informationen zu Hosts mit gemeinsam genutzten Diensten finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

## <a name="decoupled-providers"></a>Entkoppelte Anbieter

Entkoppelte Anbieter werden in einer Anwendung gehostet. Weitere Informationen finden Sie unter [Integrieren eines Anbieters in eine Anwendung.](incorporating-a-provider-in-an-application.md) Anbieter, die mithilfe von WMI in der .NET Framework werden entkoppelt. Entkoppelte Anbieter unterstützen die folgenden Anbieterfunktionen:

-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methodenanbieter](writing-a-method-provider.md)
-   [Ereignisanbieter](writing-an-event-provider.md)
-   [Ereignisverbraucheranbieter](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Anbieterhosting und -sicherheit](provider-hosting-and-security.md)
</dt> </dl>

 

 



