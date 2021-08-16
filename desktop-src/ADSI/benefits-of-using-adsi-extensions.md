---
title: Vorteile der Verwendung von ADSI-Erweiterungen
description: Die Art und Weise, wie Erweiterungsmethoden implementiert werden, hängt vom Erweiterungswriter ab.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a680e1eefbc05dac84b3420bee23287eda2bd02325274532109544b04ff73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018143"
---
# <a name="benefits-of-using-adsi-extensions"></a>Vorteile der Verwendung von ADSI-Erweiterungen

Die Art und Weise, wie Erweiterungsmethoden implementiert werden, hängt vom Erweiterungswriter ab. Ein Erweiterungswriter kann sogar eine Methode implementieren, die sich vollständig außerhalb des Bereichs des Verzeichnisses befindet. Ein Entwickler von Sicherungs- und Wiederherstellungssoftwareplänen beispielsweise, um ein Objekt namens Computer zu **erweitern.** Der Entwickler muss zwei Methoden erstellen: **BackUp** und **Restore.** Diese Methoden arbeiten remote auf dem physischen Computer, auf den **das Computerobjekt** im Verzeichnis verweist. Indem sie als Erweiterung agiert, greifen sie auf die ADSI-Infrastruktur zu und werden von ADSI-Clients als integraler Bestandteil des Objekts angezeigt.

In den folgenden Szenarien werden Situationen beschrieben, in denen das Erstellen einer Erweiterung für ADSI von Vorteil wäre:

-   Erstellen Sie eine Erweiterung, um eine Komponente in das Verzeichnisobjekt zu integrieren. Da im Verzeichnis ein **Benutzerobjekt** vorhanden ist, möchte ein HR-Entwickler möglicherweise eine ADSI-Erweiterung erstellen, die andere Daten im Verzeichnis auffüllt, wenn ein **Benutzer** erstellt wird.
-   Erstellen Sie eine Erweiterung, wenn eine Komponente eine Verzeichnissuche erfordert. Eine Komponente erfordert möglicherweise ein Verzeichnis als Ausgangspunkt für eine Suche. Zum Beispiel beim Erstellen einer neuen Anwendung. Ein Anwendungsobjekt, **ToolApp,** kann im Verzeichnis veröffentlicht werden. Ihre Anwendung unterstützt möglicherweise Statusbenachrichtigungen auf einer Sammlung von E-Mail-Servern. Sie entscheiden sich dafür, diese Anwendung zu einer ADSI-Erweiterung zu machen.

    Jetzt kann ein Benutzer nach allen Instanzen von **ToolApp** im Verzeichnis suchen. Für jedes zurückgegebene Objekt kann der Benutzer einen Aufruf von **NotifyNow() aus.** Eine Anwendung oder Erweiterung kann aktuellere Objektdaten im Verzeichnis abrufen und jeden Server asynchron benachrichtigen.

-   Erstellen Sie eine Erweiterung als Verbindung zwischen Namespaces und Programmiermodellen. Ein ISV erfindet beispielsweise ein neues Objektmodell für Druckdienste. Das **printQueue-Objekt** ist bereits im Verzeichnis definiert. Der ISV kann eine ADSI-Erweiterung erstellen und sie dem **printQueue-Objekt** zuordnen. ADSI-Benutzer können eine Bindung an ein **printQueue-Objekt** erstellen und mit der Verwendung des Objektmodells für den ISV beginnen. Aus Sicht des ADSI-Clients ist dieser Verbindungspunkt transparent.
-   Erstellen Sie eine Erweiterung, um Aufgaben zu vereinfachen. Viele Aufgaben im Verzeichnis können durch Suchen und Festlegen mehrerer Attribute in einem Objekt oder mehreren Objekten ausgeführt werden. Durch das Erstellen einer einzelnen Funktion zum Bearbeiten mehrerer Attribute wird die Entwicklung für Anwendungs- und Skriptautoren vereinfacht.

Für ADSI-Clients erweitern Erweiterungen die ADSI-Programmierumgebung auf verschiedene Arten:

-   Entwickler, die ADSI-Clients erstellen, müssen kein neues Programmiermodell erlernen. Die Erweiterungen sind Teil von ADSI. Sie würden dasselbe Paradigma zum Suchen, Ändern von Daten und Sichern von Objekten verwenden.
-   Administratoren können verwandte verzeichnisfähige Anwendungen mithilfe von Erweiterungen verwalten.
-   Erweiterungsverbraucher können ein ADSI-Objekt und eine Erweiterung als ein integriertes Objekt anzeigen.
-   Vorhandene Komponenten können in ADSI integriert werden, wodurch Erweiterungen vorhandene Investitionen nutzen und eine Verbindung zwischen den Komponenten schaffen können.

ADSI-Erweiterungen wurden mit den folgenden Zielen entwickelt:

-   Einfach zu implementieren. Mit den aktuellen microsoft-Technologien, Microsoft Visual C++ Entwicklungssystem und dem Active Template Library kann schnell eine Erweiterung erstellt werden.
-   Clients zeigen ein IDispatch an. Aus Sicht von Skript- und Automatisierungsautoren werden die Erweiterungsmethoden und -eigenschaften transparent in ein ADSI-Objekt gemischt.
-   Unabhängig. Erweiterungsautoren können ADSI unabhängig erweitern, ohne zuvor über vorhandene Erweiterungen zu wissen.

Stellen Sie sich dieses Szenario vor: Ein Unternehmensentwickler oder isv muss ein Sicherungsprogramm entwickeln. Mit dieser Sicherungsanwendung kann ein Administrator alle Computer in einer Organisationseinheit sichern. Bei einer ADSI-Erweiterung ist das folgende Skript möglich.


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



**LastBackUp ist** eine Eigenschaft, **und BackUpNow** ist eine Methode, die der Erweiterungswriter bietet. Der Code zeigt die Vorteile sowohl für Erweiterungsverbraucher als auch für Anbieter. Der Erweiterungswriter muss keine neue Methode zum Filtern, Suchen und Zugreifen auf das Verzeichnis erstellen. Der Erweiterungsverbraucher muss kein neues Programmierparadigma neu programmieren. Neue Methoden und Eigenschaften, die der Erweiterungswriter bietet, werden als Teil von ADSI angezeigt.

 

 




