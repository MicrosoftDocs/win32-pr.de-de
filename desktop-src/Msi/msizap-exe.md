---
description: Msizap.exe ist ein Befehlszeilenprogramm, das entweder alle Windows Installer Informationen für ein Produkt oder alle auf einem Computer installierten Produkte entfernt. Produkte, die vom Installationsprogramm installiert werden, funktionieren möglicherweise nicht mehr, nachdem msizap verwendet wurde.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042072"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe ist ein Befehlszeilenprogramm, das entweder alle Windows Installer Informationen für ein Produkt oder alle auf einem Computer installierten Produkte entfernt. Produkte, die vom Installationsprogramm installiert werden, funktionieren möglicherweise nicht mehr, nachdem msizap verwendet wurde.

Unter Windows 2000 und Windows XP sind Administratorrechte erforderlich, um Msizap.exe zu verwenden.

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) verfügbar und sollte nicht weiter verteilt werden. Verwenden Sie die aktuelle Version von Msizap.exe (Version 3.1.4000.2726 oder höher), die in den Windows SDK Komponenten für Windows Installer Entwickler für Windows Vista oder höher verfügbar ist. Kleinere Versionen von Msizap.exe können Informationen zu allen Updates entfernen, die auf andere Anwendungen auf dem Computer des Benutzers angewendet wurden. Wenn diese Informationen entfernt werden, müssen diese anderen Anwendungen möglicherweise entfernt und erneut installiert werden, um weitere Updates zu erhalten.

## <a name="syntax"></a>Syntax

**msizap T**_\[ WA! \] {Product Code}_

**msizap T**_\[ WA! \] <msi package>_

**msizap \* *** \[ WA! \]* **Allproducts**

**msizap pwsa?**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msizap.exe verwendet die in der folgenden Tabelle aufgeführten Befehlszeilenoptionen ohne Beachtung der Groß-/Kleinschreibung.



| Option | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | Entfernt alle Windows Installer Ordner und Registrierungsschlüssel, passt die Anzahl der freigegebenen DLL an und beendet Windows Installer Dienst. Entfernt auch die In-Progress Key-und Rollback-Informationen.                                                                           |
| a      | Ändert die Zugriffs Steuerungs Liste für alle angegebenen Entfernungs Vorgänge nur in den Administrator.                                                                                                                                                                                            |
| g      | Entfernt alle zwischengespeicherten Windows Installer Datendateien, die verwaist sind, für alle Benutzer.                                                                                                                                                                       |
| p      | Entfernt den In-Progress Schlüssel.                                                                                                                                                                                                                                  |
| s      | Entfernt Rollback-Informationen.                                                                                                                                                                                                                                 |
| t      | Entfernt alle Informationen für den angegebenen Produktcode. Wenn Sie diese Option verwenden, schließen Sie den Produkt Code in geschweiften Klammern ein. Diese Option kann entweder mit dem vollständigen Pfad der MSI-Datei oder mit dem Produktcode verwendet werden.                                        |
| w      | Entfernt Windows Installer Informationen für alle Benutzer. Wenn diese Option nicht festgelegt ist, werden nur die Informationen für den aktuellen Benutzer entfernt. Wenn Sie diese Option verwenden, muss das Profil des Benutzers geladen werden, damit die benutzerspezifische Registrierungs Struktur des Benutzers verfügbar ist. |
| ?      | Ausführliche Hilfe.                                                                                                                                                                                                                                                 |
| !      | Erzwingt eine "yes"-Antwort auf eine beliebige Eingabeaufforderung.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



