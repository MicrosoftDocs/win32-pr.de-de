---
description: Eine Win32-Assembly kann als freigegebene Assembly installiert werden und steht für die Verwendung durch mehrere Anwendungen auf dem Computer zur Verfügung. Freigegebene Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Freigegebene Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757812"
---
# <a name="shared-assemblies"></a>Freigegebene Assemblys

Eine Win32-Assembly kann als freigegebene Assembly installiert werden und steht für die Verwendung durch mehrere Anwendungen auf dem Computer zur Verfügung. Freigegebene Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.

Freigegebene Assemblys [werden als parallele](side-by-side-assemblies.md)Assemblys installiert. Der-Windows Installer installiert freigegebene parallele Assemblys im Ordner WinSxS. Die Assemblys sind nicht global auf dem System registriert, aber Sie sind global für jede Anwendung verfügbar, die eine Abhängigkeit von der Assembly in einer Manifest-Datei angibt. Weitere Informationen finden Sie unter [isolierte Anwendungen und](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)parallele Assemblys.

Auf älteren Betriebssystemen als Windows XP werden freigegebene Assemblys normalerweise im Windows-Systemordner installiert und Global registriert. Die neueste installierte Version ist für jede Anwendung verfügbar, die Sie bindet.

Informationen zum Erstellen eines Windows Installer Pakets für die Installation einer freigegebenen Assembly finden Sie in den folgenden Informationen:

-   [Installieren von Win32-Assemblys für die parallele Freigabe unter Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
