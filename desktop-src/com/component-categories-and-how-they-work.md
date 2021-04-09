---
title: Komponenten Kategorien und ihre Funktionsweise
description: Komponenten Kategorien und ihre Funktionsweise
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8065584ae2dc83e470428b7345eb2d9321d32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947410"
---
# <a name="component-categories-and-how-they-work"></a>Komponenten Kategorien und ihre Funktionsweise

In den Komponenten Kategorien werden die Funktionsbereiche identifiziert, die von einer Softwarekomponente unterstützt werden, und es wird ein Registrierungs Eintrag für jede Kategorie oder einen identifizierten Funktionsbereich verwendet. Jede Komponenten Kategorie wird durch einen Globally Unique Identifier (GUID) identifiziert. Wenn ein Steuerelement installiert ist, wird es als Steuerelement in der Systemregistrierung unter Verwendung der Komponenten Kategorie-ID für die Steuerung registriert. Weitere Informationen finden Sie unter [Selbstregistrierung für Steuerelemente](self-registration-for-controls.md). In den Steuerelementen Selbstregistrierung registriert Sie auch die Komponenten Kategorien, die implementiert werden, und die Komponenten Kategorien, die ein Container zur Unterstützung benötigt, damit das Steuerelement erfolgreich gehostet werden kann.

Wenn ein Steuerelement Container Steuerelemente für den Benutzer bereitstellt, ist es nur möglich, diese Steuerelemente auszuwählen und zu instanziieren, die in dieser Umgebung adäquat funktionieren können. Wenn der Steuerelement Container beispielsweise keine Datenbindung unterstützt, kann der Benutzer die Steuerelemente, die über einen Eintrag in der Registrierung verfügen, nicht auswählen und instanziieren, was bedeutet, dass die Datenbindung-Komponenten Kategorie erforderlich ist. Ein gängiges Dialogfeld zum Einfügen von Steuerelementen und APIs zur Behandlung der Registrierungseinträge ist verfügbar.

Komponenten Kategorien sind nicht kumulativ oder exklusiv. ein Steuerelement kann eine beliebige Kombination von Komponenten Kategorien erfordern. Ein Steuerelement, das keine erforderlichen Einträge für Komponenten Kategorien enthält, wird möglicherweise in jedem Steuerelement Container funktionieren und erfordert keine bestimmte Funktionalität eines Steuerelement Containers.

Die folgenden Komponenten Kategorien werden hier identifiziert, sofern erforderliche ausführlichere Spezifikationen der Kategorien verfügbar sein können.

-   Kapselung des [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) -Steuer Elements
-   Einfache Datenbindung über die [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) -Schnittstelle.
-   Erweiterte Datenbindung (wie von den zusätzlichen Datenbindung-Schnittstellen von VB 4.0 unterstützt).
-   Visual Basic Private Schnittstellen- [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat), [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Internet fähige Steuerelemente.
-   Fensterlose Steuerelemente.

Dies ist keine definitive Liste von Kategorien. Weitere Kategorien werden wahrscheinlich in Zukunft definiert, wenn neue Anforderungen identifiziert werden. Eine aktuelle Liste der Komponenten Kategorien steht bei Microsoft zur Verfügung. Diese Liste enthält die Komponenten Kategorien, die von Microsoft und anderen Anbietern identifiziert wurden, die von Microsoft informiert wurden.

Denken Sie daran, dass Steuerelemente in möglichst vielen Umgebungen arbeiten sollten. Wenn dies möglich ist, sollte das Steuerelement seine Funktionalität beeinträchtigen, wenn es in einem Container platziert wird, der bestimmte Schnittstellen nicht unterstützt. Der Zweck von Komponenten Kategorien besteht darin, eine Situation zu verhindern, in der das Steuerelement in einer Umgebung platziert wird, die ungeeignet ist, und das Steuerelement die gewünschte Aufgabe nicht erreichen kann. Im Allgemeinen sollte ein Steuerelement ordnungsgemäß herabgestuft werden, wenn keine Schnittstellen vorhanden sind. ein Steuerelement kann dem Benutzer beispielsweise ein Meldungs Feld mitteilen, dass einige Funktionen nicht verfügbar sind, oder die Funktionalität, die ein Steuerelement Container benötigt, für eine optimale Leistung eindeutig dokumentieren.

Beachten Sie, dass ältere Steuerelemente und Container keine Komponenten Kategorien verwenden, sondern stattdessen das Steuerelement Schlüsselwort für das Steuerelement in der Registrierung verwenden. Um von älteren Containern erkannt zu werden, kann es sein, dass Steuerelemente das Control-Schlüsselwort in der Registrierung registrieren möchten. Steuerelement Entwickler sollten prüfen, ob das Steuerelement in solchen Containern erfolgreich gehostet werden kann. Container, die Komponenten Kategorien verwenden, können diese erfolgreich verwenden, um ältere Steuerelemente zu hosten, da die Komponenten Kategorie-dll die Zuordnung behandelt, eine separate Kategorie für ältere Steuerelemente CATID \_ ControlV1, sodass Sie ggf. optional von einem Container ausgeschlossen werden können.

Da Komponenten Kategorien von GUIDs identifiziert werden, kann es vorkommen, dass Container, die bestimmte spezifische Funktionen anbieten, über eigene kategorieids verfügen, die mit einem Tool zur GUID-Generierung generiert werden. Dies kann jedoch den Vorteil der Interoperabilität von Steuerelementen und Containern beeinträchtigen, sodass es bevorzugt wird, dass immer mögliche vorhandene Komponenten Kategorien verwendet werden. Es wird empfohlen, sich beim Definieren neuer Komponenten Kategorien zusammen zu informieren, um sicherzustellen, dass Sie die allgemeinen Anforderungen des Marketplace erfüllen und den Geist der Interoperabilität von ActiveX-Steuerelementen verfolgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

 




