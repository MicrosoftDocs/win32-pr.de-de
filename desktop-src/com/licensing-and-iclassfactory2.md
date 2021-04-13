---
title: Lizenzierung und IClassFactory2
description: Lizenzierung und IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9376d5187588ba14da434161309409bf1d189a8f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391070"
---
# <a name="licensing-and-iclassfactory2"></a>Lizenzierung und IClassFactory2

Die [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle für ein Class-Objekt stellt den grundlegenden Objekt Erstellungs Mechanismus von com bereit. Mithilfe von **IClassFactory** kann ein Server die Objekt Erstellung auf einem Computer steuern. Die Implementierung der [**IClassFactory:: | ateinstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) -Methode kann die Objekt Erstellung basierend auf dem vorhanden sein einer Computer Lizenz zulassen oder nicht zulassen. Eine Computer Lizenz ist ein Teil der Informationen, die von der auf einem Computer vorhandenen Anwendung getrennt sind, um anzugeben, dass die Software aus einer gültigen Quelle, z. b. den Installations Datenträgern des Anbieters, installiert wurde. Wenn die Computer Lizenz nicht vorhanden ist, kann der Server die Objekt Erstellung nicht zulassen. Die Computer Lizenzierung verhindert die Piraterie in Fällen, in denen ein Benutzer versucht, die Software von einem Computer auf einen anderen zu kopieren, da die Lizenzinformationen nicht mit der Software kopiert werden und der Computer, der die Kopie empfängt, nicht lizenziert ist.

In einer Softwarebranche für Komponenten benötigen die Anbieter jedoch eine präzisere Kontrolle über die Lizenzierung. Zusätzlich zur Computer Lizenzkontrolle muss ein Hersteller es einigen Clients gestatten, ein Komponenten Objekt zu erstellen, während anderen Clients dieselbe Funktion verweigert wird. Hierfür ist es erforderlich, dass die Client Anwendung einen Lizenzschlüssel von der Komponente erhält, während sich die Client Anwendung noch in der Entwicklungsphase befindet. Die Client Anwendung verwendet den Lizenzschlüssel zur Laufzeit, um Objekte auf einem nicht lizenzierten Computer zu erstellen.

Wenn ein Anbieter z. b. eine Bibliothek von Steuerelementen für Entwickler bereitstellt, verfügt der Entwickler, der die Bibliothek erwirbt, über eine vollständige Computer Lizenz, sodass die Objekte auf dem Entwicklungs Computer erstellt werden können. Der Entwickler kann dann auf dem lizenzierten Computer eine Client Anwendung erstellen, die ein oder mehrere der Steuerelemente enthält. Wenn die resultierende Client Anwendung auf einem anderen Computer ausgeführt wird, müssen die in der Client Anwendung verwendeten Steuerelemente auch auf dem anderen Computer erstellt werden, auch wenn dieser Computer nicht über eine Computer Lizenz für die Steuerelemente des ursprünglichen Herstellers verfügt.

Die [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) -Schnittstelle stellt diese Steuerungsebene bereit. Um die Schlüssel basierte Lizenzierung für eine bestimmte Komponente zuzulassen, implementieren Sie **IClassFactory2** für das klassenfactoryobjekt für diese Komponente. **IClassFactory2** wird von [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)abgeleitet, d. h. durch die Implementierung von **IClassFactory2** erfüllt das klassenfactoryobjekt die grundlegenden com-Anforderungen.

Verwenden Sie die folgenden Methoden in [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), um eine lizenzierte Komponente in die Client Anwendung zu integrieren:

-   Die [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) -Methode füllt eine [**LICINFO**](/windows/win32/api/ocidl/ns-ocidl-licinfo) -Struktur mit Informationen auf, die das Lizenzierungs Verhalten der Klassenfactory beschreiben. So kann z. b. die Klassenfactory Lizenzschlüssel für die Lauf Zeit Lizenzierung bereitstellen, wenn das **fruntimekey-** Member **true** ist.
-   Die [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) -Methode stellt einen Lizenzschlüssel für die Komponente bereit. Eine Computer Lizenz muss verfügbar sein, wenn der Client diese Methode aufruft.
-   Die Methode " [**kreateinstancelic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) " erstellt eine Instanz der lizenzierten Komponente, wenn der Parameter für den Lizenzschlüssel (bstrankey) gültig ist.

> [!Note]  
> In den Typinformationen verwendet eine Komponente das lizenzierte Attribut, um die Co-Klasse zu markieren, die die Lizenzierung über [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)unterstützt.

 

Zunächst benötigen Sie ein separates Entwicklungs Tool, bei dem es sich auch um einen Client der lizenzierten Komponente handelt. Der Zweck dieses Tools ist, den Laufzeitlizenz Schlüssel abzurufen und in der Client Anwendung zu speichern. Dieses Tool wird nur auf einem Computer ausgeführt, der über eine Computer Lizenz für die Komponente verfügt. Das Tool Ruft die Methoden [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) und [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) zum Abrufen des Laufzeitlizenz Schlüssels auf und speichert dann den Lizenzschlüssel in der Client Anwendung. Das Entwicklungs Tool könnte z. b. eine Header Datei (. h) mit dem BSTR-Lizenzschlüssel erstellen und diese h-Datei in die Client Anwendung einschließen.

Um die Komponente in der Client Anwendung zu instanziieren, versuchen Sie zunächst, das Objekt direkt mit " [**IClassFactory::**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance)" zu instanziieren. Wenn " **destance** " erfolgreich ist, wird der zweite Computer für die Komponente lizenziert, und die Objekte können bei der Erstellung erstellt werden. Wenn " **destance**" mit der Rückgabecode Klasse " \_ E \_ notlizenzierte" ausfällt, besteht die einzige Möglichkeit zum Erstellen des Objekts darin, den Lauf Zeit Schlüssel an die Methode " [**kreateinstancelic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) " zu übergeben. " **Kreateinstancelic** " überprüft den Schlüssel und erstellt das Objekt, wenn der Schlüssel gültig ist.

Auf diese Weise kann eine Anwendung, die mit Komponenten (z. b. Steuerelemente) erstellt wurde, auf einem Computer ausgeführt werden, der keine andere Lizenz hat – nur die Client Anwendung, die die Laufzeitlizenz enthält, darf die fraglichen Komponenten Objekte erstellen.

Die [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) -Schnittstelle unterstützt Flexibilität in Lizenzierungs Schemas. Der Server implemenor kann z. b. die Lizenzschlüssel in der Komponente verschlüsseln, um die Sicherheit zu erhalten. Server Implementierungen können auch Funktionsebenen in ihren Objekten aktivieren bzw. deaktivieren, indem Sie unterschiedliche Lizenzschlüssel für verschiedene Funktionen bereitstellen. Beispielsweise kann ein Schlüssel eine grundlegende Funktionsebene ermöglichen, während eine andere grundlegende und erweiterte Funktionalität ermöglicht usw.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuständigkeiten von com-Servern](com-server-responsibilities.md)
</dt> </dl>

 

 