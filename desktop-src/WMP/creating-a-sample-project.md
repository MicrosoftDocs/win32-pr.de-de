---
title: Erstellen eines Beispiel-Project
description: Erstellen eines Beispiel-Project
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player Onlineshops, Erstellen von Beispielprojekten
- Onlineshops, Erstellen von Beispielprojekten
- Geben Sie 2 Onlineshops ein, und erstellen Sie Beispielprojekte.
- Windows Media Player Onlineshops, Beispielprojekte
- Onlineshops, Beispielprojekte
- Geben Sie 2 Onlineshops ein, Beispielprojekte.
- Windows Media Player Onlineshops, Projekt-Assistent
- Onlineshops, Projekt-Assistent
- Typ 2 Onlineshops, Projekt-Assistent
- Plug-Ins, Projekt-Assistent
- Windows Media Player-Plug-Ins, Projekt-Assistent
- Erstellen von Beispielprojekten
- Beispiele, Geben Sie 2 Onlineshops ein.
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58af81123e257a7f71ad4be00e44c671f8ca3fa6f61b3719cd02ae1f928b7ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579936"
---
# <a name="creating-a-sample-project"></a>Erstellen eines Beispiel-Project

Führen Sie die folgenden Schritte aus, um mithilfe des Projekt-Assistenten ein neues Projekt zu erstellen:

1.  Öffnen Sie Microsoft Visual Studio.
2.  Zeigen Sie im Menü **Datei** auf **Neu**, und klicken Sie dann auf **Projekt**.
3.  Wählen Sie im Listenfeld **Project Typen** **Visual C++ Projekte** aus.
4.  Wählen Sie im Listenfeld **Vorlagen** **Windows Media Player Assistenten für Onlineshops aus.**
5.  Geben Sie einen Namen und einen Speicherort für Ihr Projekt ein.
6.  Klicken Sie auf **OK,** um den Projekt-Assistenten zu starten.
7.  Wählen Sie **Typ 2 (Grundlegende Integration)** aus, und klicken Sie auf **Weiter.**
8.  Geben Sie den Anzeigenamen und die Inhaltsverteiler-ID für Ihren Dienst ein. Geben Sie die URL für die Webseite ein, die den Dienst vom Computer des Benutzers entfernt.
    > [!Note]  
    > Der Wert, den Sie für die Inhaltsverteiler-ID angeben, darf keine Leerzeichen enthalten. Der Assistent entfernt alle Leerzeichen aus der zeichenfolge, die Sie angeben.

     

9.  Klicken Sie auf **Fertig stellen**, um das Projekt zu erstellen.

Der Assistent generiert automatisch ein neues C++-Projekt, das ein Onlineshop-Plug-In vom Typ 2 erstellt, das die Schnittstellen **IWMPSubscriptionService** und **IWMPSubscriptionService2** implementiert. Jedes Mal, wenn Sie den Assistenten ausführen, wird dasselbe Projekt erstellt, aber die Komponente, die beim Kompilieren des Projekts erstellt wird, verfügt über eine eindeutige Klassen-ID. Der Projektname, der Anzeigename und die Inhaltsverteiler-ID können je nach den Werten, die Sie beim Ausführen des Assistenten angegeben haben, ebenfalls unterschiedlich sein. Das Beispielprojekt registriert die Komponente mithilfe eines Schlüsselnamens, der dem Wert entspricht, den Sie für den Anzeigenamen angegeben haben.

Im Beispiel wird ATL-Code (Active Template Library) verwendet, um COM-Implementierungen bereitzustellen.

Der Assistent erstellt die folgenden Dateien für Sie:

-   *ProjectName* dll.cpp. Implementiert die DLL-Exporte (Dynamic Link Library), z. B. die Hauptfunktion des DLL-Einstiegspunkts. Enthält auch die ATL-Objektzuordnung und die Moduldeklaration.
-   *ProjectName*.cpp. Enthält Standardimplementierungen für die Methoden der Schnittstellen IWMPSubscriptionService und IWMPSubscriptionService2. Enthält auch Code zum Definieren der Dialogfelder, die im Beispiel geöffnet werden, wenn Methoden von Windows Media Player aufgerufen werden.
-   *ProjectName*.def. Deklariert die DLL-Exporte.
-   StdAfx.cpp. Enthält Standardheader.
-   wmp.h. Die Windows Media Player Headerdatei.
-   wmpplug.h. Die Windows Media Player Plug-In-Headerdatei.
-   subscriptionservices.h. Die Headerdatei des Windows Media Player Onlinespeichers.
-   resource.h. Enthält Ressourcendefinitionen.
-   **ProjectName**.h. Enthält Klassendefinitionen für das Onlineshopobjekt und die Dialogfelder. Definiert die Klassen-ID des Objekts und die Inhaltsverteiler-ID-Konstante.
-   StdAfx.h. Enthält Standardsystem-Includes.
-   *ProjectName*.rc. Die Ressourcenskriptdatei. Dies enthält Definitionen für die Dialogfeldressourcen und -steuerelemente. Hier wird auch die Zeichenfolgentabelle gespeichert. Die Zeichenfolgentabelle enthält den Projektnamen und die Anzeigenamen-Zeichenfolgenkonstanten. Normalerweise arbeiten Sie mit dieser Datei im Visual Studio Ressourcen-Editor, nicht als Nur-Text.
-   *ProjectName*.rgs. Die Registrierungsskriptdatei. Diese Datei enthält die Informationen, die zum Hinzufügen ihrer Komponentenklasse zur Registrierung verwendet werden, damit Windows Media Player sie finden können. Sie können den Schlüsselnamen für Ihren Dienst in dieser Datei ändern.

> [!Note]  
> Sie sollten die Basisadresse für Ihre DLL auf 0x0F100000 festlegen, um Konflikte mit Windows Media Player zu vermeiden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen des Plug-Ins für einen Typ 2 Online Store**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**IWMPSubscriptionService-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




