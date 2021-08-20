---
description: Bestimmen, ob ein angegebenes Verzeichnis ein bereitgestellter Ordner ist.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c0af53a63f64164604a5f8f22532add3dded1a46d19d96354c0da37e12d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150593"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist

Es ist hilfreich zu bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist, wenn Sie beispielsweise eine Sicherungs- oder Suchanwendung verwenden, die auf ein Volume beschränkt ist. Eine solche Anwendung kann Informationen auf mehreren Volumes erreichen, wenn Sie Funktionen wie [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) verwenden, um bereitgestellte Ordner für die anderen Volumes auf dem Volume zu erstellen, auf das die Anwendung beschränkt ist. Weitere Informationen finden Sie unter [Erstellen von bereitgestellten Ordnern.](mounting-and-dismounting-a-volume.md)

Um zu ermitteln, ob ein angegebenes Verzeichnis ein bereitgestellter Ordner ist, rufen Sie zunächst die [**GetFileAttributes-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) auf, und überprüfen Sie das FILE ATTRIBUTE REPARSE POINT-Flag im Rückgabewert, um festzustellen, ob das Verzeichnis über einen zugeordneten **\_ \_ Reparsepunkt \_** verfügt. Wenn dies der Grund ist, verwenden Sie die [**Funktionen FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) und [**FindNextFile,**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) um das Reparsetag im **dwReserved0-Member** der [**WIN32 \_ FIND \_ DATA-Struktur**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) zu erhalten. Um zu ermitteln, ob es sich bei dem Aufbereitungspunkt um einen bereitgestellten Ordner (und nicht um eine andere Form des Aufbereitungspunkts) handelt, testen Sie, ob der Tagwert dem Wert **IO \_ REPARSE \_ TAG MOUNT POINT \_ \_ entspricht.** Weitere Informationen finden Sie unter [Reparse Points](reparse-points.md).

Verwenden Sie die [**GetVolumeNameForVolumeMountPoint-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) um das Zielvolume eines bereitgestellten Ordners zu erhalten.

Auf ähnliche Weise können Sie feststellen, ob ein Reparsepunkt eine symbolische Verknüpfung ist, indem Sie testen, ob der Tagwert **IO \_ REPARSE \_ TAG \_ SYMLINK ist.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dateiattributkonst constants**](file-attribute-constants.md)
</dt> </dl>

 

 



