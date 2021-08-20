---
title: Übersicht über Windows Medien-DRM
description: Übersicht über Windows Medien-DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Medienformat-SDK, Digital Rights Management (DRM)
- Windows Medienformat-SDK, DRM-Lizenzen
- Windows Medienformat-SDK,Lizenzen für DRM
- Digital Rights Management (DRM), Informationen
- DRM (Digital Rights Management), Informationen
- Digital Rights Management (DRM), Verpacken Windows Mediendateien
- DRM (Verwaltung digitaler Rechte),Verpacken Windows Mediendateien
- Digital Rights Management (DRM), Lizenzierung geschützter Dateien
- DRM (Verwaltung digitaler Rechte), Lizenzierung geschützter Dateien
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Lesen geschützter Dateien
- DRM (Digital Rights Management),Lesen geschützter Dateien
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- lizenzen,DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6cc882d31873a05361869b9246da1b57ac3d3aebb85073d0b31f24509a615b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846415"
---
# <a name="overview-of-windows-media-drm"></a>Übersicht über Windows Medien-DRM

Windows Media Digital Rights Management (DRM) ist ein System zum Schützen der Inhalte in Windows Mediendateien, sodass nicht autorisierte Benutzer nicht darauf zugreifen können. Der grundlegende DRM-Zyklus umfasst drei Phasen: Verpacken, Lizenzierung und Lesen.

## <a name="packaging-windows-media-files"></a>Verpacken Windows Mediendateien

Windows Medien-DRM ist für die Arbeit mit Windows Mediendateien konzipiert. Eine Windows Media-Datei ist eine Datei, die der ASF-Spezifikation (Advanced Systems Format) entspricht und nur Audio und Video enthält, die mithilfe der Windows Medienaudio- und Videocodecs komprimiert wurden.

Wenn eine ASF-Datei gepackt wird, wird dem Header ein DRM-spezifischer Abschnitt hinzugefügt. Der DRM-Header enthält eine Schlüssel-ID, die den Inhalt für die Lizenzierung identifiziert, und eine Lizenzerwerbs-URL, die die Adresse einer Webseite darstellt, die Lizenzen zum Lesen der geschützten Inhalte ausstellen kann. Es gibt viele weitere Informationen, die im DRM-Header abgelegt werden können, aber es ist optional. Der DRM-Header wird signiert, damit der Packager überprüft werden kann.

Der Inhalt in der ASF-Datei wird während des Komprimierungsprozesses verschlüsselt. Die folgenden Informationen in der gepackten Datei sind jedoch auch für Clients verfügbar, die nicht über eine Lizenz verfügen:

-   Metadaten, die im ASF-Header gespeichert sind.
-   Einige Metadaten, die im DRM-Header gespeichert sind (z. B. können Sie immer die Lizenzerwerbs-URL abrufen).

## <a name="licensing-protected-files"></a>Lizenzierung geschützter Dateien

Damit eine gepackte Datei gelesen werden kann, muss eine Lizenz für den Clientcomputer ausgestellt werden. Eine Lizenz ist ein Satz von Daten, der die Bedingungen beschreibt, unter denen Daten in geschützten Dateien gelesen werden können. In den meisten Fällen wird eine Lizenz für eine geschützte Datei als Reaktion auf den Benutzer ausgestellt, der versucht, einen Vorgang für die Datei auszuführen. Es ist jedoch auch möglich, dass ein Lizenzaussteller Lizenzen an einen Client übermittelt, bevor er explizit angefordert wird. Weitere Informationen zu Lizenzen finden Sie unter [Lizenzen.](licenses.md)

## <a name="reading-data-from-protected-files"></a>Lesen von Daten aus geschützten Dateien

Wenn ein Benutzer versucht, einen Vorgang für eine geschützte Datei auszuführen (wiedergeben, auf CD speichern, auf ein Gerät kopieren usw.), muss die Anwendung auf dem Clientcomputer nach Lizenzen für den Inhalt suchen. Wenn auf dem Clientcomputer eine gültige Lizenz vorhanden ist, kann der Vorgang fortgesetzt werden. Wenn keine Lizenz für den Inhalt vorhanden ist oder keine Lizenz für den Inhalt auf dem Clientcomputer die angeforderte Aktion zulässt, muss eine Lizenz erworben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu den erweiterten APIs des Windows Media DRM-Clients**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




