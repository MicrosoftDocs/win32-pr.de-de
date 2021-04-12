---
description: Um die Installer-Funktionalität zu aktivieren, muss eine Anwendung bei der Initialisierung eine Reihe von Funktionen aufzurufen.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Initialisieren einer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215697"
---
# <a name="initializing-an-application"></a>Initialisieren einer Anwendung

Um die Installer-Funktionalität zu aktivieren, muss eine Anwendung bei der Initialisierung eine Reihe von Funktionen aufzurufen. Weitere Informationen finden Sie unter [Installationsmechanismus](installation-mechanism.md). In den folgenden Schritten wird beschrieben, wie Sie mit dem Installationsprogramm eine Anwendung initialisieren:

**So initialisieren Sie eine Anwendung**

1.  Aufrufen der Funktion " [**msigetproductcode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) ", damit die Anwendung sich selbst beim Installer identifizieren kann.

    Der Produktcode ist ein erforderlicher Parameter für viele Installer-Funktionen.

2.  Rufen Sie die [**msigetuserinfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) -Funktion auf, um Benutzerinformationen beim ersten Start der Anwendung zu erfassen.

    Wenn der [**msigetuserinfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) -Rückruf fehlschlägt, rufen Sie die [**msicollectuserinfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) -Funktion auf, um Benutzerinformationen zu sammeln.

3.  Zeigen Sie ggf. eine Standardbenutzer Oberfläche an, indem Sie die [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) -Funktion aufrufen.

    Wenn Sie Ihre eigene Benutzeroberfläche erstellen möchten, registrieren Sie Sie beim Installer, indem Sie die Funktion [**msitentexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) aufrufen.

4.  Ruft die [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga) -Funktion auf, um den Protokolliergrad festzulegen.
5.  Stellen Sie dem Benutzer verfügbare Funktionen bereit, indem Sie die Funktionen der Anwendung auflisten. Sie können Funktionen wie folgt auflisten:
    -   Fragen Sie den Installer Feature-by-Feature ab. Bevor die Anwendung z. b. eine Schaltfläche oder ein Menü Element zeichnet, ruft die Anwendung die [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) -Funktion auf, damit das Installationsprogramm überprüfen kann, ob die Funktion verfügbar ist.
    -   Auflisten aller verfügbaren Features auf einmal durch Aufrufen der Funktion " [**msienumfeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) ". Um diese Funktion verwenden zu können, muss die Anwendung **msienumschlag-Features** wiederholt beim Inkrementieren eines Indexes aufruft.
6.  Rufen Sie ausführliche Informationen über die aktuelle Installation ab, indem Sie die folgenden Enumerationsfunktionen wiederholt aufrufen und eine Index Variable für jeden Aufruf erhöhen:

    -   Wenden Sie die Funktion " [**msienumproducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) " an, um beim Installer registrierte Produkte aufzuzählen.
    -   Zum Auflisten von Komponenten müssen Sie die Funktion [**msienumcomponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) aufzählen.
    -   Mit der Funktion " [**msienumcomponentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) " können Sie Komponenten Qualifizierer auflisten.
    -   Ruft die [**msienumclients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) -Funktion auf, um die Produkte für eine bestimmte Komponente aufzuzählen.

    Wenn der Rückgabewert einer Enumerationsfunktion ein Fehler \_ Erfolg ist, sind noch weitere Elemente aufzuzählen, und die Funktion sollte erneut mit einer inkrementierten Index Variable aufgerufen werden. Wenn der Rückgabewert fehlerhaft \_ ist \_ \_ , werden alle Elemente aufgezählt, und die Funktion sollte nicht erneut aufgerufen werden.

 

 



