---
description: Das Windows SDK für Windows Server 2008 enthält zwei WSDAPI-Beispiele.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: WSDAPI-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cf4c1ff36195e667c55d9fb5206c0cee2afcf15d1bad7f0139911b3f702a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919957"
---
# <a name="wsdapi-samples"></a>WSDAPI-Beispiele

Das Windows SDK für Windows Server 2008 enthält zwei WSDAPI-Beispiele. Den Quellcode für die Beispiele finden Sie unter <Windows SDK Install Folder> \\ Samples Web \\ \\ WSDAPI (Beispiele web WSDAPI). Diese Version des SDK ist im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)verfügbar. Die Beispiele sind im Windows Vista SDK nicht verfügbar.

Das Aktienkursbeispiel (unter <Windows SDK Install Folder> \\ Samples Web \\ \\ WSDAPI \\ StockQuote) veranschaulicht einen Dienst mit grundlegenden Messagingfunktionen. Das Dateidienstbeispiel (unter <Windows SDK Install Folder> \\ Samples Web \\ \\ WSDAPI \\ FileService) veranschaulicht einen Dienst mit erweiterten Funktionen wie asynchrones Messaging, Anlagen und Ereignis.

Beide Beispiele enthalten die folgenden Dateitypen.

-   WSDL-Dateien, die die Dienstbeschreibungen enthalten.
-   [WsdCodeGen-Konfigurationsdateien,](wsdcodegen-configuration-file.md) die zum Generieren von WSDAPI-Code verwendet werden.
-   Generierte C++-Header- und Quelldateien.
-   Client- und Dienstimplementierungen.
-   Visual Studio Projekt- und Projektmappendateien.

In beiden Beispielen werden Gerätehosts [**(IWSDDeviceHost),**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)Geräteproxys [**(IWSDDeviceProxy)**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)und Dienstproxys [**(IWSDServiceProxy)**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)implementiert. Darüber hinaus veranschaulicht das Dateidienstbeispiel die Verwendung von asynchronen Nachrichten ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), Anlagen ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) und Ereignis.

Die Dateien FileServiceContract.vcproj und StockQuoteContract.vcproj, die in den Beispielen enthalten sind, rufen [WsdCodeGen](web-services-for-devices-code-generator.md) auf, um C++-Header- und Quelldateien aus der WSDL-Datei zu generieren, die in der WsdCodeGen-Konfigurationsdatei angegeben ist. Dies bedeutet Folgendes: Wenn die WSDL- oder WsdCodeGen-Beispielkonfigurationsdatei geändert und das Beispielprojekt neu erstellt wird, generiert WsdCodeGen automatisch neue Header- und Quelldateien, die die Änderungen widerspiegeln. Dies ist die bevorzugte Methode zum Erstellen von WSDAPI-Anwendungen. WsdCodeGen wird in der Regel über die Befehlszeile aufgerufen. Öffnen Sie die entsprechende \* VCPROJ-Datei, um die WsdCodeGen-Beispielbefehlszeilenaufrufe anzuzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Anwendungsentwicklung auf Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



