---
title: Programmier Handbuch für Benutzeroberflächen-Plug-ins
description: Programmier Handbuch für Benutzeroberflächen-Plug-ins
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Windows Media Player-Plug-ins
- Windows Media Player, Benutzerschnittstellen-Plug-ins
- Windows Media Player-Plug-ins, Benutzeroberfläche
- Plug-ins, Benutzeroberfläche
- Plug-Ins für die Benutzeroberfläche, Programmier Handbuch
- UI-Plug-ins, Programmier Handbuch
- Programmier Handbuch, Benutzerschnittstellen-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d417d246e92a642711e8cb02f77ff3795d47c995
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856484"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Programmier Handbuch für Benutzeroberflächen-Plug-ins

Die zwei in diesem Abschnitt beschriebenen Codebeispiele veranschaulichen den Prozess der Implementierung eines benutzerdefinierten Benutzeroberflächen-Plug-ins, beginnend mit dem Code, der vom Assistenten für Windows-Media Player-Plug-ins generiert wurde.

Das Such Benutzeroberflächen-Plug-in ist ein Metadatenbereich-Plug-in, das eine **Such** Schaltfläche bereitstellt. Wenn Sie auf diese Schaltfläche klicken, wird eine Suchseite im Standard Webbrowser gestartet, die Informationen über den Künstler des aktuellen Medien Elements enthält.

Der erste Schritt beim Erstellen dieses Plug-ins besteht darin, ein neues Projekt in Microsoft Visual C++ zu starten, indem Sie auf der Registerkarte **Projekte** die Option **Windows Media Player Plug-in-Assistent** auswählen. Nennen Sie das Projekt "Search", und klicken Sie auf **OK**. Wählen Sie **UI-Plug-in** , und klicken Sie auf **weiter**. Wählen Sie dann den Metadatentyp in der Liste Optionen aus, und klicken Sie auf **weiter**. Klicken Sie abschließend auf das Kontrollkästchen für die automatische Ausführung Unterstützung, damit das Plug-in automatisch geladen wird, und klicken Sie dann auf **Fertig** stellen. Der Assistent generiert die erforderlichen Projektdateien, einschließlich grundlegender Implementierungen der csearch-Klasse und der von ihm unterstützten **iwmppluginui** -Schnittstelle sowie der cpluginwindow-Klasse, die die Benutzeroberfläche bereitstellt. Dies ist der Code, der geändert wird, um die in diesem Abschnitt beschriebene Plug-in-Funktionalität bereitzustellen.

Im letzten Thema dieses Abschnitts wird beschrieben, wie ein Plug-in für die Benutzeroberfläche für Windows Media Player 10 Mobile erstellt wird. Dieses Plug-in verwendet geänderten Code, der vom Assistenten für Windows Media Player-Plug-in generiert wurde, um ein Plug-in für Windows Media Player 10 Mobile zu erstellen.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                                                                                            | BESCHREIBUNG                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementieren von csearch](implementing-csearch.md)                                                                                                 | Beschreibt die Änderungen, die für die csearch-Klasse erforderlich sind.                                |
| [Implementieren von cpluginwindow](implementing-cpluginwindow.md)                                                                                     | Beschreibt die Änderungen, die für die cpluginwindow-Klasse erforderlich sind.                          |
| [Erstellen eines Benutzeroberflächen-Plug-Ins für Windows Media Player 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Hier wird beschrieben, wie ein Plug-in für die Benutzeroberfläche für Windows Media Player 10 Mobile erstellt wird. |



 

 

 




