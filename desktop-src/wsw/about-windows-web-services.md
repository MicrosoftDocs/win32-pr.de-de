---
title: Informationen zu Windows-Webdiensten
description: Die Windows-Webdienste-API ist eine mehrschichtige API und kann wie folgt dargestellt werden.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104556006"
---
# <a name="about-windows-web-services"></a>Informationen zu Windows-Webdiensten

Die Windows-Webdienste-API ist eine mehrschichtige API und kann wie folgt dargestellt werden.

![Das Diagramm zeigt die Ebenen und die bereichsübergreifenden Bereiche der Windows-Webdienste-API an.](images/apistack.png)

Bei wwsapi handelt es sich um eine mehrschichtige API. Wir gehen davon aus, dass die meisten Entwickler auf das Dienstmodell abzielen, bei dem es sich um ein Methoden basiertes Programmiermodell handelt. Im Dienstmodell stellt der Dienst Host das serverseitige Programmiermodell bereit, während der Dienst Proxy das Client seitige Programmiermodell bereitstellt.

Jede Ebene macht einen Satz von APIs und Typen verfügbar, die mit APIs dieser Ebene verwendet werden können.

## <a name="service-model"></a>Dienstmodell

Die Ebene der obersten Ebene, die als [Dienstmodell](service-model-layer-overview.md) bezeichnet wird, stellt ein Methoden basiertes Programmiermodell bereit, das am einfachsten zu verwenden ist. Im Dienstmodell stellt der [Dienst Host](service-host.md) das serverseitige Programmiermodell bereit, während der [Dienst Proxy](service-proxy.md) das Client seitige Programmiermodell bereitstellt. Der [Kontext](context.md) wird innerhalb des Dienst Modells verwendet, um einen relevanten Zustand zu übergeben, der für den Dienst Vorgang und/oder den Rückruf verfügbar ist, wenn er aufgerufen wird. Und [Dienstvertrag](contract.md) wird verwendet, um einen Dienstvertrag für einen Endpunkt anzugeben, der für den Dienst verfügbar gemacht wird. Die folgenden Komponenten und Vorgänge sind Teil der Dienst Ebene:

-   [Dienst Host](service-host.md)
-   [Dienst Proxy](service-proxy.md)
-   [Context](context.md)
-   [Bedingungen](contract.md)
-   [Dienstmetadaten](service-metadata.md)

## <a name="channel-layer"></a>Kanal Ebene

Das Dienstmodell basiert auf einer Kanal Ebene, die vollständige Flexibilität bietet, aber schwieriger zu verwenden ist. Die folgenden Komponenten und Vorgänge sind Teil der Kanal Ebene:

-   [Meldung](message.md)
-   [Kanal](channel.md)
-   [Listener](listener.md)
-   [Fehler](faults.md)
-   [Url](url.md)
-   [Security](security-overview.md)
-   [Metadatenimport](metadata-import.md)

## <a name="xml-layer"></a>XML-Ebene

Die Kanal Schicht basiert wiederum auf einem vereinfachten XML-Framework, das die Deserialisierung von C-Datentypen einschließt. Die folgenden Komponenten und Vorgänge sind Teil der XML-Ebene:

-   [XML-Writer](xml-writer.md)
-   [XML-Reader](xml-reader.md)
-   [XML-Puffer](xml-buffer.md)
-   [Serialisierung](serialization.md)
-   [XML-Sprachunterstützung](xml-language-support.md)

## <a name="common-to-all-layers"></a>Alle Ebenen gemeinsam

Im folgenden finden Sie Themen, die für jede der drei Ebenen gelten:

-   [Fehler](errors.md)
-   [Asynchrones Modell](asynchronous-model.md)
-   [Threadsicherheit](thread-safety.md)
-   [Ablaufverfolgung](tracing.md)
-   [Abbruch](cancellation.md)
-   [Hilfsprogramme](utilities.md)
-   [Debuggen](debugging.md)
-   [Wsutil-Compilertool](wsutil-compiler-tool.md)
-   [Heap](heap.md)

## <a name="examples"></a>Beispiele

Weitere Informationen zu API-Elementen finden Sie unter [Referenz zu Windows-Webdiensten](windows-web-services-reference.md). Beispiele für die Verwendung der-API finden [Sie unter Verwenden von Windows-Webdiensten](using-windows-web-services.md).

 

 




