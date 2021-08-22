---
description: Msizap.exe ist ein Befehlszeilenprogramm, das entweder alle Windows Installer-Informationen für ein Produkt oder alle auf einem Computer installierten Produkte entfernt. Produkte, die vom Installationsprogramm installiert werden, funktionieren nach der Verwendung von Msizap möglicherweise nicht mehr.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f29de42f41a72f06f62627489f8f44d1b21c5c76066ba1b1a990334f53c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943671"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe ist ein Befehlszeilenprogramm, das entweder alle Windows Installer-Informationen für ein Produkt oder alle auf einem Computer installierten Produkte entfernt. Produkte, die vom Installationsprogramm installiert werden, funktionieren nach der Verwendung von Msizap möglicherweise nicht mehr.

Auf Windows 2000 und Windows XP sind Administratorrechte erforderlich, um Msizap.exe.

Dieses Tool ist nur in Windows [SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md) verfügbar und sollte nicht neu verteilt werden. Verwenden Sie die aktuelle Version von Msizap.exe (Version 3.1.4000.2726 oder höher), die in den Windows SDK-Komponenten für Windows Installer Developers für Windows Vista oder höher verfügbar ist. Kleinere Versionen von Msizap.exe können Informationen zu allen Updates entfernen, die auf andere Anwendungen auf dem Computer des Benutzers angewendet wurden. Wenn diese Informationen entfernt werden, müssen diese anderen Anwendungen möglicherweise entfernt und neu installiert werden, um zusätzliche Updates zu erhalten.

## <a name="syntax"></a>Syntax

**msizap T**_\[ WA! \] {Produktcode}_

**msizap T**_\[ WA! \] <msi package>_

**msizap \* *** \[ WA! \]* **ALLPRODUCTS**

**msizap PWSA?!**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msizap.exe verwendet Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird, wie in der folgenden Tabelle gezeigt.



| Option | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | Entfernt alle Windows Installer-Ordner und Registrierungsschlüssel, passt die Anzahl der freigegebenen DLLs an und beendet Windows Installer-Dienst. Entfernt außerdem die In-Progress und Rollbackinformationen.                                                                           |
| a      | Ändert die ACLs nur für alle angegebenen Entfernungen in Admin Full Control.                                                                                                                                                                                            |
| g      | Entfernt für alle Benutzer alle zwischengespeicherten Windows Installer-Datendateien, die verwaist sind.                                                                                                                                                                       |
| p      | Entfernt den In-Progress Schlüssel.                                                                                                                                                                                                                                  |
| s      | Entfernt Rollbackinformationen.                                                                                                                                                                                                                                 |
| t      | Entfernt alle Informationen für den angegebenen Produktcode. Wenn Sie diese Option verwenden, schließen Sie den Produktcode in geschweifte Klammern ein. Diese Option kann entweder mit dem vollständigen Pfad zur .msi oder mit dem Produktcode verwendet werden.                                        |
| w      | Entfernt Windows Installer-Informationen für alle Benutzer. Wenn diese Option nicht festgelegt ist, werden nur die Informationen für den aktuellen Benutzer entfernt. Die Verwendung dieser Option erfordert, dass das Profil des Benutzers geladen wird, damit die Registrierungsstruktur des Benutzers pro Benutzer verfügbar ist. |
| ?      | Ausführliche Hilfe.                                                                                                                                                                                                                                                 |
| !      | Erzwingt eine "Ja"-Antwort auf eine beliebige Eingabeaufforderung.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



