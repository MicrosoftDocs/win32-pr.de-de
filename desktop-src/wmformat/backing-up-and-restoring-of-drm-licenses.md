---
title: Sichern und Wiederherstellen von DRM-Lizenzen
description: Sichern und Wiederherstellen von DRM-Lizenzen
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media-Format-SDK, Sichern von DRM-Lizenzen
- Windows Media Format SDK, Wiederherstellen von DRM-Lizenzen
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Windows Media-Format-SDK, Sicherungs Wiederherstellungs Feature
- Windows Media-Format-SDK, Lizenz Verwaltungsdienst
- Windows Media-Format-SDK, Betrugserkennung
- Digital Rights Management (DRM), Sichern von Lizenzen
- DRM (Digital Rights Management), Sichern von Lizenzen
- Digital Rights Management (DRM), Wiederherstellen von Lizenzen
- DRM (Digital Rights Management), Wiederherstellen von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Sicherungs Wiederherstellungs Feature
- DRM (Digital Rights Management), Sicherungs Wiederherstellungs Feature
- Digital Rights Management (DRM), Lizenz Verwaltungsdienst
- DRM (Digital Rights Management), Lizenz Verwaltungsdienst
- Digital Rights Management (DRM), Betrugserkennung
- DRM (Digital Rights Management), Betrugserkennung
- Sichern von DRM-Lizenzen
- Herstellen von DRM-Lizenzen
- Lizenzen, DRM
- Lizenzen, Sichern von DRM
- Lizenzen, Wiederherstellen von DRM
- Sicherungs Wiederherstellungs Feature
- Lizenz Verwaltungsdienst
- Betrugserkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104316652"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Sichern und Wiederherstellen von DRM-Lizenzen

Mit dem Feature für die Sicherungs Wiederherstellung können Benutzer [*Lizenzen*](wmformat-glossary.md) auf demselben Computer oder auf anderen Computern sichern und wiederherstellen. Diese Funktion ermöglicht es Benutzern, Lizenzen auf einen neuen Computer oder zurück an denselben Computer zu übertragen (z. b. nach dem erneuten Formatieren der Festplatte). Außerdem können Benutzer geschützte ASF-Dateien auf mehr als einem Computer wiedergeben.

Um die legitime Verwendung einer Lizenz zu fördern, schränkt eine Richtlinie zur Betrugserkennung ein, wie oft eine Lizenz wieder hergestellt werden kann. Microsoft stellt einen Dienst bereit, mit dem die Anzahl der Computer nachverfolgt wird, auf denen eine Lizenz wieder hergestellt wurde. Wenn ein Grenzwert erreicht wird, kann der Benutzer die Lizenz nicht wiederherstellen.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Zulassen oder Deaktivieren der Berechtigung zum Sichern und Wiederherstellen

Die Sicherungs Wiederherstellungs Funktion funktioniert nur für Lizenzen, für die das Sicherungs-und Wiederherstellungs Recht erteilt wurde. Wenn Inhalts Besitzer oder Lizenz Aussteller diese Funktion nicht wünschen oder wenn Sie Lizenzen ausstellen, die einen sicheren Zustand (z. b. gezählte Vorgänge oder begrenzte Zeit) enthalten, können Sie dieses Recht nicht zulassen.

Wenn eine Lizenz nicht wieder hergestellt werden kann, weil ein Benutzer nicht über das Recht verfügt, wird eine [*Schlüssel-ID*](wmformat-glossary.md) an die Anwendung übermittelt. Der Benutzer sollte mindestens benachrichtigt werden, dass einige Lizenzen nicht gesichert werden konnten, obwohl der Benutzer nicht weiß, auf welche Lizenzen diese Nachricht verweist. Wenn Sie die Schlüssel-ID für verfügbare geschützte Dateien kennen, können Sie eine stabilere Lösung für die Information des Benutzers entwickeln.

Beispielsweise könnte ein Player für eine Daten Satz Bezeichnung entwickelt werden, die geschützte Lieder im Internet bereitstellt. Diese Lieder und Ihre Schlüssel-IDs können in einer Datenbank nachverfolgt werden. Wenn einige Lizenzen nicht gesichert werden konnten, könnte die Player Anwendung die Schlüssel-ID verwenden, um die Datenbank nach dem Namen der Lieder abzufragen, und dann den Benutzer darüber informieren, welche Lieder nicht gesichert werden können. Oder eine Musikbibliothek kann für jeden Benutzer lokal erstellt werden, und die Schlüssel-ID kann verwendet werden, um weitere Informationen darüber abzurufen, welche Lizenzen nicht gesichert werden konnten.

## <a name="the-license-management-service"></a>Der Lizenz Verwaltungsdienst

Wenn die Sicherungs Wiederherstellungs Funktion implementiert ist, verwaltet ein von Microsoft gehosteter Lizenz Verwaltungsdienst die Wiederherstellung von Lizenzen.

Zuerst sichern Benutzerlizenzen in der Anwendung, z. b. durch Auswahl einer Menüoption. Alle Lizenzen auf dem Computer werden an einem angegebenen Speicherort, z. b. einer Diskette, gesichert. Anschließend stellen Benutzerlizenzen mithilfe der Anwendung wieder her, indem Sie beispielsweise eine Menüoption auswählen und deren Sicherungs Speicherort angeben.

An diesem Punkt muss der Benutzer mit dem Internet verbunden sein. eine Anforderung von der Anwendung wird an den Lizenz Verwaltungsdienst gesendet. Wenn der Computer, von dem die Lizenz gesichert wurde, nicht mit dem ursprünglichen Computer identisch ist (oder der ursprüngliche Computer neu formatiert wurde), gibt der Lizenz Verwaltungsdienst eine neue Lizenz für den neuen Computer aus. Andernfalls wird die Lizenz, die zuvor für diesen Computer ausgestellt wurde, neu ausgestellt.

Da der Lizenz Verwaltungsdienst Informationen vom Benutzer abruft, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der [Microsoft](https://www.microsoft.com/licensing/default)-Website angeben.

> [!Note]  
> Wenn ein Endbenutzer eine Lizenz auf einem anderen Computer wiederherstellt und die Lizenz eine Individualisierung erfordert, muss der Endbenutzer die zu aktualisierenden DRM-Komponenten autorisieren. Zur Unterstützung dieses Features müssen Sie in der Player Anwendung einen Prozess implementieren.

 

## <a name="detecting-fraud"></a>Erkennen von Betrug

Der Benutzer ist berechtigt, eine Lizenz auf eine begrenzte Anzahl von Zeiten wiederherzustellen. Jedes Mal, wenn eine Lizenz wieder hergestellt wird, wird Sie vom Lizenz Verwaltungsdienst nachverfolgt, und die Anzahl für diese Lizenz wird um eins erhöht. Wenn Sie eine Lizenz auf einem Computer wiederherstellen, auf dem die Lizenz zuvor wieder hergestellt wurde (z. b. auf dem Computer, von dem die Lizenz gesichert wurde), wird die Anzahl nicht angehoben. Ein Computer gilt als anders, wenn er ein neues Betriebssystem aufweist oder das Betriebssystem neu installiert wurde.

In Übereinstimmung mit der Betrugs Erkennungs Richtlinie von Microsoft, wenn eine Lizenz eine bestimmte Anzahl von Wiederholungen wieder hergestellt wurde, empfängt die Anwendung eine URL von den DRM-Komponenten und ist für das Öffnen eines Browsers und das Anzeigen der Webseite zuständig. Dies deutet darauf hin, dass die Lizenzvereinbarung möglicherweise verletzt wurde. Der Benutzer muss sich an den Lizenz Verteiler wenden, der dann ermitteln muss, ob die Anforderung gültig ist.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Sichern und Wiederherstellen von Lizenzen**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




