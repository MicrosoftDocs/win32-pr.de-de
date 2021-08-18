---
description: Der erste Schritt beim Zuordnen einer Datei besteht im Öffnen der Datei durch Aufrufen der CreateFile-Funktion.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Erstellen eines Dateizuordnungsobjekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e22fc60de9797f8b84fcc12639d39b9f07e7b0d61d905aaeccc1b7f6aa19220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067890"
---
# <a name="creating-a-file-mapping-object"></a>Erstellen eines Dateizuordnungsobjekts

Der erste Schritt beim Zuordnen einer Datei besteht im Öffnen der Datei durch Aufrufen der [**CreateFile-Funktion.**](/windows/win32/api/fileapi/nf-fileapi-createfilea) Um sicherzustellen, dass andere Prozesse nicht in den zugeordneten Teil der Datei schreiben können, sollten Sie die Datei mit exklusivem Zugriff öffnen. Darüber hinaus sollte das Dateihand handle geöffnet bleiben, bis der Prozess das Dateizuordnungsobjekt nicht mehr benötigt. Eine einfache Möglichkeit, exklusiven Zugriff zu erhalten, besteht in der Angabe von 0 (null) im *fdwShareMode-Parameter* **von CreateFile.** Das von **CreateFile zurückgegebene Handle** wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) verwendet, um ein Dateizuordnungsobjekt zu erstellen.

Die [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) gibt ein Handle an das Dateizuordnungsobjekt zurück. Dieses Handle wird beim Erstellen einer [Dateiansicht verwendet,](creating-a-file-view.md) damit Sie auf den freigegebenen Speicher zugreifen können. Wenn Sie **CreateFileMapping aufrufen,** geben Sie einen Objektnamen, die Anzahl der Bytes, die aus der Datei zugeordnet werden sollen, und die Lese-/Schreibberechtigung für den zugeordneten Speicher an. Der erste Prozess, der **CreateFileMapping aufruft,** erstellt das Dateizuordnungsobjekt. Prozesse, **die CreateFileMapping** für ein vorhandenes Objekt aufrufen, erhalten ein Handle für das vorhandene Objekt. Sie können feststellen, ob ein erfolgreicher Aufruf von **CreateFileMapping** das Dateizuordnungsobjekt erstellt oder geöffnet hat, indem Sie die [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen. **GetLastError gibt** **NO ERROR \_ an** den Erstellungsprozess und **ERROR ALREADY EXISTS \_ \_ für** nachfolgende Prozesse zurück.

Die [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) schlägt fehl, wenn die Zugriffsflags mit denen in Konflikt stehen, die beim Öffnen der Datei durch die [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) angegeben wurden. So lesen und schreiben Sie beispielsweise in die Datei:

-   Geben Sie **die GENERIC \_ READ-** **und GENERIC \_ WRITE-Werte** im *fdwAccess-Parameter* von [**CreateFile an.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)
-   Geben Sie **den PAGE \_ READWRITE-Wert** im *fdwProtect-Parameter* von [**CreateFileMapping an.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)

Beim Erstellen eines Dateizuordnungsobjekts wird kein physischer Speicher committ, sondern nur reserviert.

## <a name="file-mapping-size"></a>Dateizuordnungsgröße

Die Größe des Dateizuordnungsobjekts ist unabhängig von der Größe der zugeordneten Datei. Wenn das Dateizuordnungsobjekt jedoch größer als die Datei ist, erweitert das System die Datei, bevor [**CreateFileMapping zurückgegeben**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) wird. Wenn das Dateizuordnungsobjekt kleiner als die Datei ist, ordnet das System nur die angegebene Anzahl von Bytes aus der Datei zu.

Mit *den Parametern dwMaximumSizeHigh* und *dwMaximumSizeLow* von [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) können Sie die Anzahl der Bytes angeben, die aus der Datei zugeordnet werden sollen:

-   Wenn Die Größe der Datei nicht geändert werden soll (z. B. beim Zuordnen schreibgeschützter Dateien), rufen Sie [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) auf, und geben Sie 0 (null) für *dwMaximumSizeHigh* und *dwMaximumSizeLow* an. Dadurch wird ein Dateizuordnungsobjekt erstellt, das genau die gleiche Größe wie die Datei hat. Andernfalls müssen Sie die Größe der fertig gestellten Datei berechnen oder schätzen, da Dateizuordnungsobjekte statisch sind. Nach derEntgröße kann die Größe nicht erhöht oder verringert werden. Der Versuch, eine Datei mit einer Länge von 0 (null) auf diese Weise zu zuordnen, schlägt mit dem Fehlercode **ERROR \_ FILE INVALID \_ fehl.** Programme sollten auf Dateien mit einer Länge von 0 (null) testen und solche Dateien ablehnen.

-   Die Größe eines Dateizuordnungsobjekts, das durch eine benannte Datei erstellt wird, ist durch den Speicherplatz beschränkt. Die Größe einer Dateiansicht ist auf den größten verfügbaren zusammenhängenden Block des nicht reservierten virtuellen Arbeitsspeichers beschränkt. Dies sind mindestens 2 GB abzüglich des virtuellen Arbeitsspeichers, der bereits vom Prozess reserviert wurde.

Die Größe des ausgewählten Dateizuordnungsobjekts steuert, wie weit sie mit der Speicherzuordnung in der Datei "sehen" können. Wenn Sie ein Dateizuordnungsobjekt mit einer Größe von 500 KB erstellen, haben Sie unabhängig von der Größe der Datei nur Zugriff auf die ersten 500 KB der Datei. Da es keine Systemressourcen kostet, ein größeres Dateizuordnungsobjekt zu erstellen, erstellen Sie ein Dateizuordnungsobjekt, das die Größe der Datei hat (legen Sie die *Parameter dwMaximumSizeHigh* und *dwMaximumSizeLow* von [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) beide auf null fest), auch wenn Sie nicht erwarten, dass Sie die gesamte Datei anzeigen. Die Kosten für Systemressourcen sind für das Erstellen der Ansichten und den Zugriff darauf ankommt.

Sie können einen Teil der Datei anzeigen, der nicht am Anfang der Datei beginnt. Weitere Informationen finden Sie unter [Erstellen einer Ansicht in einer Datei.](creating-a-view-within-a-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Dateiansicht](creating-a-file-view.md)
</dt> <dt>

[Erstellen einer Ansicht innerhalb einer Datei](creating-a-view-within-a-file.md)
</dt> </dl>


 
