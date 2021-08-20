---
title: Programmierhandbuch für Benutzeroberfläche Plug-Ins
description: Programmierhandbuch für Benutzeroberfläche Plug-Ins
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Windows Media Player, Plug-Ins
- Windows Media Player, Benutzeroberflächen-Plug-Ins
- Windows Media Player-Plug-Ins, Benutzeroberfläche
- Plug-Ins, Benutzeroberfläche
- Benutzeroberflächen-Plug-Ins, Programmierhandbuch
- UI-Plug-Ins, Programmierhandbuch
- Programmierhandbuch, Benutzeroberflächen-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcba6c3c7218e504a2e8752a4d1680e4887ec5aa7bfa69744fab00b27cbee797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831480"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Programmierhandbuch für Benutzeroberfläche Plug-Ins

Die beiden in diesem Abschnitt beschriebenen Codebeispiele veranschaulichen den Prozess der Implementierung eines benutzerdefinierten Benutzeroberflächen-Plug-Ins, beginnend mit Code, der vom Assistenten für Windows Media Player Plug-Ins generiert wird.

Das Plug-In für die Benutzeroberfläche für die Suche ist ein Metadatenbereichs-Plug-In, das die Schaltfläche **Suchen** bereitstellt. Wenn auf diese Schaltfläche geklickt wird, wird im Standardwebbrowser eine Suchseite gestartet, die Informationen zum Interpreten des aktuellen Medienelements enthält.

Der erste Schritt beim Erstellen dieses Plug-Ins besteht darin, ein neues Projekt in Microsoft Visual C++ zu starten, indem Sie **Windows Media Player Plug-In-Assistenten auf** der Registerkarte **Projekte** auswählen. Nennen Sie das Projekt "Search", und klicken Sie auf **OK.** Wählen Sie **UI-Plug-In** aus, und klicken Sie auf **Weiter.** Wählen Sie dann den Metadatentyp aus der Optionsliste aus, und klicken Sie auf **Weiter.** Klicken Sie abschließend auf das Kontrollkästchen für automatische Ausführungsunterstützung, damit das Plug-In automatisch geladen wird, und klicken Sie dann auf **Fertig stellen.** Der Assistent generiert die erforderlichen Projektdateien, einschließlich der grundlegenden Implementierungen der CSearch-Klasse und der **unterstützten IWMPPluginUI-Schnittstelle** sowie der CPluginWindow-Klasse, die die Benutzeroberfläche bereitstellt. Dies ist der Code, der geändert wird, um die in diesem Abschnitt beschriebenen Plug-In-Funktionen bereitzustellen.

Im letzten Thema dieses Abschnitts wird beschrieben, wie Sie ein Hintergrund-UI-Plug-In für Windows Media Player 10 Mobile erstellen. Dieses Plug-In verwendet geänderten Code, der vom Assistenten für Windows Media Player Plug-Ins generiert wurde, um ein Plug-In für Windows Media Player 10 Mobile zu erstellen.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                                                                                            | Beschreibung                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementieren von CSearch](implementing-csearch.md)                                                                                                 | Beschreibt die an der CSearch-Klasse erforderlichen Änderungen.                                |
| [Implementieren von CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Beschreibt die an der CPluginWindow-Klasse erforderlichen Änderungen.                          |
| [Erstellen eines Benutzeroberfläche-Plug-Ins für Windows Media Player 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Beschreibt das Erstellen eines Hintergrund-UI-Plug-Ins für Windows Media Player 10 Mobile. |



 

 

 




