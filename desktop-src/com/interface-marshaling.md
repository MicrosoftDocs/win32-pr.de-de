---
title: Schnittstellenmarshalling
description: Schnittstellenmarshalling
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337874"
---
# <a name="interface-marshaling"></a>Schnittstellenmarshalling

Wenn Sie nicht sicher sind, dass Ihre Schnittstelle nie über Apartment-, Thread-oder Prozess Grenzen hinweg verwendet wird, müssen Sie entscheiden, wie Sie Marshallingunterstützung für ihre Schnittstellen bereitstellen möchten. Es gibt drei Möglichkeiten, marshalingunterstützung bereitzustellen:

-   Schreiben Sie Ihren eigenen Proxy-/Stubcode, der den com-Kanal aufruft, der wiederum die RPC-Laufzeitbibliotheken aufruft. Theoretisch ist es möglich, dies zu tun, aber in der Praxis ist es fast unmöglich, ohne großen Aufwand zu arbeiten.
-   Beschreiben Sie die Schnittstellen in einer IDL-Datei (Interface Definition Language), und verwenden Sie den-compilercompiler, um eine Proxy-/Stub-DLL zu generieren. Diese Methode bietet die beste Leistung und die größte Flexibilität in Bezug auf akzeptable Datentypen. Mithilfe von mit mittlerer l generierten proxystubzugriff können Sie nicht nur die Speicherverwaltung steuern, sondern auch das Marshalling und das nicht Marshalling komplexer Datentypen auf verschiedenen Plattformen.
-   Verwenden Sie die-Mittell, um eine Typbibliothek zu generieren, mit der das System zur Laufzeit Marshallingunterstützung bereitstellt. Dies ist die einfachste Möglichkeit zum Implementieren von Marshalling-Unterstützung. Sie müssen lediglich eine Typbibliothek generieren und registrieren. Ihre Schnittstellen müssen Automatisierungs kompatibel sein (entweder [**oleautomation**](/windows/desktop/Midl/oleautomation) oder [**Dual**](/windows/desktop/Midl/dual)), sodass einige Einschränkungen hinsichtlich der Arten von Datentypen bestehen, die Sie als Methoden Parameter verwenden können. In den meisten Fällen hat der Vorteil, dass die Schnittstellen für Programme, die in anderen Sprachen geschrieben wurden, wie z. b. Microsoft Visual Basic und Java, die Einschränkungen der Datentypen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kommunikation zwischen Objekten](inter-object-communication.md)
</dt> </dl>

 

 