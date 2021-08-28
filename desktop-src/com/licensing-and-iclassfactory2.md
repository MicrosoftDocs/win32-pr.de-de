---
title: Lizenzierung und IClassFactory2
description: Lizenzierung und IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8248b24d6b629d42e9ca631b1574c5a6719f0f4f626b2ea22792c3196c591e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096930"
---
# <a name="licensing-and-iclassfactory2"></a>Lizenzierung und IClassFactory2

Die [**IClassFactory-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) für ein Klassenobjekt stellt den grundlegenden Objekterstellungsmechanismus von COM bereit. Mithilfe **von IClassFactory** kann ein Server die Objekterstellung auf Computerbasis steuern. Die Implementierung der [**IClassFactory::CreateInstance-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) kann die Objekterstellung basierend auf dem Vorhandensein einer Computerlizenz zulassen oder nicht zulassen. Eine Computerlizenz ist eine Information, die von der Anwendung getrennt ist, die auf einem Computer vorhanden ist, um anzugeben, dass die Software aus einer gültigen Quelle installiert wurde, z. B. den Installationsdatenträgern des Anbieters. Wenn die Computerlizenz nicht vorhanden ist, kann der Server die Objekterstellung nicht zumuten. Die Computerlizenzierung verhindert Dies wird verhindert, wenn ein Benutzer versucht, die Software von einem Computer auf einen anderen zu kopieren, da die Lizenzinformationen nicht mit der Software kopiert werden und der Computer, der die Kopie empfängt, nicht lizenziert ist.

In einer Komponentensoftwarebranche benötigen Anbieter jedoch ein feineres Maß an Kontrolle über die Lizenzierung. Zusätzlich zur Computerlizenzsteuerung muss ein Anbieter einigen Clients erlauben, ein Komponentenobjekt zu erstellen, während andere Clients die gleiche Funktion verweigern. Dies erfordert, dass die Clientanwendung einen Lizenzschlüssel von der Komponente erhält, während sich die Clientanwendung noch in der Entwicklung befindet. Die Clientanwendung verwendet den Lizenzschlüssel zur Laufzeit, um Objekte auf einem nicht lizenzierten Computer zu erstellen.

Wenn ein Anbieter beispielsweise entwicklern eine Bibliothek mit Steuerelementen zur Verfügung stellt, verfügt der Entwickler, der die Bibliothek erwirbt, über eine vollständige Computerlizenz, sodass die Objekte auf dem Entwicklungscomputer erstellt werden können. Der Entwickler kann dann eine Clientanwendung auf dem lizenzierten Computer erstellen, der mindestens eines der Steuerelemente enthält. Wenn die resultierende Clientanwendung auf einem anderen Computer ausgeführt wird, müssen die in der Clientanwendung verwendeten Steuerelemente auch dann auf dem anderen Computer erstellt werden, wenn dieser Computer keine Computerlizenz für die Steuerelemente des ursprünglichen Anbieters besitzt.

Die [**IClassFactory2-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) bietet diese Steuerungsebene. Um die schlüsselbasierte Lizenzierung für eine bestimmte Komponente zu ermöglichen, implementieren Sie **IClassFactory2** für das Klassenfactoryobjekt für diese Komponente. **IClassFactory2 wird** von [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)abgeleitet. Durch die Implementierung von **IClassFactory2** erfüllt das Klassenfactoryobjekt daher die grundlegenden COM-Anforderungen.

Verwenden Sie die folgenden Methoden in [**IClassFactory2,**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)um eine lizenzierte Komponente in Ihre Clientanwendung zu integrieren:

-   Die [**GetLicInfo-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) füllt eine [**LICINFO-Struktur**](/windows/win32/api/ocidl/ns-ocidl-licinfo) mit Informationen, die das Lizenzierungsverhalten der Klassen factory beschreiben. Beispielsweise kann die Klassen factory Lizenzschlüssel für die Laufzeitlizenzierung bereitstellen, wenn **der fRunTimeKeyAvail-Member** **TRUE ist.**
-   Die [**RequestLicKey-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) stellt einen Lizenzschlüssel für die Komponente zur Verfügung. Eine Computerlizenz muss verfügbar sein, wenn der Client diese Methode aufruft.
-   Die [**CreateInstanceLic-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) erstellt eine Instanz der lizenzierten Komponente, wenn der Lizenzschlüsselparameter (BSTRÂ bstrKey) gültig ist.

> [!Note]  
> In den Typinformationen verwendet eine Komponente das -Attribut, das lizenziert ist, um die Co-Klasse zu markieren, die die Lizenzierung über [**IClassFactory2 unterstützt.**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)

 

Zunächst benötigen Sie ein separates Entwicklungstool, das auch ein Client der lizenzierten Komponente ist. Der Zweck dieses Tools besteht im Abrufen des Laufzeitlizenzschlüssels und speichern ihn in Ihrer Clientanwendung. Dieses Tool wird nur auf einem Computer ausgeführt, der über eine Computerlizenz für die Komponente verfügt. Das Tool ruft die [**Methoden GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) und [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) auf, um den Laufzeitlizenzschlüssel zu erhalten, und speichert den Lizenzschlüssel dann in Ihrer Clientanwendung. Das Entwicklungstool könnte beispielsweise eine Headerdatei (.h) erstellen, die den BSTR-Lizenzschlüssel enthält, und dann würden Sie diese H-Datei in Ihre Clientanwendung hinzufügen.

Um die Komponente in Ihrer Clientanwendung zu instanziieren, versuchen Sie zunächst, das Objekt direkt mit [**IClassFactory::CreateInstance zu instanziieren.**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) Wenn **CreateInstance** erfolgreich ist, wird der zweite Computer für die Komponente lizenziert, und Objekte können nach Be willen erstellt werden. Wenn **CreateInstance mit** dem Rückgabecode CLASS E NOTLICENSED fehlschlägt, besteht die einzige Möglichkeit zum Erstellen des Objekts in der Übergeben des Laufzeitschlüssels an die \_ \_ [**CreateInstanceLic-Methode.**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) **CreateInstanceLic** überprüft den Schlüssel und erstellt das Objekt, wenn der Schlüssel gültig ist.

Auf diese Weise kann eine anwendung, die mit Komponenten (z. B. Steuerelementen) erstellt wurde, auf einem Computer ohne andere Lizenz ausgeführt werden. Nur die Clientanwendung, die die Laufzeitlizenz enthält, kann die in Frage gestellten Komponentenobjekte erstellen.

Die [**IClassFactory2-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) unterstützt Flexibilität bei Lizenzierungsschemas. Beispielsweise kann der Server implementor Lizenzschlüssel in der Komponente verschlüsseln, um die Sicherheit zu erhöhen. Server-Implementierer können auch Funktionalitätsebenen in ihren Objekten aktivieren oder deaktivieren, indem sie unterschiedliche Lizenzschlüssel für verschiedene Funktionen bereitstellen. Beispielsweise könnte ein Schlüssel eine Grundlegende Funktionalitätsebene zulassen, während ein anderer grundlegende und erweiterte Funktionen zulässt, und so weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Serveraufgaben](com-server-responsibilities.md)
</dt> </dl>

 

 