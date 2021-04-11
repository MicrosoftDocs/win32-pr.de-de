---
title: Aktualisieren von Lizenzen für Filialen mit dem PlaysForSure-Logo
description: Aktualisieren von Lizenzen für Filialen mit dem PlaysForSure-Logo
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player Online Stores, Aktualisieren von Lizenzen
- Online Stores, Lizenz Aktualisierung
- Windows Media Player Online Stores, Lizenz Aktualisierung
- Online Stores, Aktualisieren von Lizenzen
- Windows Media Player Online Stores, PlaysForSure-Logo
- Online Stores, PlaysForSure-Logo
- Aktualisieren von Lizenzen
- Lizenzen, aktualisieren
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101290"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>Aktualisieren von Lizenzen für Filialen mit dem PlaysForSure-Logo

Bestimmte Online-Musikspeicher verfügen über das PlaysForSure-Logo, sind aber nicht in Windows Media Player 11 integriert. Diese Speicher müssen ein serviceInfo-Dokument und eine Lightweight-Komponente bereitstellen, damit Windows Media Player 11 Lizenzen für Ihre Inhalte abrufen und aktualisieren kann.

Im folgenden Beispiel wird veranschaulicht, wie der Lizenz Aktualisierungsprozess funktioniert.

1.  Der Benutzer erhält 50 Musiktitel aus dem Proseware Online Store. Jede Spur ist eine Datei mit der Dateinamenerweiterung ". wma". Zusammen mit den Spuren erhält der Benutzerlizenzen, um die Spuren zu spielen.
2.  Der Benutzer kopiert die 50-Spuren auf einen neuen Computer, auf dem Windows Media Player 11 installiert ist, und fügt die Spuren der Windows Media Player-Bibliothek hinzu.
3.  Zu einem späteren Zeitpunkt überprüft das License Refresh Module (LRM), das Teil von Windows Media Player 11 ist, die Metadaten in den 50-Spuren und bestimmt, dass Proseware der Inhaltsanbieter ist.
    > [!Note]  
    > In Windows Media Player kann der Inhaltsanbieter identifiziert werden, indem das **contentdistributor** -Attribut in einer Mediendatei überprüft wird. Wenn ein Online Shop mit dem PlaysForSure-Logo eine Mediendatei bereitstellt, die Windows Media Digital Rights Management (WMDRM) verwendet, muss der Onlinespeicher das **contentdistributor** -Attribut in der Mediendatei platzieren. Weitere Informationen finden Sie unter Hinzufügen des Content Distributor-Attributs im Windows Media Player SDK.

     

4.  Die LRM sucht nach der URL des serviceInfo-Dokuments von Proseware, lädt das Dokument herunter und überprüft das **install** -Element des Dokuments, um die URL eines Pakets abzurufen, das von der LRM zum Installieren der Komponente von Proseware verwendet werden kann. Der LRM installiert und lädt die Komponente.
5.  Für jede der 50-Spuren Ruft die LRM die [iwmpabonneptionservice:: allowplay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) -Methode der Proseware-Komponente auf. Mit der **allowplay** -Methode wird eine Lizenz für den einzelnen Titel auf dem neuen Computer platziert, und der Parameter " *pfallowplay* " gibt " **true** " zurück.
    > [!Note]  
    > Die Proseware-Komponente muss alle Lizenzen bereitstellen, die für die Wiedergabe der einzelnen Spur erforderlich sind. Das heißt, die Komponente muss bei Bedarf sowohl eine Stamm Lizenz als auch eine Blatt Lizenz bereitstellen.

     

    Beim ersten Aufrufen der **allowplay** -Methode muss die Proseware-Komponente ein Dialogfeld anzeigen, um zu überprüfen, ob der aktuelle Benutzer über ein Proseware-Konto verfügt und über das Recht zum Wiedergeben des Titels verfügt. Bei nachfolgenden Aufrufen von **allowplay** kann die Komponente die Anmelde Informationen verwenden, die im ersten Aufruf abgerufen wurden, um zu überprüfen, ob der Benutzer über das Recht zum Wiedergeben der restlichen Spuren verfügt.

Die Komponente, die vom Online Store geschrieben wird, muss die **allowplay** -Methode der **iwmpabonneptionservice** -Schnittstelle implementieren. Die Komponente muss E \_ notimpl von jeder der drei folgenden Methoden zurückgeben: **allowcdburn**, **allowpdatransfer** und **startbackgroundprocessing**. Außerdem muss die Komponente den Wert des Registrierungs Eintrags " **Funktionen** " auf "1" festlegen. Das heißt, dass das Abonnement \_ Cap \_ -allowplay-funktionsflag festgelegt werden muss, und alle anderen funktionsflags müssen gelöscht werden. Weitere Informationen zum Registrieren der Komponente finden Sie unter [Registrierungsschlüssel und Einträge für den Online Store vom Typ 2](registry-keys-and-entries-for-a-type-2-online-store.md).

Informationen zum Erstellen einer Komponente, die die **iwmpabonneptionservice** -Schnittstelle implementiert, finden Sie unter [Erstellen des Plug-Ins für einen Typ 2-Online Store](building-the-plug-in-for-a-type-2-online-store.md).

Um Informationen zur Bereitstellung von Microsoft mit einem serviceInfo-Dokument zu erhalten, senden Sie eine e-Mail an das Windows Media Player Virtual Services-Team. Die e-Mail-Adresse des Teams lautet mpsvctm@microsoft.com .

Technische Anleitungen zur Verwendung einer Vielzahl von Windows Media SDOs zum Erstellen eines Dienstanbieter, der lizenzierte Digital Media-Inhalte bietet, finden Sie im [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) , und suchen Sie nach "Erstellen eines Windows Media Player 10-Abonnements Online Store".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> <dt>

[**Windows Media Player Online Stores**](windows-media-player-online-stores.md)
</dt> </dl>

 

 




