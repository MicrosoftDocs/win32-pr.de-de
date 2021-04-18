---
description: WMI unterstützt verschiedene Threading Modelle in Abhängigkeit davon, wie der Anbieter gehostet wird, und den Typ der Anbieter Funktionalität, z. b. Klasse oder Eigenschaft.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Auswählen der richtigen Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357808"
---
# <a name="choosing-correct-registration"></a>Auswählen der richtigen Registrierung

WMI unterstützt verschiedene Threading Modelle in Abhängigkeit davon, wie der Anbieter gehostet wird, und den Typ der Anbieter Funktionalität, z. b. [Klasse](writing-a-class-provider.md) oder [Eigenschaft](writing-a-property-provider.md). Beispielsweise unterstützen [*entkoppelte Anbieter*](gloss-d.md) nicht alle Typen von Anbieter Funktionen. Weitere Informationen zu unterschiedlichen Hostingmodellen und deren Konfiguration finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

## <a name="in-process-providers"></a>In-Process Anbieter

In-Process-Anbieter werden in einem freigegebenen Host Prozess ausgeführt, Wmiprvse.exe. Die meisten in-Process-Anbieter Typen verwenden das Multithread-Apartment-Modell (MTA).

Das MTA-Modell wird für die folgenden Typen von Anbieter Funktionen unterstützt:

-   [Klassen Anbieter](writing-a-class-provider.md)
-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methoden Anbieter](writing-a-method-provider.md)
-   [Eigenschaften Anbieter](writing-a-property-provider.md)
-   [Ereignis Anbieter](writing-an-event-provider.md)
-   [Ereignisconsumeranbieter](writing-an-event-consumer-provider.md)

Das STA-Modell (Single Thread-Apartment) wird für einige Arten von Anbieter Funktionen unterstützt:

-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methoden Anbieter](writing-a-method-provider.md)
-   [Ereignis Anbieter](writing-an-event-provider.md)
-   [Ereignisconsumeranbieter](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Out-of-Process-Anbieter

Anbieter, die auf einem anderen gemeinsamen Dienst Host gehostet werden, unterstützen die folgende Anbieter Funktionalität:

-   [Klassen Anbieter](writing-a-class-provider.md)
-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methoden Anbieter](writing-a-method-provider.md)
-   [Eigenschaften Anbieter](writing-a-property-provider.md)
-   [Ereignis Anbieter](writing-an-event-provider.md)
-   [Ereignisconsumeranbieter](writing-an-event-consumer-provider.md)

Weitere Informationen zu Hosts für gemeinsame Dienste finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

## <a name="decoupled-providers"></a>Entkoppelte Anbieter

Entkoppelte Anbieter werden in einer Anwendung gehostet. Weitere Informationen finden Sie unter [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md). Anbieter, die im .NET Framework mithilfe von WMI erstellt wurden, sind entkoppelt. Entkoppelte Anbieter unterstützen die folgende Anbieter Funktionalität:

-   [Instanzanbieter](writing-an-instance-provider.md)
-   [Methoden Anbieter](writing-a-method-provider.md)
-   [Ereignis Anbieter](writing-an-event-provider.md)
-   [Ereignisconsumeranbieter](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md)
</dt> </dl>

 

 



