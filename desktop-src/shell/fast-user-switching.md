---
description: In älteren Betriebssystemen musste sich ein Benutzer abmelden, bevor sich ein anderer Benutzer anmelden konnte. Ab Windows XP muss sich der Benutzer nicht mehr abmelden, damit sich ein anderer Benutzer anmelden kann.
ms.assetid: 72f99d32-184f-4f0b-bec1-6068c6e32f88
title: Schnelle Benutzerumschaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d79f16ef8a1ea8c97bfb61d34dfa727f3d0cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994766"
---
# <a name="fast-user-switching"></a>Schnelle Benutzerumschaltung

Wenn sich ein Benutzer bei einem Computer anmeldet, lädt das System das Profil. Da jeder Benutzer über ein eindeutiges Benutzerkonto verfügt, können mehrere Benutzer einen Computer freigeben. Wenn sich ein Benutzer anmeldet, werden die Desktop Einstellungen, Dateien, Favoriten und der Verlauf angezeigt. auf Sie kann nicht von anderen Benutzern zugegriffen werden. Wenn sich der Benutzer abmeldet, wird das zugehörige Profil beim nächsten Anmelden beibehalten. In älteren Betriebssystemen musste sich ein Benutzer abmelden, bevor sich ein anderer Benutzer anmelden konnte. Ab Windows XP muss sich der Benutzer nicht mehr abmelden, damit sich ein anderer Benutzer anmelden kann. Stattdessen ist es möglich, dass sich mehrere Benutzer schnell anmelden und zwischen den geöffneten Konten wechseln. Diese Funktion wird als *schnelle Benutzerumschaltung* bezeichnet. Wenn Sie zu einem anderen Konto wechseln, wird der Zustand der Anwendungen, die gerade von einem Benutzer ausgeführt werden, nicht geändert. Nehmen wir beispielsweise an, dass ein Benutzer einem anderen Benutzer gestattet, zu seinem Konto zu wechseln, während der erste Benutzer angemeldet ist. Wenn der erste Benutzer auf sein Konto zurückschaltet, werden seine Anwendungen ausgeführt, und Ihre Netzwerkverbindungen werden beibehalten. Daher wird angezeigt, dass beide Benutzer gleichzeitig den Computer verwenden.

Wenn Ihre Anwendungen die Windows 2000-Logo-Anforderungen erfüllen, sollten Sie mit der schnellen Benutzerumschaltung unter Windows XP und neueren Betriebssystemen arbeiten. Es ist jedoch wichtig, dieses Szenario bei der Entwicklung einer Anwendung zu berücksichtigen, damit Sie sich wie erwartet verhält. Beachten Sie beim Schreiben von Anwendungen die folgenden Richtlinien:

-   Implementieren Sie die echte Profil Trennung. Das System stellt eine zugrunde liegende Infrastruktur bereit, die die Trennung von Benutzerdaten, Benutzereinstellungen und Computereinstellungen unterstützt. Verwenden Sie z. b. den Ordner " **Dokumente** " des Benutzers, um von Benutzern erstellte Daten zu speichern. Um ein Verzeichnis für anwendungsspezifische Daten zu suchen, verwenden Sie das [bekannte Ordner](known-folders.md) System mit [**folderid \_ roamingappdata**](knownfolderid.md)) oder für ältere Betriebssysteme das [**CSIDL**](csidl.md) -System mit [**CSIDL \_ AppData**](csidl.md). Verwenden Sie " **folderid \_ LocalAppData** " oder " **local CSIDL \_ local \_ AppData** " für Daten, die für den Benutzer nicht auf anderen Computern verfügbar sein sollen, z. b. temporäre Dateien.
-   Registrieren Sie sich für eine Benachrichtigung über einen Benutzer Switch. In der Regel muss eine Anwendung nicht benachrichtigt werden, wenn der Switch auftritt. Wenn Ihre Anwendung jedoch über eine Sitzungs Änderung benachrichtigt werden muss, kann Sie sich registrieren, um eine [**WM- \_ wtssession- \_ Änderungs**](../termserv/wm-wtssession-change.md) Meldung zu erhalten.
-   Beachten Sie die anderen Instanzen Ihrer Anwendung. Beispielsweise kann es vorkommen, dass eine Anwendung ein Update aus dem Internet herunterladen muss. Das Update kann fehlschlagen, wenn ein anderer Benutzer gleichzeitig eine Instanz der Anwendung in einer anderen Sitzung ausgeführt. Auch wenn das Update erfolgreich ist, kann das Update dazu führen, dass sich andere laufende Instanzen der Anwendung auf unvorhersehbare Weise Verhalten. Daher ist es am besten, ein dynamisches Upgrade nur durchzuführen, wenn keine anderen Instanzen der Anwendung ausgeführt werden. Bevor Sie ein Anwendungs Update herunterladen, kann es sinnvoll sein, eine Methode zu implementieren, die allen ausgelaufenden Instanzen der Anwendung signalisiert, Daten zu speichern und ordnungsgemäß zu beenden.

 

 
