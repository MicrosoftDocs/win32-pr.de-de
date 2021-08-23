---
description: Shell-Zwischenablageformate werden verwendet, um den Typ der Shelldaten zu identifizieren, die über die Zwischenablage übertragen werden.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Shell-Zwischenablageformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fccd73f5b364c247454d874f5b9bb7586e3187150ebce28620cc6dc01f8298d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351390"
---
# <a name="shell-clipboard-formats"></a>Shell-Zwischenablageformate

Shell-Zwischenablageformate werden verwendet, um den Typ der Shelldaten zu identifizieren, die über die Zwischenablage übertragen werden. Die meisten Shell-Zwischenablageformate identifizieren einen Datentyp, z. B. eine Liste von Dateinamen oder Zeiger auf Elementbezeichnerlisten (PIDLs). Einige Formate werden jedoch für die Kommunikation zwischen Quelle und Ziel verwendet. Sie können den Datenübertragungsprozess beschleunigen, indem [](datascenarios.md) sie Shellvorgänge wie optimiertes Verschieben und [Delete_on_paste.](datascenarios.md) Shelldaten sind immer in einem Datenobjekt [enthalten,](dataobject.md) das eine [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) als allgemeinere Methode zum Charakterisieren von Daten verwendet. Der **cfFormat-Member der** -Struktur wird auf das Zwischenablageformat für das bestimmte Datenelement festgelegt. Die anderen Member stellen zusätzliche Informationen zur Verfügung, z. B. den Datenübertragungsmechanismus. Die Daten sind in einer zugehörigen [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) enthalten.

> [!Note]  
> Standardformatbezeichner der Zwischenablage haben das Format CF_ *XXX*. Ein gängiges Beispiel ist CF_TEXT, das zum Übertragen von ANSI-Textdaten verwendet wird. Diese Bezeichner verfügen über vordefinierte Werte und können direkt mit [**FORMATETC-Strukturen verwendet**](/windows/win32/api/objidl/ns-objidl-formatetc) werden. Mit Ausnahme von [CF_HDROP](#cf_hdrop)sind Shellformatbezeichner nicht vordefiniert. Mit Ausnahme von DragWindow haben sie das Format CFSTR_ *XXX*. Um diese Werte von vordefinierten Formaten zu unterscheiden, werden sie häufig als einfache Formate *bezeichnet.* Im Gegensatz zu vordefinierten Formaten müssen sie jedoch sowohl von der Quelle als auch vom Ziel registriert werden, bevor sie zum Übertragen von Daten verwendet werden können. Um ein Shellformat zu registrieren, schließen Sie die Headerdatei Shlobj.h ein, und übergeben Sie CFSTR_ *XXX-Formatbezeichner* an [RegisterClipboardFormat.](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) Diese Funktion gibt einen gültigen Zwischenablageformatwert zurück, der dann als **cfFormat-Member** einer **FORMATETC-Struktur verwendet werden** kann.

 

Die Shell-Zwischenablageformate sind hier basierend auf ihrer Verwendung in drei Gruppen organisiert.

-   [Formate zum Übertragen von Dateisystemobjekten](#formats-for-transferring-file-system-objects)
    -   [CF_HDROP](#cf_hdrop)
    -   [CFSTR_FILECONTENTS](#cfstr_filecontents)
    -   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
    -   [CFSTR_FILENAME](#cfstr_filename)
    -   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
    -   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
    -   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
    -   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)
-   [Formate für die Übertragung virtueller Objekte](#formats-for-transferring-virtual-objects)
    -   [CFSTR_NETRESOURCES](#cfstr_netresources)
    -   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
    -   [CFSTR_INETURL](#cfstr_ineturl)
    -   [CFSTR_SHELLURL (veraltet)](#cfstr_shellurl-deprecated)
-   [Formate für die Kommunikation zwischen Quelle und Ziel](#formats-for-communication-between-source-and-target)
    -   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
    -   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
    -   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
    -   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
    -   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
    -   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
    -   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
    -   [DragWindow](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>Formate zum Übertragen von Dateisystemobjekten

Diese Formate werden verwendet, um eine oder mehrere Dateien oder andere Shellobjekte zu übertragen.

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

Dieses Zwischenablageformat wird verwendet, wenn die Speicherorte einer Gruppe vorhandener Dateien übertragen werden. Im Gegensatz zu den anderen Shellformaten ist sie vordefiniert, sodass [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)nicht aufrufen muss. Die Daten bestehen aus einer [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Das **hGlobal-Member der** -Struktur verweist auf eine [**DROPFILES-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) als **hGlobal-Member.**

Das **pFiles-Member** der [**DROPFILES-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) enthält einen Offset zu einem mit **doppelt null beendeten** Zeichenarray, das die Dateinamen enthält. Wenn Sie ein CF_HDROP aus einem Datenobjekt extrahieren, können Sie [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) verwenden, um einzelne Dateinamen aus dem globalen Speicherobjekt zu extrahieren. Wenn Sie ein formatiertes CF_HDROP erstellen, das in einem Datenobjekt gespeichert werden soll, müssen Sie das Dateinamenarray erstellen.

Das Dateinamenarray besteht aus einer Reihe von Zeichenfolgen, die jeweils den vollqualifizierten Pfad einer Datei enthalten, einschließlich des beendenden **NULL-Zeichens.** An die **endgültige Zeichenfolge** wird ein zusätzliches NULL-Zeichen angefügt, um das Array zu beenden. Wenn beispielsweise die Dateien c:temp1.txt und c:temp2.txt werden, sieht das Zeichenarray \\ \\ wie hier gezeigt aus:


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> In diesem Beispiel wird '0' verwendet, um das NULL-Zeichen und nicht die literalen Zeichen, \\ die eingeschlossen werden sollen, zu repräsentieren. 


If the object was copied to the clipboard as part of a drag-and-drop operation, the **pt** member of the [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) structure contains the coordinates of the point where the object was dropped. Sie können [**DragQueryPoint verwenden,**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) um die Cursorkoordinaten zu extrahieren.

Wenn dieses Format in einem Datenobjekt vorhanden ist, simuliert eine OLE-Ziehschleife WM_DROPFILES Funktionalität mit Nicht-OLE-Abbruchzielen. [](wm-dropfiles.md) Dies ist wichtig, wenn Ihre Anwendung die Quelle eines Drag & Drop-Vorgangs auf einem Windows 3.1-System ist.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Dieser Formatbezeichner wird mit dem [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) verwendet, um Daten zu übertragen, als wäre es eine Datei, unabhängig davon, wie sie tatsächlich gespeichert werden. Die Daten bestehen aus einer [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die den Inhalt einer Datei darstellt. Die Datei wird normalerweise als Streamobjekt dargestellt, wodurch vermieden wird, dass der Inhalt der Datei im Arbeitsspeicher gespeichert werden muss. In diesem Fall wird der **tymed-Member** der **STGMEDIUM-Struktur** auf TYMED_ISTREAM festgelegt, und die Datei wird durch eine [**IStream-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-istream) dargestellt. Die Datei kann auch ein Speicher- oder globales Speicherobjekt (TYMED_ISTORAGE oder TYMED_HGLOBAL. Das zugeordnete CFSTR_FILEDESCRIPTOR enthält eine [**FILEDESCRIPTOR-Struktur**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) für jede Datei, die den Namen und die Attribute der Datei angibt.

Das Ziel behandelt die daten, die einem CFSTR_FILECONTENTS sind, als wäre es eine Datei. Wenn das Ziel [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufruft, um die Daten zu extrahieren, gibt es eine bestimmte Datei an, indem das **formatx-Element** der [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) auf den nullbasierten Index der [**FILEDESCRIPTOR-Struktur**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) der Datei im zugehörigen [CFSTR_FILEDESCRIPTOR-Format festgelegt](#cfstr_filedescriptor) wird. Das Ziel verwendet dann den zurückgegebenen Schnittstellenzeiger oder das globale Speicherhand handle, um die Daten zu extrahieren.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Dieser Formatbezeichner wird mit dem [CFSTR_FILECONTENTS](#cfstr_filecontents) verwendet, um Daten als Gruppe von Dateien zu übertragen. Diese beiden Formate sind die bevorzugte Methode zum Übertragen von Shellobjekten, die nicht als Dateisystemdateien gespeichert sind. Diese Formate können beispielsweise verwendet werden, um eine Gruppe von E-Mail-Nachrichten als einzelne Dateien zu übertragen, obwohl jede E-Mail tatsächlich als Datenblock in einer Datenbank gespeichert wird. Die Daten bestehen aus einer [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Das **hGlobal-Member** der -Struktur verweist auf eine [**FILEGROUPDESCRIPTOR-Struktur,**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) auf die ein Array folgt, das eine [**FILEDESCRIPTOR-Struktur**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) für jede Datei in der Gruppe enthält. Für jede **FILEDESCRIPTOR-Struktur** gibt es ein separates CFSTR_FILECONTENTS, das den Inhalt der Datei enthält. Um das Format einer bestimmten Datei CFSTR_FILECONTENTS, legen Sie den **lIndex-Wert** der [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) auf den nullbasierten Index der **FILEDESCRIPTOR-Struktur der Datei** fest.

Das CFSTR_FILEDESCRIPTOR format wird häufig verwendet, um Daten zu übertragen, als wäre es eine Gruppe von Dateien, unabhängig davon, wie sie tatsächlich gespeichert werden. Aus Sicht des Ziels stellt jedes CFSTR_FILECONTENTS eine einzelne Datei dar und wird entsprechend behandelt. Die Quelle kann die Daten jedoch auf beliebige Weise speichern. Während ein CSFTR_FILECONTENTS format einer einzelnen Datei entsprechen kann, kann es beispielsweise auch Daten darstellen, die von der Quelle aus einer Datenbank oder einem Textdokument extrahiert wurden.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Dieser Formatbezeichner wird verwendet, um eine einzelne Datei zu übertragen. Die Daten bestehen aus einer [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Das **hGlobal-Member der** -Struktur verweist auf eine einzelne mit **NULL** beendete Zeichenfolge, die den vollqualifizierten Dateipfad der Datei enthält. Dieses Format wurde durch CF_HDROP [](#cf_hdrop)ersetzt, wird jedoch aus Gründen der Abwärtskompatibilität mit Windows 3.1-Anwendungen unterstützt.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Dieser Formatbezeichner wird verwendet, wenn eine Gruppe von Dateien [CF_HDROP](#cf_hdrop) Format umbenannt und übertragen wird. Die Daten bestehen aus einer [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der -Struktur zeigt auf ein mit **doppelt NULL** endendes Zeichenarray. Dieses Array enthält einen neuen Namen für jede Datei in der reihenfolge, in der die Dateien im zugehörigen CF_HDROP Format aufgeführt sind. Das Format des Zeichenarrays entspricht dem Format, das von CF_HDROP zum Auflisten der übertragenen Dateien verwendet wird.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Dieser Formatbezeichner wird verwendet, um einen Pfad auf einem eingebundenen Volume zu übertragen. Sie ähnelt [CF_HDROP](#cf_hdrop), enthält jedoch nur einen einzigen Pfad und kann die längeren Pfadzeichenfolgen verarbeiten, die möglicherweise benötigt werden, um einen Pfad darzustellen, wenn das Volume in einem Ordner bereitgestellt wird. Die Daten bestehen aus einer [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der Struktur zeigt auf eine einzelne **NULL-endende** Zeichenfolge, die den vollqualifizierten Dateipfad enthält. Die Pfadzeichenfolge muss mit einem \\ ''-Zeichen enden, gefolgt vom abschließenden **NULL-Zeichen.**

Vor Windows 2000 konnten Volumes nur auf Laufwerkbuchstaben eingebunden werden. Für Windows Systeme ab 2000 mit einem NTFS-formatierten Laufwerk können Sie volumes auch in leeren Ordnern einbinden. Mit diesem Feature kann ein Volume eingebunden werden, ohne dass ein Laufwerkbuchstabe aufgenommen werden muss. Das eingebundene Volume kann jedes derzeit unterstützte Format verwenden, einschließlich FAT, FAT32, NTFS und CDFS.

Sie können einem Eigenschaftenblatt für Laufwerkeigenschaften Seiten hinzufügen, indem Sie einen [Eigenschaftenblatthandler](propsheet-handlers.md)implementieren. Wenn das Volume auf einem Laufwerkbuchstaben eingebunden ist, übergibt die Shell Pfadinformationen an den Handler mit dem [CF_HDROP](#cf_hdrop) Format. Bei systemen mit Windows 2000 und höher wird das CF_HDROP-Format verwendet, wenn ein Volume auf einem Laufwerkbuchstaben bereitgestellt wird, genau wie bei früheren Systemen. Wenn jedoch ein Volume in einem Ordner bereitgestellt wird, wird der [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) Formatbezeichner anstelle von CF_HDROP verwendet.

Wenn nur Laufwerkbuchstaben zum Einbinden von Volumes verwendet werden, werden nur [CF_HDROP](#cf_hdrop) verwendet, und vorhandene Eigenschaftenblatthandler funktionieren wie bei früheren Systemen. Wenn Ihr Handler jedoch eine Seite für Volumes anzeigen soll, die in Ordnern bereitgestellt werden, sowie Laufwerkbuchstaben, muss der Handler sowohl die CSFTR_MOUNTEDVOLUME- als auch die CF_HDROP-Formate verstehen können.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Dieser Formatbezeichner wird verwendet, wenn die Positionen eines oder mehrerer vorhandener Namespaceobjekte übertragen werden. Sie wird in etwa auf die gleiche Weise wie [CF_HDROP](#cf_hdrop)verwendet, enthält jedoch PIDLs anstelle von Dateisystempfaden. Die Verwendung von PIDLs ermöglicht es dem CFSTR_SHELLIDLIST-Format, sowohl virtuelle Objekte als auch Dateisystemobjekte zu verarbeiten. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der Struktur zeigt auf eine [**CIDA-Struktur.**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida)

Der **aoffset-Member** der [**CIDA-Struktur**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) ist ein Array, das Offsets bis zum Anfang der [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für jede übertragene PIDL enthält. Um eine bestimmte PIDL zu extrahieren, bestimmen Sie zunächst ihren Index. Fügen Sie dann der Adresse der **CIDA-Struktur** den **aoffset-Wert** hinzu, der diesem Index entspricht.

Das erste Element von **aoffset** enthält einen Offset zur vollqualifizierten PIDL eines übergeordneten Ordners. Wenn diese PIDL leer ist, ist der übergeordnete Ordner der Desktop. Jedes der verbleibenden Elemente des Arrays enthält einen Offset zu einer der zu übertragenden PIDLs. Alle diese PIDLs sind relativ zur PIDL des übergeordneten Ordners.

Die folgenden beiden Makros können verwendet werden, um PIDLs aus einer [**CIDA-Struktur**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) abzurufen. Der erste verwendet einen Zeiger auf die -Struktur und ruft die PIDL des übergeordneten Ordners ab. Die zweite verwendet einen Zeiger auf die -Struktur und ruft eine der anderen PIDLs ab, die durch ihren nullbasierten Index identifiziert werden.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> Der wert, der von diesen Makros zurückgegeben wird, ist ein Zeiger auf die [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) der PIDL. Da sich diese Strukturen in der Länge unterscheiden, müssen Sie das Ende der Struktur bestimmen, indem Sie jede der [**SHITEMID-Strukturen**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) der **ITEMIDLIST-Struktur** durchlaufen, bis Sie das 2-Byte **NULL** erreichen, das das Ende markiert.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Dieser Formatbezeichner wird mit Formaten wie [CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)und [CFSTR_FILECONTENTS](#cfstr_filecontents) verwendet, um die Position einer Gruppe von Objekten nach einer Übertragung anzugeben. Die Daten bestehen aus einer [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der Struktur zeigt auf ein Array von [**POINT-Strukturen.**](/previous-versions//dd162805(v=vs.85)) Die erste -Struktur gibt die Bildschirmkoordinaten in Pixel der oberen linken Ecke des Rechtecks an, das die Gruppe einschließt. Der Rest der Strukturen gibt die Positionen der einzelnen Objekte relativ zur Position der Gruppe an. Sie müssen in derselben Reihenfolge wie die zum Auflisten der Objekte im zugeordneten Format verwendeten reihenfolgen.

## <a name="formats-for-transferring-virtual-objects"></a>Formate für die Übertragung virtueller Objekte

Das CFSTR_SHELLIDLIST Format kann verwendet werden, um sowohl Dateisystem- als auch virtuelle Objekte zu übertragen. Es gibt jedoch auch mehrere spezielle Formate für die Übertragung bestimmter Typen von virtuellen Objekten.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (veraltet)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Dieser Formatbezeichner wird verwendet, wenn Netzwerkressourcen übertragen werden, z. B. eine Domäne oder ein Server. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der Struktur zeigt auf eine [**NRESARRAY-Struktur.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) Der **nr-Member** dieser Struktur gibt eine [**NETRESOURCE-Struktur**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) an, deren **lpRemoteName-Member** eine **mit NULL** endende Zeichenfolge enthält, die die Netzwerkressource identifiziert. Das Ablageziel kann dann die Daten mit einer der [Windows-Netzwerk-API-Funktionen (WNet),](../wnet/windows-networking-wnet-.md) z. B. [**WNetAddConnection,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)verwenden, um Netzwerkvorgänge für das Objekt auszuführen.

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Dieser Formatbezeichner wird beim Übertragen der Anzeigenamen von Druckern verwendet. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der Struktur zeigt auf eine Zeichenfolge im gleichen Format wie [bei CF_HDROP](#cf_hdrop). Der **pFiles-Member** der [**DROPFILES-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) enthält jedoch einen oder mehrere Anzeigenamen von Druckern anstelle von Dateipfaden.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Dieser Formatbezeichner ersetzt [CFSTR_SHELLURL (veraltet).](#cfstr_shellurl-deprecated) Wenn Ihre Anwendung zwischenablage-URLs bearbeiten soll, verwenden Sie CFSTR_INETURL anstelle von CFSTR_SHELLURL (veraltet). Dieses Format bietet die beste Darstellung einer einzelnen URL in der Zwischenablage. Wenn UNICODE nicht definiert ist, ruft die Anwendung die CF_TEXT/CFSTR_SHELLURL Version der URL ab. Wenn UNICODE definiert ist, ruft die Anwendung die CF_UNICODE Version der URL ab.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (veraltet)

> [!Note]  
> Dieser Formatbezeichner ist veraltet. Verwenden Sie stattdessen CFSTR_INETURL.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formate für die Kommunikation zwischen Quelle und Ziel

Diese Formatbezeichner ermöglichen die Kommunikation zwischen Quelle und Ziel. Die Formate unterstützen die Daten und bieten Anwendungen ein höheres Maß an Kontrolle über Vorgänge zum Verschieben, Kopieren und Einfügen oder Drag & Drop mit Shell-Objekten.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [DragWindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Dieser Formatbezeichner wird von einem Datenobjekt verwendet, um anzugeben, ob er sich in einer Drag & Drop-Schleife befindet. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der Struktur zeigt auf einen **DWORD-Wert.** If the **DWORD** value is nonzero, the data object is within a drag-and-drop loop. Wenn der Wert auf 0 (null) festgelegt ist, befindet sich das Datenobjekt nicht innerhalb einer Drag & Drop-Schleife.

Some drop targets might call [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) and attempt to extract data while the object is still within the drag-and-drop loop. Das vollständige Rendern des Objekts für jedes derartige Vorkommen kann dazu führen, dass der Ziehcursor angehalten wird. If the data object supports [CFSTR_INDRAGLOOP](#cfstr_indragloop), the target can instead use that format to check the status of the drag-and-drop loop and avoid memory intensive rendering of the object until it is actually dropped. Die formate, die speicherintensiv zu rendern [](/windows/win32/api/objidl/ns-objidl-formatetc) sind, sollten weiterhin im FORMATETC-Enumerator und in Aufrufen von [**IDataObject::QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata)enthalten sein. Wenn das Datenobjekt CFSTR_INDRAGLOOP nicht festgelegt hat, sollte es so fungieren, als ob der Wert auf 0 (null) festgelegt wäre.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Version 5.0.](versions.md) Mit diesem Formatbezeichner kann eine Ablagequelle die [**IDataObject::GetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) des Datenobjekts aufrufen, um das Ergebnis einer Shell-Datenübertragung zu bestimmen. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der Struktur zeigt auf ein DWORD, das einen [**DROPEFFECT-Wert**](../com/dropeffect-constants.md) enthält.

Der [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) Formatbezeichner sollte es dem Ziel ermöglichen, dem Datenobjekt anzugeben, welcher Vorgang tatsächlich durchgeführt wurde. Die Shell verwendet jedoch nach Möglichkeit [optimierte Verschiebungen](datascenarios.md) für Dateisystemobjekte. In diesem Fall legt die Shell normalerweise den CFSTR_PERFORMEDDROPEFFECT Wert auf DROPEFFECT_NONE fest, um dem Datenobjekt anzugeben, dass die ursprünglichen Daten gelöscht wurden. Daher kann die Quelle den CFSTR_PERFORMEDDROPEFFECT Wert nicht verwenden, um zu bestimmen, welcher Vorgang stattgefunden hat. Obwohl die meisten Quellen diese Informationen nicht benötigen, gibt es einige Ausnahmen. Auch wenn optimierte Verschiebebewegungen beispielsweise die Notwendigkeit einer Quelle zum Löschen von Daten beseitigen, muss die Quelle möglicherweise trotzdem eine verknüpfte Datenbank aktualisieren, um anzugeben, dass die Dateien verschoben oder kopiert wurden.

Wenn eine Quelle wissen muss, welcher Vorgang stattgefunden hat, kann sie die [**IDataObject::GetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) des Datenobjekts aufrufen und das CFSTR_LOGICALPERFORMEDDROPEFFECT anfordern. Dieses Format spiegelt im Wesentlichen wider, was aus Sicht des Benutzers geschieht, nachdem der Vorgang abgeschlossen ist. Wenn eine neue Datei erstellt und die ursprüngliche Datei gelöscht wird, wird dem Benutzer ein Move-Vorgang angezeigt, und der Datenwert des Formats wird auf DROPEFFECT_MOVE. Wenn die ursprüngliche Datei noch dort ist, wird dem Benutzer ein Kopiervorgang angezeigt, und der Datenwert des Formats wird auf DROPEFFECT_COPY. Wenn ein Link erstellt wurde, wird der Datenwert des Formats DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

Dieser Formatbezeichner wird vom Ziel verwendet, um das Datenobjekt über seine [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) darüber zu informieren, dass ein Vorgang zum Löschen beim Einfügen erfolgreich war. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member der** -Struktur verweist auf ein **DWORD, das** einen [**DROPEFFECT-Wert**](../com/dropeffect-constants.md) enthält. Dieses Format wird verwendet, um das Datenobjekt zu benachrichtigen, dass es den Ausschneidevorgang abschließen und die ursprünglichen Daten bei Bedarf löschen soll. Weitere Informationen finden Sie unter [Vorgänge zum Löschen beim Einfügen.](datascenarios.md)

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

Dieser Formatbezeichner wird vom Ziel verwendet, um das Datenobjekt über seine [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) über das Ergebnis einer Datenübertragung zu informieren. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Der **hGlobal-Member** der -Struktur verweist auf einen **DWORD-Wert,** der auf den entsprechenden [**DROPEFFECT-Wert**](../com/dropeffect-constants.md) festgelegt ist, normalerweise DROPEFFECT_MOVE oder DROPEFFECT_COPY.

Dieses Format wird normalerweise verwendet, wenn das Ergebnis eines Vorgangs [](datascenarios.md) entweder verschieben oder kopieren kann, z. B. bei einem optimierten Verschieben oder Beim Einfügen löschen. Es bietet dem Ziel eine zuverlässige Möglichkeit, dem Datenobjekt mitteilen zu können, was tatsächlich passiert ist. Es wurde eingeführt, da der wert von *pdwEffect,* der von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) zurückgegeben wurde, nicht zuverlässig darauf hindeuten konnte, welcher Vorgang stattgefunden hat. Das [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) ist die zuverlässige Möglichkeit, anzugeben, dass eine nicht optimierte Bewegung stattgefunden hat.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

Dieser Formatbezeichner wird von der Quelle verwendet, um anzugeben, ob die bevorzugte Methode der Datenübertragung verschieben oder kopieren wird. Ein Abbruchziel fordert dieses Format an, indem es die [**IDataObject::GetData-Methode des Datenobjekts**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufruft. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Das **hGlobal-Member der** -Struktur verweist auf einen **DWORD-Wert.** Dieser Wert wird auf DROPEFFECT_MOVE, wenn ein Move-Vorgang bevorzugt wird, oder DROPEFFECT_COPY, wenn ein Kopiervorgang bevorzugt wird.

Dieses Feature wird verwendet, wenn eine Quelle einen Verschieben- oder Kopiervorgang unterstützen kann. Es verwendet das [CFSTR_PREFERREDDROPEFFECT,](#cfstr_preferreddropeffect) um seine Präferenz an das Ziel zu übermitteln. Da das Ziel nicht dazu verpflichtet ist, die Anforderung zu verarbeiten, muss das Ziel die [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) der Quelle mit einem [CFSTR_PERFORMEDDROPEFFECT-Format](#cfstr_performeddropeffect) aufrufen, um dem Datenobjekt mitteilen zu können, welcher Vorgang tatsächlich ausgeführt wurde.

Bei einem [Delete-on-Paste-Vorgang](datascenarios.md) wird das CFSTR_PREFERREDDROPFORMAT verwendet, um das Ziel darüber zu informieren, ob die Quelle einen Ausschneide- oder Kopiervorgang durchgeführt hat. Mit einem Drag & Drop-Vorgang können Sie CFSTR_PREFERREDDROPFORMAT, um die Shellaktion anzugeben. Wenn dieses Format nicht vorhanden ist, führt die Shell eine Standardaktion basierend auf dem Kontext aus. Wenn ein Benutzer beispielsweise eine Datei von einem Volume zieht und auf einem anderen Volume ablaget, ist die Standardaktion der Shell das Kopieren der Datei. Durch das CFSTR_PREFERREDDROPFORMAT in das Datenobjekt können Sie die Standardaktion überschreiben und die Shell explizit anschreiben, die Datei zu kopieren, zu verschieben oder zu verknüpfen. If the user chooses to drag with the right button, CFSTR_PREFERREDDROPFORMAT specifies the default command on the [drag-and-drop](context-menu-handlers.md) shortcut menu. Der Benutzer kann weiterhin andere Befehle im Menü auswählen.

Vor Microsoft Internet Explorer 4.0 hat eine Anwendung angegeben, dass Verknüpfungsdateitypen übertragen wurden, indem FD_LINKUI im **dwFlags-Member** der [**FILEDESCRIPTOR-Struktur angegeben**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) wurde. Ziele mussten dann einen potenziell zeitaufwändigen Aufruf von [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) verwenden, um herauszufinden, ob das FD_LINKUI festgelegt wurde. Nun ist die bevorzugte Möglichkeit, anzugeben, dass Verknüpfungen übertragen werden, die Verwendung des CFSTR_PREFERREDDROPEFFECT, das auf DROPEFFECT_LINK. Aus Gründen der Abwärtskompatibilität mit älteren Systemen sollten Quellen jedoch weiterhin das Flag FD_LINKUI festlegen.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Dieser Formatbezeichner wird von einem Ziel verwendet, um seine CLSID für die Quelle zur Verfügung zu stellen. Die Daten sind eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die ein globales Speicherobjekt enthält. Das **hGlobal-Member der** -Struktur verweist auf die CLSID-GUID des Abbruchziels.

Dieses Format wird hauptsächlich verwendet, um zu ermöglichen, dass Objekte gelöscht werden, indem sie in die Papierkorb. Wenn ein Objekt im Papierkorb gelöscht wird, wird die [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) der Quelle mit einem CFSTR_TARGETCLSID-Format aufgerufen, das auf die CLSID (CLSID_RecycleBin) des Papierkorb festgelegt ist. Die Quelle kann dann das ursprüngliche Objekt löschen.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

This format identifier is used by Windows Internet Explorer and the Windows Shell to provide a mechanism through which to block or prompt for drag-and-drop operations originating from Internet Explorer in conjunction with the [**URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) flag.

**CFSTR_UNTRUSTEDDRAGDROP** is added by the source of a drag-and-drop operation to specify that the data object might contain untrustworthy data. Die Daten werden durch eine [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) dargestellt, die ein globales Speicherobjekt enthält. Das **hGlobal-Member** der Struktur verweist auf ein **DWORD-Flag,** das auf ein entsprechendes URL-Aktionsflag festgelegt ist, um eine Richtlinienüberprüfung über die [**IInternetSecurityManager::P rocessUrlAction-Methode**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) mithilfe des PUAF_ENFORCERESTRICTED-Flags [**zu verursachen.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85)) [](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85))

### <a name="dragwindow"></a>DragWindow

Dieses Format wird in einem Drag & Drop-Vorgang verwendet, um das Ziehbild (Fenster) eines Objekts zu identifizieren, sodass seine visuellen Informationen dynamisch aktualisiert werden können. Wenn ein Objekt über ein Absturzziel gezogen wird, aktualisiert eine Anwendung ihre [**DROPDESCRIPTION-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) als Reaktion auf die [**IDropTarget::D ragOver-**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) oder [**IDropSource::GiveFeedback-Methode.**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) **DROPDESCRIPTION wird mit** einem neuen [**DROPIMAGETYPE-Wert**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) aktualisiert, der die Aufschrift angibt, die auf das Visual des Ziehfensters angewendet werden soll. Beispielsweise ein Hinweis darauf, dass die Datei kopiert und nicht verschoben wird oder dass das Objekt nicht an diesem Speicherort gelöscht werden kann. Bis das -Objekt jedoch eine [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) empfängt, werden die Visuals nicht aktualisiert. Dieses Format stellt den **HWND** des Ziehfensters des Empfängers an den Absender der **DDWM_UPDATEWINDOW** zur Verfügung.

Die Zwischenablagedaten sind vom Typ [**TYMED_HGLOBAL.**](/windows/win32/api/objidl/ne-objidl-tymed) Es handelt sich um **eine DWORD-Darstellung** eines **HWND.** Die Daten können an die in Basetsd.h definierte **ULongToHandle-Funktion** übergeben werden, um ein 64-Bit-HWND für die Verwendung auf 64-Bit-Windows. 

Dieses Format erfordert nicht die Einbeziehung von Shlobj.h.

 

 
