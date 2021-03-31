---
description: Das bekannte Ordnersystem bietet eine Möglichkeit, mit bestimmten hoch Profil Ordnern zu interagieren, die in Windows standardmäßig vorhanden sind.
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: Arbeiten mit bekannten Ordnern in Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484006"
---
# <a name="working-with-known-folders-in-applications"></a>Arbeiten mit bekannten Ordnern in Anwendungen

Das bekannte Ordnersystem bietet eine Möglichkeit, mit bestimmten hoch Profil Ordnern zu interagieren, die in Windows standardmäßig vorhanden sind. Sie ermöglicht auch die gleichen Interaktionen mit Ordnern, die von Anwendungen installiert und in dem bekannten Ordnersystem registriert sind. In diesem Thema werden die möglichen Interaktionen erläutert, die von den bekannten Ordner-APIs bereitgestellt werden.

-   [Bekannte Ordner Schnittstellen](#known-folder-interfaces)
-   [Umleitung](#redirection)
-   [Zugehörige Themen](#related-topics)

> [!IMPORTANT]
> Verwenden Sie zum Umleiten der Dokumente, Bilder oder Desktop Ordner in onedrive anstelle der in diesem Artikel beschriebenen Umleitungs Methode die Verwendung von onedrive known Folder Move. Weitere Informationen finden [Sie unter Umleiten und Verschieben von bekannten Windows-Ordnern auf onedrive](/onedrive/redirect-known-folders).  

## <a name="known-folder-interfaces"></a>Bekannte Ordner Schnittstellen

Es gibt zwei bekannte Ordner Schnittstellen: [**iknownfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) und [**iknownfoldermanager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager).

[**Iknownfoldermanager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) bietet viele allgemeinere Funktionen in Bezug auf diese Ordner. Mit den dazugehörigen Methoden können Sie folgende Aktionen ausführen:

-   Abrufen eines [**iknownfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) basierend auf der [**KNOWNFOLDERID**](knownfolderid.md)des Ordners, dem kanonischen Namen, dem Pfad als Zeichenfolge oder dem Pfad, der als idlist ausgedrückt wird.
-   Konvertieren Sie eine CSIDL in Ihre [**KNOWNFOLDERID**](knownfolderid.md) -Entsprechung, oder konvertieren Sie eine **KNOWNFOLDERID** in Ihre Legacy-CSIDL-Entsprechung.
-   Registrieren Sie einen bekannten Ordner beim System, oder heben Sie die Registrierung auf.
-   Ruft alle auf diesem System registrierten [**KNOWNFOLDERID**](knownfolderid.md) -Werte ab.
-   Umleiten eines bekannten Ordners an einen neuen Speicherort.

[**Iknownfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) stellt eine Methode bereit, die es einem Ordner ermöglicht, sich selbst umzuleiten, indem ein neuer Pfad bereitgestellt wird. Die anderen Methoden erhalten Informationen zu einem bestimmten bekannten Ordner, einschließlich:

-   Die Kategorie des Ordners: "Virtual", "Fixed", "Common" oder "pro Benutzer".
-   Der Typ des Ordners, z. b. komprimierte Dateien, Dokumente, Bilder oder Benutzer Dateien.
-   Die [**KNOWNFOLDERID**](knownfolderid.md) des Ordners.
-   Der vollständige Pfad des Ordners als idlist oder als Zeichenfolge. Auch der relative Pfad zu einem übergeordneten Ordner.
-   Der kanonische Name des Ordners.
-   Die für den Ordner angezeigte QuickInfo.
-   Das Symbol, das für den Ordner angezeigt wird.
-   Eine Beschreibung des Ordners, in dem der Zweck und die Verwendung erläutert werden.
-   Gibt an, ob der Ordner umgeleitet werden kann.

[**Iknownfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) bietet auch eine Methode zum Abrufen eines [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , das auf dem Ordner basiert. Auf diese Weise können Sie den Ordner an einen Handler binden, zwei Ordner vergleichen und die Ordner Attribute, den anzeigen Amen und den übergeordneten Ordner abrufen.

## <a name="redirection"></a>Umleitung

Die Ordner Umleitung ist ein wichtiges Feature des bekannten Ordner Systems. Alle bekannten Ordner der Kategorie " [ **Common** KF \_ Category \_ Common * * * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) " oder " [ **pro Benutzer**", "KF \_ Category \_ peruser * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * *", sind redirectable. Der Ordner der Kategorie " [ **Virtual** KF \_ Category \_ Virtual * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * *" oder " [ **fixedr** KF \_ Category \_ Fixed * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)* *" kann jedoch nicht umgeleitet werden.

Ordner können entweder an einen anderen Speicherort auf demselben Computer oder an einen Speicherort in einem Netzwerk umgeleitet werden. Bei einer Netzwerk Umleitung kann der Ordner lokal durch Client seitiges zwischenspeichern zwischengespeichert werden, um Offline Zugriff zu ermöglichen. Auch wenn ein lokaler Cache vorhanden ist, muss auf den umgeleiteten Ordner selbst über das Netzwerk zugegriffen werden.

Die Ordner Umleitung ist für Windows Vista nicht neu. Beispielsweise könnten in Windows XP einige Ordner, die über das CSIDL-System identifiziert werden, durch einen [**shsetfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) -Befehl umgeleitet oder durch Ändern des CSIDL-Eintrags in der Registrierung geändert werden. In Windows Vista und höher sollte die Umleitung über [**iknownfolder:: setpath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) oder [**shsetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)durchgeführt werden.

Um zu ermitteln, ob ein Ordner umgeleitet werden kann, nennen Sie [**iknownfolder:: getredirection-Funktionen**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities). Wenn der Ordner nicht umgeleitet werden kann, kann dieser Befehl eine Erläuterung erhalten.

Wenn ein Ordner an einen Netzwerk Speicherort umgeleitet wird, können die [**iknownfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) -Methoden weiterhin erfolgreich aufgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
