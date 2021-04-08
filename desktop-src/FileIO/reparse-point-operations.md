---
description: Beschreibt die Analyse Punkt Vorgänge, die Sie mithilfe von DeviceIoControl ausführen können.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Analyse Punkt Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050290"
---
# <a name="reparse-point-operations"></a>Analyse Punkt Vorgänge

Um zu ermitteln, ob ein Dateisystem Analyse Punkte unterstützt, müssen Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und die **Datei \_ unterstützt \_ \_** das Bitflag "Analyse Punkte" untersuchen.

Mit der Funktion " [**de viceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) " können Sie Analyse Punkte festlegen, ändern, abrufen und entfernen. In der folgenden Tabelle werden die Vorgänge für Analyse Punkte beschrieben, die Sie mithilfe von **DeviceIoControl** ausführen können.



| Vorgang                                                           | BESCHREIBUNG                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Analyse Punkt für die ssctl- \_ Gruppe \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | Ermöglicht dem aufrufenden Programm, einen neuen Analyse Punkt festzulegen oder eine vorhandene zu ändern.<br/> |
| [**Sicherungspunkt für "f" \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | Ruft die Informationen ab, die in einem vorhandenen Analyse Punkt gespeichert sind.<br/>                         |
| [**Lösch Analyse Punkt für den \_ Löschvorgang \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | Entfernt einen vorhandenen Analyse Punkt.<br/>                                                   |



 

Wenn Sie einen Analyse Punkt ändern, Abrufen oder löschen, müssen Sie in dem Vorgang, der in der Datei enthalten ist, dasselbe Analyse Kennzeichen angeben. Andernfalls schlägt der Vorgang mit dem Fehler Fehleranalyse **- \_ \_ tagkonflikt \_ fehl**. Wenn Sie einen Analyse Punkt ändern oder löschen, müssen Sie auch die Analyse- **GUID** in dem Vorgang angeben, der in der Datei enthalten ist. Andernfalls schlägt der Vorgang mit dem Fehler Fehleranalyse **- \_ \_ Attribut \_ Konflikt** fehl.

Verwenden Sie die [**getfileattributfunktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) , um zu bestimmen, ob eine Datei oder ein Verzeichnis einen Analyse Punkt enthält. Wenn die Datei oder das Verzeichnis über einen zugeordneten Analyse Punkt verfügt, wird das Attribut " **file \_ Attribute Analyse \_ \_ Point** " festgelegt.

Um einen vorhandenen Analyse Punkt zu überschreiben, ohne bereits über ein Handle für die Datei oder das Verzeichnis zu verfügen, müssen Sie [**die Datei mit**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) dem **Dateiflag zum Öffnen des Analyse \_ \_ \_ \_ Punkts** aufrufen. Mit diesem Flag können Sie die Datei öffnen, unabhängig davon, ob der entsprechende Dateisystem Filter installiert ist und ordnungsgemäß funktioniert.

 

