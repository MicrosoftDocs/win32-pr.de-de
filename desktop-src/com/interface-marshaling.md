---
title: Marshallen von Schnittstellen
description: Marshallen von Schnittstellen
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdee8762fb9ef69507fb5b2c4295531dd87a98d5174ab4e10f05a66cab718d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029870"
---
# <a name="interface-marshaling"></a>Marshallen von Schnittstellen

Wenn Sie nicht sicher sind, dass Ihre Schnittstelle nie über Apartment-, Thread- oder Prozessgrenzen hinweg verwendet wird, müssen Sie entscheiden, wie Sie Marshallingunterstützung für Ihre Schnittstellen bereitstellen. Es gibt drei Möglichkeiten, Marshallingunterstützung bereitzustellen:

-   Schreiben Sie Einen eigenen Proxy-/Stubcode, der den COM-Kanal aufruft, der wiederum die RPC-Laufzeitbibliotheken aufruft. Theoretisch ist dies möglich, aber in der Praxis ist es fast unmöglich, auf einen erheblichen Aufwand zu verzichten.
-   Beschreiben Sie Ihre Schnittstellen in einer IDL-Datei (Interface Definition Language), und verwenden Sie den MIDL-Compiler, um eine Proxy-/Stub-DLL zu generieren. Diese Methode bietet die beste Leistung und die größte Flexibilität in Bezug auf akzeptable Datentypen. Mit midl-generierten Proxystubs können Sie nicht nur die Speicherverwaltung steuern, sondern auch das Marshallen und Aufheben derMarshaling komplexer Datentypen auf verschiedenen Plattformen.
-   Verwenden Sie MIDL, um eine Typbibliothek zu generieren, die das System zur Bereitstellung von Marshallingunterstützung zur Laufzeit verwendet. Dies ist die einfachste Möglichkeit, Marshallingunterstützung zu implementieren. Sie müssen nur eine Typbibliothek generieren und registrieren. Ihre Schnittstellen müssen automatisierungskompatibel sein [**(oleautomation**](/windows/desktop/Midl/oleautomation) oder [**dual),**](/windows/desktop/Midl/dual)wodurch einige Einschränkungen hinsichtlich der Datentypen bestehen, die Sie als Methodenparameter verwenden können. In den meisten Fällen überwiegt der Vorteil, dass Ihre Schnittstellen für Programme zugänglich sind, die in anderen Sprachen geschrieben sind, z. B. Microsoft Visual Basic und Java, die Einschränkungen bei Datentypen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektübergreifende Kommunikation](inter-object-communication.md)
</dt> </dl>

 

 