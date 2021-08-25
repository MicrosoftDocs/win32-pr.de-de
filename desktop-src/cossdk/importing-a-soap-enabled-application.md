---
description: Wenn eine SOAP-fähige Anwendung von einem Server im Proxymodus exportiert wurde, können Clients, die sie importieren, automatisch auf die Methoden der Enthaltenen Komponenten zugreifen, die sie remote als Webdienste enthält, die vom Server im clientaktivierten Objektmodus (CAO) angeboten werden. Dadurch können Sie die Funktionalität einer COM+-Anwendung ganz einfach über ein Netzwerk als XML-Webdienst bereitstellen.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importieren einer SOAP-Enabled-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a41a60c2b5ca69197582a684920e9e935f28631779bc632810049f1a7d03945
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858920"
---
# <a name="importing-a-soap-enabled-application"></a>Importieren einer SOAP-Enabled-Anwendung

Wenn eine SOAP-fähige Anwendung von einem Server im Proxymodus [exportiert](exporting-a-soap-enabled-application.md) wurde, können Clients, die sie importieren, automatisch auf die Methoden der Enthaltenen Komponenten zugreifen, die sie remote als Webdienste enthält, die vom Server im clientaktivierten Objektmodus (CAO) angeboten werden. Dadurch können Sie die Funktionalität einer COM+-Anwendung ganz einfach über ein Netzwerk als XML-Webdienst bereitstellen.

Wenn die Auf diese Weise importierten Komponenten einer Anwendung auf dem Client verwendet werden, werden sie nicht auf dem Client ausgeführt, sondern über den XML-Webdienst, der vom Server bereitgestellt wird, von dem die Anwendung exportiert wurde, remote aufgerufen. Ausführliche Informationen zur Verwendung der Komponenten einer Auf diese Weise importierten Anwendung finden Sie unter [Zugreifen auf XML-Webdienste im CAO-Modus.](accessing-xml-web-services-in-cao-mode.md)

## <a name="component-services-administrative-tool"></a>Verwaltungstool "Komponentendienste"

Um eine SOAP-fähige Anwendung in einen Client zu importieren, verwenden Sie die folgenden Schritte:

1.  Öffnen Sie in der Konsolenstruktur des Component Services-Verwaltungstools unter **Komponentendienste** den Ordner, der dem Clientcomputer zugeordnet ist, auf dem Sie die Anwendung installieren möchten.

2.  Klicken Sie mit der rechten Maustaste auf den Ordner **COM+-Anwendungen** des Clients, und wählen Sie dann **Neu** aus. Der **COM+-Anwendungsinstallations-Assistent** wird angezeigt.

3.  Klicken Sie im **COM+-Anwendungsinstallations-Assistenten** auf **Vordefinierte Anwendungen installieren.**

4.  Durchsuchen Sie das Netzwerk, um den Netzwerkpfad der MSI-Datei auf dem Server zu suchen oder anzugeben, von dem aus Sie die Anwendung installieren möchten.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="remarks"></a>Hinweise

COM-Komponenten werden durch eine GUID identifiziert, die sich ändert, wenn die Komponenten neu kompiliert werden. Wenn eine konfigurierte COM-Komponente, die als XML-Webdienst verfügbar gemacht wird, neu kompiliert wird, werden Clientanwendungen, die sie verwenden, ausfallen. Wenn daher eine Komponente, die als XML-Webdienst verfügbar gemacht wird, neu kompiliert wird, sollten Clients die Anwendungen, die die Komponente verwenden, erneut importieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über den COM+-SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Exportieren einer SOAP-Enabled-Anwendung](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



