---
title: ADSI-Beispiel Anbieter Komponente
description: Active Directory Dienst Schnittstellen Anbieter-Writer finden diesen Abschnitt von besonderem Interesse, da die ADSI-Beispiel Anbieter Komponente ausführlich beschrieben wird.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309267"
---
# <a name="adsi-example-provider-component"></a>ADSI-Beispiel Anbieter Komponente

Active Directory Dienst Schnittstellen Anbieter-Writer finden diesen Abschnitt von besonderem Interesse, da die ADSI-Beispiel Anbieter Komponente ausführlich beschrieben wird. Administratoren von ADSI-Anbietern können den Beispiel Anbieter installieren und das Code Framework als Grundlage für die Erstellung einer eigenen Implementierung verwenden. Die folgenden Themen werden erörtert:

Bei [der Installation der Beispiel Anbieter Komponente](installing-the-example-provider-component.md) wird beschrieben, wie Sie den ADSI-Beispiel Anbieter und das zugehörige Mock-Verzeichnis installieren. Dieser Abschnitt enthält eine Liste der Registrierungs Einstellungen.

[Verzeichnis Definition](directory-definition.md) beschreibt die Verzeichniseinträge, die von der Beispiel Anbieter Komponente definiert werden.

In der [Schema Verwaltung](schema-management.md) wird beschrieben, wie jedes Element im Beispiel Verzeichnisdienst der Anbieter Komponente durch einen bestimmten Typ von Active Directory Objekt dargestellt werden kann.

Beim [binden an ein Active Directory Objekt](binding-to-an-active-directory-object.md) wird beschrieben, wie die Beispiel Anbieter Komponente bei Verwendung einer ADsPath-Zeichenfolge dieses Element identifiziert, den entsprechenden Typ Active Directory Objekts erstellt und den angeforderten Typ des Schnittstellen Zeigers für das Objekt abruft, das an die ADS-Client Software zurückgegeben werden soll.

[Enumeratorobjekte](enumerator-objects.md) listet die spezifischen Typen von Enumerationen auf, die von der Beispiel Anbieter Komponente bereitgestellt werden, und in welchem Quellcode die Implementierungen gefunden werden können.

Die [Code Übersicht](code-overview.md) enthält eine Beschreibung der einzelnen Teile der Beispiel Anbieter Komponente auf Aufgaben Ebene.

[Code Details](code-details.md) listet die Softwaremodule und deren Inhalte auf.

 

 




