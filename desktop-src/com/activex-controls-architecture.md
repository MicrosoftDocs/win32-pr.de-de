---
title: ActiveX-Steuerelement Architektur
description: ActiveX-Steuerelemente bauen auf einer Grundlage von vielen Objekten auf niedrigerer Ebene und Schnittstellen in OLE auf. Die exakten Schnittstellen, die in einem Steuerelement verfügbar sind, variieren je nach Funktionalität. In diesem Abschnitt werden die Funktionen, die ein Steuerelement möglicherweise bereitstellt, näher betrachtet.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709552"
---
# <a name="activex-controls-architecture"></a>ActiveX-Steuerelement Architektur

ActiveX-Steuerelemente bauen auf einer Grundlage von vielen Objekten auf niedrigerer Ebene und Schnittstellen in OLE auf. Die exakten Schnittstellen, die in einem Steuerelement verfügbar sind, variieren je nach Funktionalität. In diesem Abschnitt werden die Funktionen, die ein Steuerelement möglicherweise bereitstellt, näher betrachtet.

ActiveX-Steuerelemente werden verwendet, um die Bausteine zum Erstellen von Benutzeroberflächen in Anwendungen bereitzustellen. Beispielsweise ist eine Schaltfläche, die eine Aktion in der Containeranwendung initiiert, wenn darauf geklickt wird, ein einfaches Steuerelement. Die folgenden Aspekte sind an der Bereitstellung dieser Benutzeroberflächen Bausteine beteiligt:

-   Ein-Steuerelement kann in seinen Container Client eingebettet werden, um Benutzeroberflächen Aktivitäten innerhalb des Clients zu unterstützen. Folglich muss ein Steuerelement eine visuelle Darstellung von sich selbst bereitstellen, wenn es in den Container eingebettet ist und eine Möglichkeit bieten muss, seinen Zustand zu speichern, z. b. seine Eigenschaftswerte und seine Position innerhalb des Containers. Der Client muss die Verwendung eines Containers mit eingebetteten Objekten unterstützen.
-   Wenn Sie das Steuerelement mit einer Tastatur oder Maus aktivieren, initiiert der Endbenutzer eine Aktion in der Client Anwendung. Folglich muss ein Steuerelement auf die Tastatur Aktivität reagieren und in der Lage sein, mit seinem Client zu kommunizieren, damit er den Container seiner Aktivitäten benachrichtigen und Ereignisse im Client auslöst.
-   Der Client stellt in der Regel auch eine Programmiersprache bereit, über die der Endbenutzer Aktionen initiieren kann, die von den Eigenschaften und Methoden des Steuer Elements bereitgestellt werden. Folglich muss ein Steuerelement Automation und eine Reihe von Entwurfszeit-und Lauf Zeit Features unterstützen.

Aufgrund der Rolle beim Bereitstellen von Benutzeroberflächen Bausteinen unterstützt ein Steuerelement in der Regel Features in den folgenden Bereichen mithilfe von OLE-Technologien, wie hier gezeigt:

<dl> <dt>

<span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Eigenschaften und Methoden
</dt> <dd>

Wie jedes OLE-Objekt kann ein Steuerelement einen Großteil seiner Funktionen über einen Satz eingehender Schnittstellen mit Eigenschaften und Methoden bereitstellen. Der Container kann zusätzliche Ambient-Eigenschaften bereitstellen, und er kann die Erweiterung der Eigenschaften des Steuer Elements durch Aggregation unterstützen. Diese Features verbleibenden sich auf OLE-Automatisierung, Eigenschaften Seiten, Verbindungs fähige Objekte und ActiveX-Steuerelement Technologien.

</dd> <dt>

<span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Fall
</dt> <dd>

Zusätzlich zur Bereitstellung von Eigenschaften und Methoden kann ein ActiveX-Steuerelement auch ausgehende Schnittstellen bereitstellen, um den Client über Ereignisse zu benachrichtigen. Der Client muss die Behandlung dieser Ereignisse unterstützen. Diese Features verwenden OLE-Automatisierung und Verbindungs fähige Objekte.

</dd> <dt>

<span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visuelle Darstellung
</dt> <dd>

Ein Steuerelement kann die Positionierung und Anzeige innerhalb des Containers unterstützen. Der Container positioniert das Steuerelement und bestimmt seine Größe. Diese Features verwenden Verbund Dokument Technologie, einschließlich OLE-Drag & Drop-Technologie.

</dd> <dt>

<span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Tastatur Behandlung
</dt> <dd>

Ein Steuerelement kann auf Tastaturbeschleuniger reagieren, sodass der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden. Der Container verwaltet die Tastatur Aktivität für alle eingebetteten Steuerelemente. Diese Features verwenden Steuerungs-und Verbund Dokument Technologien.

</dd> <dt>

<span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistenz
</dt> <dd>

Ein Steuerelement kann seinen Zustand speichern. Der Client verwaltet die Persistenz der eingebetteten Steuerelemente. Diese Features verwenden strukturierte Speicher-und objektpersistenztechnologien.

</dd> <dt>

<span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registrierung und Lizenzierung
</dt> <dd>

Ein Steuerelement unterstützt in der Regel die Selbstregistrierung und erstellt einen Satz von Registrierungs Einträgen, wenn er instanziiert wird. Ein Steuerelement kann auch lizenziert werden, um eine unbefugte Verwendung zu verhindern.

</dd> </dl>

Die meisten dieser Features umfassen sowohl das-Steuerelement als auch den Client Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




