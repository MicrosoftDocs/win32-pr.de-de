---
description: Der erste Schritt beim Zuordnen einer Datei besteht darin, die Datei durch Aufrufen der CreateFile-Funktion zu öffnen.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Erstellen eines Dateizuordnungsobjekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502c484dd0466b47a87f4db205d1da5499bf5ef
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432502"
---
# <a name="creating-a-file-mapping-object"></a>Erstellen eines Dateizuordnungsobjekts

Der erste Schritt beim Zuordnen einer Datei besteht darin, die Datei durch Aufrufen der [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) zu öffnen. Um sicherzustellen, dass andere Prozesse nicht in den Teil der zugeordneten Datei schreiben können, sollten Sie die Datei mit exklusivem Zugriff öffnen. Darüber hinaus sollte das Dateihandle geöffnet bleiben, bis der Prozess das Dateizuordnungsobjekt nicht mehr benötigt. Eine einfache Möglichkeit, exklusiven Zugriff zu erhalten, besteht darin, 0 (null) im *fdwShareMode-Parameter* von **CreateFile** anzugeben. Das von **CreateFile** zurückgegebene Handle wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) verwendet, um ein Dateizuordnungsobjekt zu erstellen.

Die [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) gibt ein Handle für das Dateizuordnungsobjekt zurück. Dieses Handle wird beim [Erstellen einer Dateiansicht](creating-a-file-view.md) verwendet, damit Sie auf den freigegebenen Arbeitsspeicher zugreifen können. Wenn Sie **CreateFileMapping** aufrufen, geben Sie einen Objektnamen, die Anzahl der aus der Datei zuzuordnenden Bytes und die Lese-/Schreibberechtigung für den zugeordneten Speicher an. Der erste Prozess, der **CreateFileMapping** aufruft, erstellt das Dateizuordnungsobjekt. Prozesse, die **CreateFileMapping** für ein vorhandenes Objekt aufrufen, empfangen ein Handle für das vorhandene Objekt. Sie können feststellen, ob ein erfolgreicher Aufruf von **CreateFileMapping** das Dateizuordnungsobjekt erstellt oder geöffnet hat, indem Sie die [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen. **GetLastError** gibt **NO \_ ERROR** an den Erstellungsprozess und **ERROR ALREADY \_ \_ EXISTS** an nachfolgende Prozesse zurück.

Die [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) schlägt fehl, wenn die Zugriffsflags mit denen in Konflikt geraten, die beim Öffnen der Datei durch die [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) angegeben wurden. Um z. B. die Datei zu lesen und in sie zu schreiben:

-   Geben Sie die Werte **GENERIC \_ READ** und **GENERIC \_ WRITE** im *fdwAccess-Parameter* von [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)an.
-   Geben Sie den **PAGE \_ READWRITE-Wert** im *fdwProtect-Parameter* von [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)an.

Beim Erstellen eines Dateizuordnungsobjekts wird kein physischer Arbeitsspeicher committen, sondern nur reserviert.

## <a name="file-mapping-size"></a>Dateizuordnungsgröße

Die Größe des Dateizuordnungsobjekts ist unabhängig von der Größe der zuzuordnenden Datei. Wenn das Dateizuordnungsobjekt jedoch größer als die Datei ist, erweitert das System die Datei, bevor [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) zurückgegeben wird. Wenn das Dateizuordnungsobjekt kleiner als die Datei ist, ordnet das System nur die angegebene Anzahl von Bytes aus der Datei zu.

Mit *den Parametern dwMaximumSizeHigh* und *dwMaximumSizeLow* von [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) können Sie die Anzahl der Bytes angeben, die aus der Datei zugeordnet werden sollen:

-   Wenn Sie nicht möchten, dass sich die Größe der Datei ändert (z. B. beim Zuordnen schreibgeschützter Dateien), rufen [**Sie CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) auf, und geben Sie 0 (null) für *dwMaximumSizeHigh* und *dwMaximumSizeLow* an. Dadurch wird ein Dateizuordnungsobjekt erstellt, das genau die gleiche Größe wie die Datei hat. Andernfalls müssen Sie die Größe der fertig gestellten Datei berechnen oder schätzen, da Dateizuordnungsobjekte statisch sind. Nach der Erstellung kann die Größe nicht mehr erhöht oder verringert werden. Der Versuch, eine Datei mit der Länge 0 (null) auf diese Weise zuzuordnen, schlägt mit dem Fehlercode **ERROR \_ FILE INVALID \_ fehl.** Programme sollten auf Dateien mit einer Länge von 0 (null) testen und solche Dateien ablehnen.

-   Die Größe eines Dateizuordnungsobjekts, das durch eine benannte Datei gesichert wird, ist durch den Speicherplatz beschränkt. Die Größe einer Dateiansicht ist auf den größten verfügbaren zusammenhängenden Block nicht bereitgestellten virtuellen Arbeitsspeichers beschränkt. Dies beträgt höchstens 2 GB abzüglich des virtuellen Arbeitsspeichers, der bereits vom Prozess reserviert wurde.

Die Größe des ausgewählten Dateizuordnungsobjekts steuert, wie weit die Datei mit der Speicherzuordnung "angezeigt" werden kann. Wenn Sie ein Dateizuordnungsobjekt mit einer Größe von 500 KB erstellen, haben Sie unabhängig von der Größe der Datei nur Zugriff auf die ersten 500 KB der Datei. Da die Erstellung eines größeren Dateizuordnungsobjekts keine Systemressourcen kostet, erstellen Sie ein Dateizuordnungsobjekt, das der Größe der Datei entspricht (legen Sie die Parameter *dwMaximumSizeHigh* und *dwMaximumSizeLow* von [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) auf 0 fest), auch wenn Sie nicht erwarten, die gesamte Datei anzuzeigen. Die Kosten für Systemressourcen entstehen durch das Erstellen der Ansichten und den Zugriff darauf.

Sie können einen Teil der Datei anzeigen, der nicht am Anfang der Datei beginnt. Weitere Informationen finden Sie unter [Erstellen einer Ansicht in einer Datei.](creating-a-view-within-a-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>
[Erstellen einer Dateiansicht](creating-a-file-view.md)
</dt> <dt> 
[Erstellen einer Ansicht in einer Datei](creating-a-view-within-a-file.md)
</dt> </dl>


 
