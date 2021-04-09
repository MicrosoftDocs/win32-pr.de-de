---
description: Im Windows SDK für Windows Server 2008 sind zwei WSDAPI-Beispiele enthalten.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: WSDAPI-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754960"
---
# <a name="wsdapi-samples"></a>WSDAPI-Beispiele

Im Windows SDK für Windows Server 2008 sind zwei WSDAPI-Beispiele enthalten. Den Quellcode für die Beispiele finden Sie unter <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI. Diese SDK-Version ist im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)verfügbar. Die Beispiele sind im Windows Vista SDK nicht verfügbar.

Das Aktienkurs Beispiel (in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ StockQuote) veranschaulicht einen Dienst mit grundlegenden Messaging Funktionen. Das Beispiel für den Datei Dienst (in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ Fileservice) veranschaulicht einen Dienst mit erweiterten Funktionen, wie z. b. asynchrones Messaging, Anlagen und Ereignisse.

Beide Beispiele enthalten die folgenden Dateitypen.

-   WSDL-Dateien, die die Dienst Beschreibungen enthalten.
-   [Wsdcodegen-Konfigurationsdateien](wsdcodegen-configuration-file.md) , die zum Generieren von WSDAPI-Code verwendet werden.
-   Generierte C++-Header-und-Quelldateien.
-   Client-und Dienst Implementierungs Dateien.
-   Visual Studio-Projekt-und-Projektmappendateien.

Beide Beispiele implementieren Geräte Hosts ([**iwsddevicehost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), Geräte [**Proxys (iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) und Dienst [**Proxys (iwsdserviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)). Außerdem wird im Beispiel für den Datei Dienst die Verwendung von asynchronem Messaging ([**iwsdasynccallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**iwsdasynkresult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), Anlagen ([**iwsdinboundattachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**iwsdoutboundattachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) und Eventing veranschaulicht.

Die Dateien "fileservicecontract. vcproj" und "stockquotecontract. vcproj", die in den Beispielen enthalten sind, rufen [wsdcodegen](web-services-for-devices-code-generator.md) auf, um den C++-Header und die Quelldateien aus der WSDL-Datei zu generieren Dies bedeutet Folgendes: Wenn die WSDL-oder wsdcodegen-Beispielkonfigurationsdatei geändert und das Beispiel Projekt neu erstellt wird, generiert wsdcodegen automatisch neue Header-und Quelldateien, die die Änderungen widerspiegeln. Dies ist die bevorzugte Methode zum Entwickeln von WSDAPI-Anwendungen. Wsdcodegen wird in der Regel von der Befehlszeile aus aufgerufen. Öffnen Sie die relevante \* VCPROJ-Datei, um die Beispiele für wsdcodegen-Befehlszeilen Aufrufe anzuzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Anwendungsentwicklung unter Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



