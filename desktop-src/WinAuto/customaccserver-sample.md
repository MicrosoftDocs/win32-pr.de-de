---
title: Customaccserver-Beispiel
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389970"
---
# <a name="customaccserver-sample"></a>Customaccserver-Beispiel

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Download Informationen](#download-information)
-   [Mindestanforderungen](#minimum-requirements)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel wird gezeigt, wie ein Microsoft Active Accessibility Server für ein einfaches benutzerdefiniertes Steuerelement implementiert wird. Das barrierefreie Objekt für das-Steuerelement besteht aus dem Stamm Element (einem Listenfeld) und seinen untergeordneten Elementen (Listenelemente).

## <a name="download-information"></a>Download Informationen

Das customaccserver-Beispiel wird als Teil des [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) installiert und ist am folgenden Speicherort verfügbar.



| Standort    | Pfad/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | % Program Files% \\ Microsoft sdert \\ Windows- \\ \[ Versionsnummer \] \\ Beispiele \\ WinUI \\ MSAA |



 

## <a name="minimum-requirements"></a>Mindestanforderungen



| Produkt          | Version                         |
|------------------|---------------------------------|
| Betriebssystem | Windows XP, Windows Server 2003 |
| Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel mit Visual Studio 2008:

1.  Führen Sie das Microsoft Windows Software Development Kit (SDK)-Konfigurations Tool aus, das mit dem SDK bereitgestellt wird, um Visual Studio SDK include-Verzeichnisse hinzuzufügen.
2.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis.
3.  Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um das Projekt in Visual Studio zu öffnen.
4.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus, um die Projekt Mappe zu erstellen. Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.

Wenn Sie das Beispiel über die Befehlszeile erstellen möchten, finden Sie weitere Informationen unter Erstellen von Beispielen in den Anmerkungen zur Windows SDK-Version unter folgendem Speicherort:% Program Files% \\ Microsoft sdert \\ Windows \\ v 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie AccServer.exe in der Befehlszeile ein, oder Doppelklicken Sie auf das Symbol für AccServer.exe, um es im Windows-Explorer zu starten.

Um in Visual Studio auszuführen, drücken Sie F5, oder klicken Sie im Menü **Debuggen** auf **Debuggen starten** .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele](samples.md)
</dt> </dl>

 

 




