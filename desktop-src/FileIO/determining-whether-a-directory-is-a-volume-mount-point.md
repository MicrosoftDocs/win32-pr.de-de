---
description: Bestimmen, ob ein angegebenes Verzeichnis ein bereitgestellter Ordner ist.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867696"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist

Es ist hilfreich, zu bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist, wenn Sie z. b. eine Sicherungs-oder Suchanwendung verwenden, die auf ein Volume beschränkt ist. Eine solche Anwendung kann Informationen auf mehreren Volumes erreichen, wenn Sie Funktionen wie [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) verwenden, um bereitgestellte Ordner für die anderen Volumes auf dem Volume zu erstellen, auf das die Anwendung beschränkt ist. Weitere Informationen finden Sie unter [Erstellen eingebundenes Ordner](mounting-and-dismounting-a-volume.md).

Um zu ermitteln, ob ein angegebenes Verzeichnis ein bereitgestellter Ordner ist, müssen Sie zuerst die [**getfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) -Funktion aufrufen und das File Attribute-Flag für den Analyse **\_ \_ \_ Punkt** im Rückgabewert überprüfen, um festzustellen, ob dem Verzeichnis ein Analyse Punkt zugeordnet ist. Wenn dies der Fall ist, verwenden Sie die Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) " und " [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) ", um das Analyse-Tag im **dwReserved0** -Member der [**Win32- \_ \_ Datenstruktur suchen**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) zu erhalten. Um zu ermitteln, ob der Analyse Punkt ein bereitgestellter Ordner (und nicht eine andere Form des Analyse Punkts) ist, überprüfen Sie, ob der Tagwert dem Wert-e/a- **\_ \_ tageinstellungspunkt \_ \_** entspricht. Weitere Informationen finden Sie unter Analyse [Punkte](reparse-points.md).

Verwenden Sie die [**getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) -Funktion, um das Ziel Volume eines eingebundenen Ordners abzurufen.

Auf ähnliche Weise können Sie ermitteln, ob ein Analyse Punkt eine symbolische Verknüpfung ist, indem Sie überprüfen, ob der Tagwert e/a-Analyse **\_ Tags- \_ \_ symlink** ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Datei Attribut Konstanten**](file-attribute-constants.md)
</dt> </dl>

 

 



