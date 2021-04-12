---
description: Der erste Schritt beim Mapping einer Datei besteht darin, die Datei zu öffnen, indem Sie die CreateFile-Funktion aufrufen.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Erstellen eines Datei Mapping-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65badc2af8aed5211c2f5c590fc0998019dae264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345368"
---
# <a name="creating-a-file-mapping-object"></a>Erstellen eines Datei Mapping-Objekts

Der erste Schritt beim Mapping einer Datei besteht darin, die Datei zu öffnen, indem Sie die [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) -Funktion aufrufen. Um sicherzustellen, dass andere Prozesse nicht in den Teil der Datei schreiben können, der zugeordnet ist, sollten Sie die Datei mit exklusiven Zugriffsberechtigungen öffnen. Außerdem sollte das Datei Handle geöffnet bleiben, bis der Prozess das Datei Zuordnungsobjekt nicht mehr benötigt. Eine einfache Möglichkeit, exklusiven Zugriff zu erhalten, ist die Angabe von 0 (null) im *fdwsharemode* -Parameter von " **kreatefile**". Das von " **kreatefile** " zurückgegebene Handle wird von der Funktion "Create [**FileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " verwendet, um ein Datei Zuordnung-Objekt zu erstellen.

Die Funktion " [**fiatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " gibt ein Handle für das Datei-Mapping-Objekt zurück. Dieses Handle wird verwendet, wenn [eine Dateiansicht erstellt](creating-a-file-view.md) wird, sodass Sie auf den freigegebenen Speicher zugreifen können. Wenn Sie " **kreatefilemapping**" aufrufen, geben Sie einen Objektnamen, die Anzahl der Bytes, die der Datei zugeordnet werden sollen, und die Lese-/Schreibberechtigung für den zugeordneten Speicher an. Der erste Prozess, der " **kreatefilemapping** " aufruft, erstellt das Datei Zuordnung-Objekt. Prozesse, die **CreateFileMapping** für ein vorhandenes Objekt aufrufen, erhalten ein Handle für das vorhandene Objekt. Sie können feststellen, ob ein erfolgreicher Aufruf von **CreateFileMapping** das Datei Zuordnung-Objekt erstellt oder geöffnet hat, indem Sie die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen. **GetLastError** gibt **keinen \_ Fehler** an den Erstellungsprozess zurück, und der Fehler ist für nachfolgende Prozesse **\_ bereits \_ vorhanden** .

Die Funktion "Funktion für die Funktion" schlägt fehl, wenn die Zugriffsflags [**mit den beim**](/windows/win32/api/fileapi/nf-fileapi-createfilea) Öffnen der Datei [**angegebenen Funktionen in**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) Konflikt stehen. Beispielsweise zum Lesen und Schreiben in die Datei:

-   Geben **Sie die generischen \_ Lese** -und **generischen \_ Schreib** Werte im Parameter " *bdwaccess* " von " [**kreatefile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)" an.
-   Geben Sie den Wert für die **Seiten \_ Lese** Vorgänge im Parameter " *sdwprotect* " von " [**kreatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)" an.

Beim Erstellen eines Datei Zuordnungsobjekts wird kein Commit für den physischen Speicher durchführt, sondern nur reserviert.

## <a name="file-mapping-size"></a>Größe der Datei Zuordnung

Die Größe des Datei Zuordnungsobjekts ist unabhängig von der Größe der Datei, die zugeordnet wird. Wenn das Datei Zuordnungsobjekt jedoch größer als die Datei ist, erweitert das System die Datei [](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) , bevor die Datei zuordnet. Wenn das Datei Zuordnungs Objekt kleiner als die Datei ist, ordnet das System nur die angegebene Anzahl von Bytes aus der Datei zu.

Mit den Parametern *dwmaximumsizehigh* und *dwmaximumsizelow* von " [**kreatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " können Sie die Anzahl der Bytes angeben, die aus der Datei zugeordnet werden sollen:

-   Wenn Sie nicht möchten, dass die Datei geändert wird (z. b. bei der Zuordnung Schreib geschützter Dateien), müssen Sie für " *dwmaximumsizehigh* [**" und "**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) *dwmaximumsizelow*" den Wert "0" aufrufen und NULL angeben. Dadurch wird ein Datei Mapping-Objekt erstellt, das exakt der Größe der Datei entspricht. Andernfalls müssen Sie die Größe der fertigen Datei berechnen oder schätzen, da die Größe der Datei Zuordnung von Objekten statisch ist. nach der Erstellung kann die Größe nicht mehr gesteigert oder verringert werden. Der Versuch, eine Datei mit einer Länge von NULL auf diese Weise zuzuordnen, schlägt mit dem Fehlercode **" \_ \_ ungültige Fehler Datei**" fehl. Programme sollten auf Dateien mit einer Länge von 0 (null) testen und solche Dateien ablehnen.

-   Die Größe eines Datei Mapping-Objekts, das von einer benannten Datei unterstützt wird, ist durch Speicherplatz beschränkt. Die Größe einer Dateiansicht ist auf den größten verfügbaren zusammenhängenden Block des nicht reservierten virtuellen Speichers beschränkt. Dies liegt höchstens bei 2 GB minus dem virtuellen Arbeitsspeicher, der vom Prozess bereits reserviert wurde.

Die Größe des von Ihnen ausgewählten Datei Mapping-Objekts steuert, wie weit die Datei, die Sie anzeigen können, mit der Speicher Zuordnung angezeigt wird. Wenn Sie ein Datei Zuordnungsobjekt erstellen, das 500 KB groß ist, haben Sie nur Zugriff auf die ersten 500 KB der Datei, unabhängig von der Größe der Datei. Da Sie keine Systemressourcen für die Erstellung eines größeren Datei Zuordnungs Objekts Kosten, erstellen Sie ein Datei Zuordnungs Objekt, bei dem es sich um die Größe der Datei handelt (legen Sie die Parameter *dwmaximumsizehigh* und *dwmaximumsizelow* von [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) auf NULL fest), auch wenn Sie nicht erwarten, dass Sie die gesamte Datei anzeigen. Die Kosten für Systemressourcen entstehen in der Erstellung der Sichten und des Zugriffs auf diese.

Wenn Sie einen Teil der Datei anzeigen möchten, der nicht am Anfang der Datei beginnt, müssen Sie ein Datei Zuordnungsobjekt erstellen. Bei diesem Objekt handelt es sich um die Größe des Teils der Datei, die Sie anzeigen möchten, sowie um den Offset in der Datei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Ansicht in einer Datei](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
