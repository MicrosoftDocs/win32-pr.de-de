---
title: Vorteile der Verwendung von ADSI-Erweiterungen
description: Die Art und Weise, in der Erweiterungs Methoden implementiert werden, hängt vom erweiterungswriter ab.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036323"
---
# <a name="benefits-of-using-adsi-extensions"></a>Vorteile der Verwendung von ADSI-Erweiterungen

Die Art und Weise, in der Erweiterungs Methoden implementiert werden, hängt vom erweiterungswriter ab. Ein erweiterungswriter kann sogar eine Methode vollständig außerhalb des Gültigkeits Bereichs des Verzeichnisses implementieren. Beispielsweise ist ein Entwickler von Sicherungs-und Wiederherstellungssoftware zum Erweitern eines Objekts mit dem Namen **Computer** vorgesehen. Der Entwickler muss zwei Methoden erstellen: **sichern** und **Wiederherstellen**. Diese Methoden arbeiten remote auf dem physischen Computer, auf den das **Computer** Objekt im Verzeichnis verweist. Durch das fungieren als Erweiterung greift die Komponente auf die ADSI-Infrastruktur zu und wird von ADSI-Clients als integraler Bestandteil des Objekts angezeigt.

In den folgenden Szenarien werden Situationen beschrieben, in denen das Erstellen einer Erweiterung für ADSI von Vorteil sein könnte:

-   Erstellen Sie eine Erweiterung, um eine Komponente in das Verzeichnis Objekt zu integrieren. Da es ein **Benutzer** Objekt im Verzeichnis gibt, möchte ein HR-Entwickler möglicherweise eine ADSI-Erweiterung erstellen, die andere Daten im Verzeichnis auffüllt, wenn ein **Benutzer** erstellt wird.
-   Erstellen Sie eine Erweiterung, wenn eine Komponente eine Verzeichnis Suche erfordert. Eine Komponente erfordert möglicherweise ein Verzeichnis als Ausgangspunkt für eine Suche. Beispielsweise beim Erstellen einer neuen Anwendung. Ein Anwendungs Objekt, **toolapp**, kann im Verzeichnis veröffentlicht werden. Die Anwendung unterstützt möglicherweise Status Benachrichtigungen für eine Sammlung von e-Mail-Servern. Sie beschließen, diese Anwendung zu einer ADSI-Erweiterung zu machen.

    Nun kann ein Benutzer im Verzeichnis nach allen Instanzen von **toolapp** suchen. Für jedes Objekt, das zurückgegeben wird, kann der Benutzer einen **callfynow-Rückruf ()** ausgeben. Eine Anwendung oder Erweiterung kann mehr aktuelle Objektdaten im Verzeichnis abrufen und jeden Server asynchron benachrichtigen.

-   Erstellen Sie eine Erweiterung als Verknüpfung zwischen Namespaces und Programmier Modellen. Ein ISV stellt z. b. ein neues Objektmodell für Druckdienste dar. Das **PrintQueue** -Objekt ist bereits im Verzeichnis definiert. Der ISV kann eine ADSI-Erweiterung erstellen und dem **PrintQueue** -Objekt zuordnen. ADSI-Benutzer können eine Bindung an ein **PrintQueue** -Objekt herstellen und mit der Verwendung des Objektmodells für den ISV beginnen. Aus der ADSI-Client Perspektive ist dieser Verknüpfungs Punkt transparent.
-   Erstellen Sie eine Erweiterung, um Aufgaben zu vereinfachen. Viele Tasks im Verzeichnis können durchsuchen und Festlegen mehrerer Attribute in einem Objekt oder mehreren Objekten erreicht werden. Durch das Erstellen einer einzelnen Funktion zum Bearbeiten mehrerer Attribute wird die Entwicklung für Anwendungs-und Skript Schreiber vereinfacht.

Bei ADSI-Clients erweitern Erweiterungen die ADSI-Programmierumgebung auf verschiedene Weise:

-   Entwickler, die ADSI-Clients erstellen, müssen kein neues Programmiermodell erlernen. Die Erweiterungen sind Teil von ADSI. Sie würden dasselbe Paradigma für die Suche, die Datenbearbeitung und das Sichern von Objekten verwenden.
-   Administratoren können verknüpfte Verzeichnis aktivierte Anwendungen mithilfe von Erweiterungen verwalten.
-   Erweiterungs Consumer können ein ADSI-Objekt und eine Erweiterung als ein integriertes Objekt anzeigen.
-   Vorhandene Komponenten können in ADSI integriert werden, wodurch Erweiterungen vorhandene Investitionen nutzen und Synergie zwischen Komponenten erstellen können.

ADSI-Erweiterungen wurden mit den folgenden Zielen entworfen:

-   Leicht zu implementieren. Mit den aktuellen vorhandenen Microsoft-Technologien, Microsoft Visual C++ Entwicklungssystem und Active Template Library kann eine Erweiterung schnell erstellt werden.
-   Clients zeigen eine IDispatch an. Aus der Perspektive von Skript-und Automatisierungs Writern werden die Erweiterungs Methoden und-Eigenschaften transparent in ein ADSI-Objekt gemischt.
-   Ständigen. Erweiterungs Schreiber können ADSI unabhängig von früheren Kenntnissen vorhandener Erweiterungen erweitern.

Beachten Sie dieses Szenario: ein Unternehmensentwickler oder ein ISV muss ein Sicherungsprogramm entwickeln. Diese Sicherungs Anwendung ermöglicht es einem Administrator, alle Computer in einer Organisationseinheit zu sichern. Mit der Erweiterung ADSI ist das folgende Skript möglich.


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



**LastBackup** ist eine Eigenschaft, und **backupnow** ist eine Methode, die der erweiterungswriter bereitstellt. Der Code zeigt die Vorteile für Erweiterungs Consumer und-Anbieter. Der erweiterungswriter muss keine neue Methode zum Filtern, suchen und Zugreifen auf das Verzeichnis erstellen. Der erweiterungsconsumer muss ein neues Programmierparadigma nicht erlernen. Neue Methoden und Eigenschaften, die der erweiterungswriter bereitstellt, werden als Teil von ADSI angezeigt.

 

 




