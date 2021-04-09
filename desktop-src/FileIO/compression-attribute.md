---
description: Auf einem NTFS-Dateisystem Volume weist jede Datei und jedes Verzeichnis ein Komprimierungs Attribut auf.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Komprimierungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869092"
---
# <a name="compression-attribute"></a>Komprimierungs Attribut

Auf einem NTFS-Dateisystem Volume weist jede Datei und jedes Verzeichnis ein *Komprimierungs Attribut* auf. Andere Dateisysteme können auch ein Komprimierungs Attribut für einzelne Dateien und Verzeichnisse implementieren.

Sie können bestimmen, ob ein Dateisystem ein Komprimierungs Attribut für Dateien und Verzeichnisse unterstützt, indem Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und das Bitflag für die **\_ \_ Komprimierung der Datei Datei** untersuchen.

Verwenden Sie die Funktion [**getfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) oder [**getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) , um das Komprimierungs Attribut einer Datei oder eines Verzeichnisses zu bestimmen.

Wenn das Komprimierungs Attribut einer Datei festgelegt ist (**file- \_ Attribut \_ komprimiert**), werden alle Daten in der Datei komprimiert. Wenn das Attribut eindeutig ist, wird keine der Daten in der Datei komprimiert. Es gibt keinen teilweise komprimierten Zustand aus einer Programmier Perspektive im Benutzermodus. Das Komprimierungs Attribut ist ein einfacher boolescher Indikator für den Komprimierungs Status.

Das Komprimierungs Attribut eines Verzeichnisses stellt ein Standard Komprimierungs Attribut für neu erstellte Dateien und Unterverzeichnisse bereit. Wenn Sie zum Erstellen einer neuen Datei oder eines neuen Verzeichnisses " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " oder " [**kreatedirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) " aufrufen, erbt die neue Datei bzw. das zugehörige Verzeichnis das Komprimierungs Attribut des übergeordneten Verzeichnisses.

Um das **\_ \_ komprimierte Attribut file Attribute** für eine Datei oder ein Verzeichnis zu ändern, müssen Sie die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion mit dem Code für die [**\_ \_ Komprimierung des FSCTL-Satzes**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Datei Attribut Konstanten**](file-attribute-constants.md)
</dt> </dl>

 

 
