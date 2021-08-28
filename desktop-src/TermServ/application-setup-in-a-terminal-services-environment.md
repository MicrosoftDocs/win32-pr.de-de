---
title: Anwendungseinrichtung
description: Das Installieren einer Anwendung für einen einzelnen Benutzer kann probleme in einer Umgebung mit mehreren Benutzern Remotedesktopdienste verursachen.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743eff150edf5e9d213759ccef8c786bab98754b8e4dc2b968929ba3ad2d6709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099590"
---
# <a name="application-setup"></a>Anwendungseinrichtung

Bei der automatisierten Einrichtung vieler vorhandener Anwendungen wird davon ausgegangen, dass die Anwendung für einen einzelnen Benutzer installiert wird. In einer Umgebung mit mehreren Remotedesktopdienste kann diese Annahme folgende Probleme verursachen:

-   Wenn das Setupverfahren die Registrierungs- und Desktopumgebung für nur einen Benutzer aktualisiert, müssen zusätzliche Benutzer das gesamte Paket neu installieren, oder ein Administrator muss manuell Informationen aus der Registrierung und dem Desktop eines Benutzers auf die anderen Benutzer kopieren.
-   Mit einigen Setupverfahren können Sie die Anwendung zur Installationszeit anpassen, indem Sie Features ausschließen. Wenn das anfängliche Installationsprogramm einen Teil der Anwendung ausschließt, müssen zusätzliche Benutzer die Anwendung neu installieren, um die ausgeschlossenen Features zu erhalten.

Um diese Probleme zu vermeiden, sollten setup-Verfahren beim Installieren einer Anwendung auf einem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) die folgenden Richtlinien befolgen:

-   Installieren Sie Anwendungen in der Standardbenutzerumgebung, die allen Benutzern gemeinsam ist. Führen Sie vor der Installation der Anwendung den Befehl **change user /install** console aus, und führen Sie nach Abschluss der Installation den Befehl **change user /execute** console aus. Verwenden Sie ein Remotedesktopdienste-Kompatibilitätsskript für die Installation.
-   Unterstützen sie die benutzerspezifische Anpassung durch die Verwendung von Benutzerprofilen. Erstellen Sie hierzu ein [Administratives Vorlagendateiformat,](/previous-versions/windows/desktop/Policy/administrative-template-file-format) damit ein Administrator die Registrierung so konfigurieren kann, dass die für jeden Benutzer verfügbaren Features angegeben werden. Anschließend kann die Anwendung zur Laufzeit Features abhängig von den Einstellungen in den Registrierungseinstellungen des aktuellen Benutzers aktivieren oder deaktivieren. Die Anwendung kann die Konfiguration pro Benutzer in der **Registrierungsstruktur HKEY CURRENT USER** speichern und jedem Benutzer erlauben, die Anwendung gemäß ihren Einstellungen zu konfigurieren.

 

 