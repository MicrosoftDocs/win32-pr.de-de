---
title: Serialisierungshandles
description: Eine Anwendung verwendet die serialisierungsprozeduren oder die vom-Mittelwert generierten Unterstützungs Routinen in Verbindung mit einer Reihe von Bibliotheksfunktionen, um ein serialisierungshandle zu bearbeiten.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5585fc3f34b6cc826c1f8157bd59a144070ea081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037408"
---
# <a name="serialization-handles"></a>Serialisierungshandles

Eine Anwendung verwendet die serialisierungsprozeduren oder die vom-Mittelwert generierten Unterstützungs Routinen in Verbindung mit einer Reihe von Bibliotheksfunktionen, um ein serialisierungshandle zu bearbeiten. Zusammen bieten diese Funktionen einen Mechanismus zur Anpassung der Art und Weise, in der eine Anwendung Daten serialisiert.

Ein serialisierungshandle ist für einen Serialisierungsvorgang erforderlich, und alle serialisierenden Handles müssen explizit von Ihnen verwaltet werden. Zu diesem Zweck erstellen Sie zunächst ein gültiges Handle, indem Sie eine der folgenden Routinen aufrufen:

-   [**Mesdecodebufferlagercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**Mesdecodeinkrementallagercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**Mesencoentdynbufferlenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**Mesencodefixedbufferlenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**Mesencodeinkrementallenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Sie geben das Handle mit einem aufzurufenden [**messhandfree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)-Befehl frei. Nachdem das Handle erstellt oder erneut initialisiert wurde, stellt es einen gültigen Serialisierungskontext dar und kann verwendet werden, um je nach Typ des Handles codieren oder decodieren.

In diesem Abschnitt werden die serialisierungshandles und deren Verwendung in den folgenden Themen beschrieben:

-   [Implizite und explizite Handles](implicit-versus-explicit-handles.md)
-   [Serialisierungsstile](serialization-styles.md)
-   [Abrufen einer Codierungs Identität](obtaining-an-encoding-identity.md)

 

 




