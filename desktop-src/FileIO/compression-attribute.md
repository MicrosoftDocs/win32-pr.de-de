---
description: Auf einem NTFS-Dateisystemvolume verfügt jede Datei und jedes Verzeichnis über ein Komprimierungsattribut.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Komprimierungsattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99fb42aaa30fc3e5d2ef36da85bae194950c587d024510b18233f3c83504ab88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982150"
---
# <a name="compression-attribute"></a>Komprimierungsattribut

Auf einem NTFS-Dateisystemvolume verfügt jede Datei und jedes Verzeichnis über das *Komprimierungsattribut*. Andere Dateisysteme können auch ein Komprimierungsattribut für einzelne Dateien und Verzeichnisse implementieren.

Sie können ermitteln, ob ein Dateisystem ein Komprimierungsattribut für Dateien und Verzeichnisse unterstützt, indem Sie die [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) aufrufen und das **FILE FILE \_ COMPRESSION-Bitflag \_** untersuchen.

Verwenden Sie die [**Funktion GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) oder [**GetFileAttributesEx,**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) um das Komprimierungsattribut einer Datei oder eines Verzeichnisses zu bestimmen.

Wenn das Komprimierungsattribut einer Datei festgelegt ist **(FILE \_ ATTRIBUTE \_ COMPRESSED**), werden alle Daten in der Datei komprimiert. Wenn das Attribut eindeutig ist, wird keine der Daten in der Datei komprimiert. Aus Der Programmierperspektive des Benutzermodus gibt es keinen teilweise komprimierten Zustand. Das Komprimierungsattribut ist ein einfacher boolescher Indikator für den Komprimierungszustand.

Das Komprimierungsattribut eines Verzeichnisses stellt ein Standardkomprimierungsattribut für neu erstellte Dateien und Unterverzeichnisse bereit. Wenn Sie [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) oder [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) aufrufen, um eine neue Datei oder ein neues Verzeichnis zu erstellen, erbt die neue Datei oder das neue Verzeichnis das Komprimierungsattribut des übergeordneten Verzeichnisses.

Um das **ATTRIBUT FILE ATTRIBUTE \_ \_ COMPRESSED** für eine Datei oder ein Verzeichnis zu ändern, müssen Sie die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit dem [**FSCTL SET \_ \_ COMPRESSION-Steuerungscode**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dateiattributkonstanten**](file-attribute-constants.md)
</dt> </dl>

 

 
