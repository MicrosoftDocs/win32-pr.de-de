---
description: Eine Win32-Assembly kann als freigegebene Assembly installiert werden und kann von mehreren Anwendungen auf dem Computer verwendet werden. Freigegebene Assemblys sollten von einem installationsinstallierten Windows installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Freigegebene Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1097a0f2bbbc4d91a6206734cb2dead53bb38748b82c0204daff476d3eb663e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628510"
---
# <a name="shared-assemblies"></a>Freigegebene Assemblys

Eine Win32-Assembly kann als freigegebene Assembly installiert werden und kann von mehreren Anwendungen auf dem Computer verwendet werden. Freigegebene Assemblys sollten von einem installationsinstallierten Windows installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.

Freigegebene Assemblys werden als [nebeneinander seitige Assemblys installiert.](side-by-side-assemblies.md) Der Windows Installer installiert freigegebene, nebeneinander gespeicherte Assemblys im Ordner Winsxs. Die Assemblys werden nicht global auf dem System registriert, sind aber global für jede Anwendung verfügbar, die eine Abhängigkeit von der Assembly in einer Manifestdatei angibt. Weitere Informationen finden Sie unter [Isolierte Anwendungen und nebenseitige Assemblys.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

Unter Betriebssystemen vor Windows XP werden freigegebene Assemblys in der Regel im Windows Systemordner installiert und global registriert. Die neueste installierte Version ist für jede Anwendung verfügbar, die daran gebunden ist.

Informationen zum Erstellen eines Pakets Windows Installer zum Installieren einer freigegebenen Assembly finden Sie in den folgenden Themen:

-   [Installieren von Win32-Assemblys für die side-by-side-Freigabe auf Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installieren von Win32-Assemblys für die private Verwendung einer Anwendung auf Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
