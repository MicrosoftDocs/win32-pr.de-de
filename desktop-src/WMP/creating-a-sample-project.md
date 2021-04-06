---
title: Erstellen eines Beispielprojekts
description: Erstellen eines Beispielprojekts
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player Online Stores, Erstellen von Beispielprojekten
- Online Stores, Erstellen von Beispielprojekten
- Typ 2 Online Stores, Erstellen von Beispielprojekten
- Windows Media Player Online Stores, Beispiel Projekte
- Online Stores, Beispiel Projekte
- Typ 2 Online Stores, Beispiel Projekte
- Windows Media Player Online Stores, Projekt-Assistent
- Online Stores, Projekt-Assistent
- Typ 2 Online Stores, Projekt-Assistent
- Plug-ins, Projekt-Assistent
- Windows Media Player-Plug-ins, Projekt-Assistent
- Erstellen von Beispielprojekten
- Beispiele, Typ 2 Online Stores
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104101326"
---
# <a name="creating-a-sample-project"></a>Erstellen eines Beispielprojekts

Führen Sie die folgenden Schritte aus, um ein neues Projekt mit dem Projekt-Assistenten zu erstellen:

1.  Öffnen Sie Microsoft Visual Studio.
2.  Zeigen Sie im Menü **Datei** auf **Neu**, und klicken Sie dann auf **Projekt**.
3.  Wählen Sie im Listenfeld **Projekttypen** die Option **Visual C++ Projekte** aus.
4.  Wählen Sie im Listenfeld **Vorlagen** die Option **Windows Media Player Online Stores-Assistent** aus.
5.  Geben Sie einen Namen und einen Speicherort für das Projekt ein.
6.  Klicken Sie auf **OK** , um den Projektassistenten zu starten.
7.  Wählen Sie **Typ 2 (grundlegende Integration)** aus, und klicken Sie auf **weiter**.
8.  Geben Sie den anzeigen Amen und die Inhalts Verteiler-ID für den Dienst ein. Geben Sie die URL für die Webseite ein, die den Dienst vom Computer des Benutzers entfernt.
    > [!Note]  
    > Der Wert, den Sie für die ID des Inhalts Verteilers angeben, darf keine Leerzeichen enthalten. Der Assistent entfernt alle Leerzeichen aus der von Ihnen bereitgestellten Zeichenfolge.

     

9.  Klicken Sie auf **Fertig stellen**, um das Projekt zu erstellen.

Der Assistent generiert automatisch ein neues C++-Projekt, das ein Type 2 Online Store-Plug-in erstellt, das die **iwmpabonneptionservice** -und **IWMPSubscriptionService2** -Schnittstellen implementiert. Jedes Mal, wenn Sie den Assistenten ausführen, wird das gleiche Projekt erstellt, aber die Komponente, die beim Kompilieren des Projekts erstellt wird, verfügt über eine eindeutige Klassen-ID. Der Projektname, der Anzeige Name und die Inhalts Verteiler-ID können sich auch je nach den Werten unterscheiden, die Sie beim Durchlaufen des Assistenten angegeben haben. Das Beispiel Projekt registriert die Komponente unter Verwendung eines Schlüssel namens, der mit dem Wert übereinstimmt, den Sie für den anzeigen Amen angegeben haben.

Im Beispiel wird Active Template Library (ATL)-Code verwendet, um com-Implementierungen bereitzustellen.

Der Assistent erstellt die folgenden Dateien:

-   *ProjectName* dll. cpp. Implementiert die DLL-Exporte (Dynamic Link Library), wie z. b. die Haupt-DLL-Einstiegspunkt Funktion. Enthält auch die ATL-Objekt Zuordnung und die Modul Deklaration.
-   *ProjectName*. cpp. Enthält Standard Implementierungen für die Methoden der iwmpabonneptionservice-und IWMPSubscriptionService2-Schnittstellen. Enthält auch Code zum Definieren der Dialogfelder, die das Beispiel öffnet, wenn Methoden von Windows Media Player aufgerufen werden.
-   *ProjectName*. def. Deklariert die DLL-Exporte.
-   Stdafx. cpp. Schließt Standard Header ein.
-   WMP. h. Die Windows-Media Player Header Datei.
-   wmpplug. h. Die Windows Media Player-Plug-in-Header Datei.
-   Abonnement Services. h. Die Header Datei des Windows Media Player Online Stores.
-   Resource. h. Enthält Ressourcen Definitionen.
-   **ProjectName**. h. Enthält Klassendefinitionen für das Onlinespeicher Objekt und die Dialogfelder. Definiert die Klassen-ID des Objekts und die ID-Konstante des Inhalts Verteilers.
-   Stdafx. h. Enthält Standardsystem-includes.
-   *ProjectName*. rc. Die Ressourcen Skriptdatei. Diese enthält Definitionen für die Dialogfeld Ressourcen und Steuerelemente. An dieser Stelle wird auch die Zeichen folgen Tabelle gespeichert. Die Zeichen folgen Tabelle enthält den Projektnamen und die Zeichen folgen Konstanten für den anzeigen Amen. Normalerweise arbeiten Sie mit dieser Datei im Ressourcen-Editor von Visual Studio, nicht als Klartext.
-   *ProjectName*. rgs. Die Registrierungs Skriptdatei. Diese Datei enthält die Informationen, die verwendet werden, um die Komponenten Klasse zur Registrierung hinzuzufügen, damit Windows Media Player Sie finden kann. Sie können den Schlüsselnamen für Ihren Dienst in dieser Datei ändern.

> [!Note]  
> Sie sollten die Basisadresse für die dll auf 0x0f100000 festlegen, um Konflikte mit Windows-Media Player zu vermeiden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwickeln des Plug-Ins für einen Typ 2-Online Store**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**Iwmpabonneptionservice-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




