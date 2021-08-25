---
title: CustomAccServer-Beispiel
description: CustomAccServer-Beispiel
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ebf1ecde2821208d788b20b5cb0fc1a00403c1607fb4604eb92845daf49d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325989"
---
# <a name="customaccserver-sample"></a>CustomAccServer-Beispiel

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Herunterladen von Informationen](#download-information)
-   [Mindestanforderungen](#minimum-requirements)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>Beschreibung

In diesem Beispiel wird gezeigt, wie sie einen Microsoft Active Accessibility server für ein einfaches benutzerdefiniertes Steuerelement implementieren. Das barrierefreie Objekt für das Steuerelement besteht aus dem Stammelement (einem Listenfeld) und seinen unteren Elementen (den Listenelementen).

## <a name="download-information"></a>Herunterladen von Informationen

Das CustomAccServer-Beispiel wird als Teil des [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) installiert und ist an folgendem Speicherort verfügbar.



| Standort    | Pfad/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | %Program Files% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ msaa |



 

## <a name="minimum-requirements"></a>Mindestanforderungen



| Produkt          | Version                         |
|------------------|---------------------------------|
| Betriebssystem | Windows XP, Windows Server 2003 |
| Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel mit Visual Studio 2008:

1.  Führen Sie das im SDK Windows Microsoft Windows Software Development Kit (SDK) bereitgestellte Konfigurationstool aus, um SDK-Includeverzeichnisse zu Visual Studio.
2.  Öffnen Windows Explorer, und navigieren Sie zum Projektverzeichnis.
3.  Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappe), um das Projekt in Visual Studio.
4.  Wählen Sie **im Menü Erstellen** die Option **Projektmappe erstellen aus,** um die Projektmappe zu erstellen. Die Anwendung wird im Standardverzeichnis \\ Debuggen oder \\ Release erstellt.

Informationen zum Erstellen des Beispiels über die Befehlszeile finden Sie unter Building Samples in the Windows SDK release notes at the following location: %Program Files% \\ Microsoft SDKs \\ Windows \\ v7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie über die Eingabeaufforderung oder den Explorer zu dem Verzeichnis, das die neue ausführbare Windows enthält.
2.  Geben AccServer.exe Befehlszeile ein, oder doppelklicken Sie auf das Symbol für AccServer.exe, um es über den Windows starten.

Drücken Sie F5 Visual Studio debuggen starten, oder klicken Sie im Menü Debuggen auf **Debuggen** starten, um die Ausführung über Visual Studio ausführen. 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele](samples.md)
</dt> </dl>

 

 




