---
title: Sichern und Wiederherstellen von DRM-Lizenzen
description: Sichern und Wiederherstellen von DRM-Lizenzen
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Medienformat-SDK, Sichern von DRM-Lizenzen
- Windows Medienformat-SDK, Wiederherstellen von DRM-Lizenzen
- Windows Medienformat-SDK, DRM-Lizenzen
- Windows Media Format SDK,Lizenzen für DRM
- Windows Medienformat-SDK, Sicherungswiederherstellungsfeature
- Windows Medienformat-SDK, Lizenzverwaltungsdienst
- Windows Medienformat-SDK, Betrugserkennung
- Digital Rights Management (DRM), Sichern von Lizenzen
- DRM (Digital Rights Management), Sichern von Lizenzen
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Wiederherstellen von Lizenzen
- DRM (Digital Rights Management), Wiederherstellen von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Sicherungswiederherstellungsfeature
- DRM (Digital Rights Management), Sicherungswiederherstellungsfeature
- Digital Rights Management (DRM), Lizenzverwaltungsdienst
- DRM (Digital Rights Management), Lizenzverwaltungsdienst
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Betrugserkennung
- DRM (Digital Rights Management), Betrugserkennung
- Sichern von DRM-Lizenzen
- Wiederherstellen von DRM-Lizenzen
- licenses,DRM
- Lizenzen,Sichern von DRM
- Lizenzen,Wiederherstellen von DRM
- Sicherungswiederherstellungsfeature
- Lizenzverwaltungsdienst
- Betrugserkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019163a42312b14b7d7b7e15cea68be1996a976e42b31491f62486a43d37b8bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028148"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Sichern und Wiederherstellen von DRM-Lizenzen

Mit dem Feature "Sicherungswiederherstellung" [](wmformat-glossary.md) können Benutzer Lizenzen auf demselben Computer oder auf anderen Computern sichern und wiederherstellen. Mit diesem Feature können Benutzer Lizenzen auf einen neuen Computer oder zurück auf denselben Computer übertragen (z. B. nach dem Neuformatieren der Festplatte). Darüber hinaus können Benutzer geschützte ASF-Dateien auf mehr als einem Computer wieder geben.

Um die legitime Verwendung einer Lizenz zu fördern, schränkt eine Richtlinie zur Betrugserkennung ein, wie oft eine Lizenz wiederhergestellt werden kann. Microsoft stellt einen Dienst zur Verfügung, der die Anzahl der Computer verfolgt, auf denen eine Lizenz wiederhergestellt wurde. Wenn ein Grenzwert erreicht wird, kann der Benutzer die Lizenz nicht wiederherstellen.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Zulassen oder Nicht-Zulassen des Rechts zum Sichern und Wiederherstellen

Das Feature "Sicherungswiederherstellung" funktioniert nur für Lizenzen, für die das Sicherungs- und Wiederherstellungsrecht erteilt wird. Wenn Inhaltsbesitzer oder Lizenzaussteller dieses Feature nicht wünschen oder Lizenzen mit einem sicheren Zustand (z. B. gezählte Vorgänge oder begrenzte Zeit) ausstellen, können sie dieses Recht nicht zusichern.

Wenn eine Lizenz nicht wiederhergestellt werden kann, weil ein Benutzer nicht über das Recht verfügt, wird eine [*Schlüssel-ID*](wmformat-glossary.md) an die Anwendung übergeben. Der Benutzer sollte mindestens darüber informiert werden, dass einige Lizenzen nicht sichern werden konnten, obwohl der Benutzer nicht weiß, auf welche Lizenzen sich diese Meldung bezieht. Wenn Sie die Schlüssel-ID für verfügbare geschützte Dateien kennen, können Sie eine stabilere Lösung für die Information des Benutzers entwickeln.

Beispielsweise könnte ein Player für eine Datensatzbezeichnung entwickelt werden, die geschützte Titel im Internet bietet. Diese Titel und ihre Schlüssel-IDs können in einer Datenbank nachverfolgt werden. Wenn einige Lizenzen nicht sichern konnten, könnte die Playeranwendung die Schlüssel-ID verwenden, um die Datenbank nach dem Namen der Titel zu fragen, und dann den Benutzer darüber informieren, für welche Titel die Lizenzen nicht sichern werden können. Oder es kann eine Musikbibliothek für jeden Benutzer lokal erstellt werden, und die Schlüssel-ID kann verwendet werden, um weitere Informationen darüber abzurufen, welche Lizenzen nicht sichern werden konnten.

## <a name="the-license-management-service"></a>Der Lizenzverwaltungsdienst

Wenn das Feature "Sicherungswiederherstellung" implementiert ist, verwaltet ein lizenzverwaltungsdienst, der von Microsoft gehostet wird, die Wiederherstellung von Lizenzen.

Zunächst sichern Benutzer Lizenzen in der Anwendung, indem sie beispielsweise eine Menüoption auswählen. Alle Lizenzen auf dem Computer werden an einem angegebenen Speicherort wie z. B. einem Diskettendatenträger gespeichert. Anschließend stellen Benutzer Lizenzen mithilfe der Anwendung wieder her, indem sie beispielsweise eine Menüoption auswählen und ihren Sicherungsspeicherort angeben.

An diesem Punkt muss der Benutzer mit dem Internet verbunden sein. Eine Anforderung von der Anwendung wird an den Lizenzverwaltungsdienst gesendet. Wenn sich der Computer, von dem die Lizenz sichern wurde, vom ursprünglichen Computer ab unterscheiden (oder der ursprüngliche Computer neu formatiert wurde), stellt der Lizenzverwaltungsdienst eine neue Lizenz für den neuen Computer aus. Andernfalls wird die Lizenz, die zuvor für diesen Computer ausgestellt wurde, erneut ausgestellt.

Da der Lizenzverwaltungsdienst Informationen vom Benutzer abruft, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der [Microsoft-Website bereitstellen.](https://www.microsoft.com/licensing/default)

> [!Note]  
> Wenn ein Endbenutzer eine Lizenz auf einem anderen Computer wiederhergestellt und die Lizenz individualisiert werden muss, muss der Endbenutzer die ZU aktualisierenden DRM-Komponenten autorisieren. Sie müssen einen Prozess in Ihrer Playeranwendung implementieren, um dieses Feature zu unterstützen.

 

## <a name="detecting-fraud"></a>Erkennen von Betrug

Der Benutzer darf eine Lizenz in einer begrenzten Anzahl wiederherstellen. Bei jeder Wiederherstellung einer Lizenz verfolgt der Lizenzverwaltungsdienst sie nach und erhöht die Anzahl für diese Lizenz um eins. Beim Wiederherstellen einer Lizenz auf einem Computer, auf dem die Lizenz zuvor wiederhergestellt wurde (z. B. auf dem Computer, auf dem die Lizenz gespeichert wurde), wird die Anzahl nicht erhöht. Ein Computer gilt als anders, wenn er über ein neues Betriebssystem verfügt oder das Betriebssystem neu installiert wurde.

In Übereinstimmung mit der Betrugserkennungsrichtlinie von Microsoft erhält die Anwendung eine URL von den DRM-Komponenten, wenn eine Lizenz mehrmals wiederhergestellt wurde, und ist dafür verantwortlich, einen Browser zu öffnen und die Webseite anzuzeigen, was darauf hinweist, dass der Lizenzvertrag möglicherweise verletzt wurde. Der Benutzer muss sich an den Lizenzverteiler wenden, der dann ermitteln muss, ob die Anforderung gültig ist.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**Sichern und Wiederherstellen von Lizenzen**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




