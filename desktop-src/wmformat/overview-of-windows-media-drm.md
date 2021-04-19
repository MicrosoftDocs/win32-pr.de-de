---
title: Übersicht über Windows Media DRM
description: Übersicht über Windows Media DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Digital Rights Management (DRM), Informationen zu
- DRM (Digital Rights Management), Informationen zu
- Digital Rights Management (DRM), Verpacken von Windows Media-Dateien
- DRM (Digital Rights Management), Verpacken von Windows Media-Dateien
- Digital Rights Management (DRM), geschützte Datei Lizenzierung
- DRM (Digital Rights Management), geschützte Datei Lizenzierung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), lesen geschützter Dateien
- DRM (Digital Rights Management), lesen geschützter Dateien
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- Lizenzen, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341839"
---
# <a name="overview-of-windows-media-drm"></a>Übersicht über Windows Media DRM

Bei Windows Media Digital Rights Management (DRM) handelt es sich um ein System zum Schutz der Inhalte in Windows Media-Dateien, sodass nicht autorisierte Benutzer nicht darauf zugreifen können. Der grundlegende DRM-Cycle umfasst drei Phasen: Verpacken, Lizenzierung und lesen.

## <a name="packaging-windows-media-files"></a>Verpacken von Windows Media-Dateien

Windows Media DRM ist für die Arbeit mit Windows Media-Dateien konzipiert. Eine Windows Media-Datei ist eine Datei, die der "Advanced Systems Format (ASF)"-Spezifikation entspricht und nur Audiodateien und Videos enthält, die mithilfe der Windows Media Audio-und Video Codecs komprimiert wurden.

Wenn eine ASF-Datei gepackt wird, wird ein DRM-spezifischer Abschnitt zum-Header hinzugefügt. Der DRM-Header enthält eine Schlüssel-ID, die den Inhalt für die Lizenzierung identifiziert, und eine Lizenz Erwerbs-URL. Hierbei handelt es sich um die Adresse einer Webseite, die Lizenzen zum Lesen geschützter Inhalte ausgeben kann. Es gibt noch viel mehr Informationen, die in den DRM-Header eingefügt werden können. Dies ist jedoch optional. Der DRM-Header ist signiert, sodass der Packager überprüft werden kann.

Der Inhalt in der ASF-Datei wird während des Verpackungsvorgangs verschlüsselt. Die folgenden Informationen in der Paketdatei sind jedoch auch für Clients verfügbar, die nicht über eine Lizenz verfügen:

-   Metadaten, die im ASF-Header gespeichert sind.
-   Einige Metadaten, die im DRM-Header gespeichert sind (z. b. können Sie immer die Lizenz Erwerbs-URL abrufen).

## <a name="licensing-protected-files"></a>Lizenzieren geschützter Dateien

Damit eine Paketdatei gelesen wird, muss eine Lizenz an den Client Computer ausgegeben werden. Eine Lizenz besteht aus einem Satz von Daten, die die Bedingungen beschreiben, unter denen Daten in geschützten Dateien gelesen werden können. In den meisten Fällen wird eine Lizenz für eine geschützte Datei ausgegeben, als Antwort darauf, dass der Benutzer versucht, einen Vorgang für die Datei auszuführen. Es ist jedoch auch möglich, dass ein Lizenz Aussteller Lizenzen an einen Client übermitteln muss, bevor er explizit angefordert wird. Weitere Informationen zu Lizenzen finden Sie unter [Lizenzen](licenses.md).

## <a name="reading-data-from-protected-files"></a>Lesen von Daten aus geschützten Dateien

Wenn ein Benutzer versucht, einen Vorgang für eine geschützte Datei auszuführen (Wiedergabe, Brennen auf CD, kopieren auf ein Gerät usw.), muss die Anwendung auf dem Client Computer nach Lizenzen suchen. Wenn auf dem Client Computer eine gültige Lizenz vorhanden ist, kann der Vorgang fortgesetzt werden. Wenn keine Lizenz für den Inhalt vorhanden ist oder wenn keine Lizenz für den Inhalt, der auf dem Client Computer vorhanden ist, die angeforderte Aktion zulässt, muss eine Lizenz erworben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu den erweiterten APIs für den Windows Media DRM-Client**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




