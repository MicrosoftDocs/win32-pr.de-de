---
title: Der Lightweight Client-Side-Handler
description: Mithilfe von Lightweight-Client seitigen Handlern können Sie allgemeine Client seitige Handler beliebiger Größe erstellen, damit Sie eine beliebige Art von Standard Aufgabe ausführen können.
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8df5be24e8773a660a4d0208b27a2f585e32
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730537"
---
# <a name="the-lightweight-client-side-handler"></a>Der Lightweight Client-Side-Handler

Mithilfe von Lightweight-Client seitigen Handlern können Sie allgemeine Client seitige Handler beliebiger Größe erstellen, damit Sie eine beliebige Art von Standard Aufgabe ausführen können. Als Handler können diese von mehr als einem Client verwendet werden. Sie unterscheiden sich von OLE-Handlern darin, dass Sie nicht vor dem Start des Servers erstellt werden können und ihre Lebensdauer an die des Proxy-Managers gebunden ist. Dadurch wird eine mögliche Racebedingung verhindert, bei der der Handler andernfalls vorzeitig freigegeben werden kann.

Der Proxy-Manager ist das vom System erstellte Objekt, das die [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) -Schnittstelle implementiert. Wenn Sie das Standardmarshalling verwenden, erstellt das System es für Sie, wenn Sie [**cogetstandardmarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (oder [**cogetstdmarshalex**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)zum Erstellen eines aggregierten Mars Haller für Lightweight-Handler) aufrufen und außerdem die [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -und [**imultiqi**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) -Schnittstellen für das-Objekt implementieren. Auf der Serverseite ist ein entsprechendes Systemobjekt vorhanden, das auch " **IMarshal**" implementiert. Diese Objekte verarbeiten das Marshalling für Sie transparent.

Es gibt zwei allgemeine Arten von Handlern, die Sie implementieren können:

-   Ein Handler, der einen Dienst ausführt, der keine zusätzlichen Daten vom Server benötigt.
-   Ein Handler, der zusätzliche Daten vom Server verwendet.

Einige potenzielle Verwendungsmöglichkeiten der zusätzlichen Daten im Stream, die vom Server bereitgestellt werden, lauten wie folgt:

-   Statische Daten vom Server. Unabhängig von der bestimmten Schnittstelle, die gemarshallt wird, schreibt der Server dieselben Daten in den Stream.
-   Pro Schnittstelle Daten vom Server. Je nachdem, welche bestimmte Schnittstelle gemarshallt wird, schreibt der Server möglicherweise andere Daten in den Stream.
-   Pro Schnittstellen-Hilfsprogramme. Pro Schnittstelle COM-Komponenten, die in den Client Handler aggregiert und an den Standard Proxy delegiert werden. Um z. b. die Netzwerkleistung zu verbessern, könnte eine COM-Komponente für [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) das Client seitige Zwischenspeichern von Daten, Read-Ahead, Write-Behind, op-Sperrung usw. durchführen.
-   Netzwerk Version einer Schnittstelle. Die Netzwerk Version der Schnittstelle unterscheidet sich von der Schnittstelle, die vom Client-und Server Anwendungscode verfügbar gemacht wird. Es ist z. b. möglich, über die gleiche Netzwerkschnittstelle wie der Einbettungs Server Handler über die gleiche Netzwerkschnittstelle wie den Einbettungs Server zu übermitteln. Beispielsweise kann eine Daten Übertragungs Schnittstelle in eine Netzwerkschnittstelle konvertiert werden, die Pipes für die effiziente Datenübertragung verwendet.

Downlevelclients können aus zwei Gründen die Verwendung von Schnittstellen, die über benutzerdefinierte Handler verfügen, nicht Mars Hallen: Erstens können Sie die CLSID, die im benutzerdefinierten gemarshallten Paket verwendet wird, nicht verstehen, wenn der Server Handler aggregiert wird und das Objekt einen Handler wünscht. Zweitens kann der Handlercode nicht einmal auf der Clientseite ausgeführt werden, wenn er neue Funktionen von com zum Erstellen des aggregierten Standard-Mars Haller und zum Ausführen von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Remote aufrufen erfordert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der OLE-Handler](the-ole-handler.md)
</dt> </dl>

 

 