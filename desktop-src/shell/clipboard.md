---
description: Shellzwischenablage Formate werden verwendet, um den Typ der shelldaten zu identifizieren, die über die Zwischenablage übertragen werden.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Shellzwischenablage Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674ccc33db3a35a1a60abb549f5e1ab5b5c96760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750265"
---
# <a name="shell-clipboard-formats"></a>Shellzwischenablage Formate

Shellzwischenablage Formate werden verwendet, um den Typ der shelldaten zu identifizieren, die über die Zwischenablage übertragen werden. Die meisten shellzwischenablage Formate identifizieren einen Datentyp, z. b. eine Liste mit Dateinamen oder Zeiger auf elementbezeichnerlisten (pidls). Einige Formate werden jedoch für die Kommunikation zwischen Quelle und Ziel verwendet. Sie können den Datenübertragungs Prozess beschleunigen, indem Sie Shellvorgänge wie [optimierte Verschiebung](datascenarios.md) und [delete_on_paste](datascenarios.md)unterstützen. Shelldaten sind immer in einem [Datenobjekt](dataobject.md) enthalten, das eine [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur als allgemeinere Methode zum charakterisieren von Daten verwendet. Der **cfFormat** -Member der Struktur wird für das jeweilige Datenelement auf das Zwischenablage Format festgelegt. Die anderen Mitglieder stellen zusätzliche Informationen bereit, z. b. den Datenübertragungsmechanismus. Die Daten sind in einer zugehörigen [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur enthalten.

> [!Note]  
> Standard Bezeichner für die Zwischenablage haben das Format CF_ *xxx*. Ein gängiges Beispiel ist CF_TEXT, mit dem ANSI-Textdaten übertragen werden. Diese Bezeichner verfügen über vordefinierte Werte und können direkt mit [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Strukturen verwendet werden. Mit Ausnahme von [CF_HDROP](#cf_hdrop)sind shellformatbezeichner nicht vordefiniert. Mit der Ausnahme dragwindow haben Sie die Form CFSTR_ *xxx*. Um diese Werte von vordefinierten Formaten zu unterscheiden, werden Sie häufig als einfache *Formate* bezeichnet. Anders als bei vordefinierten Formaten müssen Sie jedoch sowohl von der Quelle als auch vom Ziel registriert werden, bevor Sie zum Übertragen von Daten verwendet werden können. Zum Registrieren eines shellformats schließen Sie die Header Datei "shlobj. h" ein, und übergeben Sie den Format Bezeichner "CFSTR_ *xxx* " an " [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)". Diese Funktion gibt einen gültigen Wert für die Zwischenablage Format zurück, der dann als **cfFormat** -Member einer **FORMATETC** -Struktur verwendet werden kann.

 

Die shellzwischenablage Formate sind hier in drei Gruppen angeordnet, je nachdem, wie Sie verwendet werden.

-   [Formate für das Übertragen von Datei System Objekten](#formats-for-transferring-file-system-objects)
    -   [CF_HDROP](#cf_hdrop)
    -   [CFSTR_FILECONTENTS](#cfstr_filecontents)
    -   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
    -   [CFSTR_FILENAME](#cfstr_filename)
    -   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
    -   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
    -   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
    -   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)
-   [Formate für das Übertragen von virtuellen Objekten](#formats-for-transferring-virtual-objects)
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
    -   [Dragwindow](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>Formate für das Übertragen von Datei System Objekten

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

Dieses Zwischenablage Format wird verwendet, wenn die Speicherorte einer Gruppe vorhandener Dateien übertragen werden. Anders als bei den anderen shellformaten ist es vordefiniert, sodass es nicht erforderlich ist, [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)aufzurufen. Die Daten bestehen aus einer [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf eine [**dropfiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) -Struktur als sein **HGLOBAL** -Member.

Der **pfiles** -Member der [**dropfiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) -Struktur enthält einen Offset zu einem Double- **null**-terminierten Zeichen Array, das die Dateinamen enthält. Wenn Sie ein CF_HDROP Format aus einem Datenobjekt extrahieren, können Sie [**dragqueryfile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) verwenden, um einzelne Dateinamen aus dem globalen Speicher Objekt zu extrahieren. Wenn Sie ein CF_HDROP-Format erstellen, das in einem Datenobjekt platziert werden soll, müssen Sie das Dateinamen Array erstellen.

Das Dateinamen Array besteht aus einer Reihe von Zeichen folgen, die jeweils den voll qualifizierten Pfad einer Datei enthalten, einschließlich des abschließenden **null** -Zeichens. Ein zusätzliches **null** -Zeichen wird an die endgültige Zeichenfolge angehängt, um das Array zu beenden. Wenn z. b. die Dateien c: \\temp1.txt und c: \\temp2.txt übertragen werden, sieht das Zeichen Array wie folgt aus:


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> In diesem Beispiel wird " \\ 0" verwendet, um das **null** -Zeichen darzustellen, nicht die Literalzeichen, die eingeschlossen werden sollen.


Wenn das Objekt als Teil eines Drag & Drop-Vorgangs in die Zwischenablage kopiert wurde, enthält der **PT** -Member der [**dropfiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) -Struktur die Koordinaten des Punkts, an dem das Objekt abgelegt wurde. Sie können [**dragquerypoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) verwenden, um die Cursor Koordinaten zu extrahieren.

Wenn dieses Format in einem Datenobjekt vorhanden ist, simuliert eine OLE-Drag-Schleife [**WM_DROPFILES**](wm-dropfiles.md) Funktionen mit nicht-OLE-Ablage Zielen. Dies ist wichtig, wenn Ihre Anwendung die Quelle eines Drag & Drop-Vorgangs auf einem Windows 3,1-System ist.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Dieser Format Bezeichner wird mit dem [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) -Format verwendet, um Daten zu übertragen, als ob es sich um eine Datei handelt, unabhängig davon, wie Sie tatsächlich gespeichert wird. Die Daten bestehen aus einer [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die den Inhalt einer Datei darstellt. Die Datei wird normalerweise als Streamobjekt dargestellt, das den Inhalt der Datei nicht im Arbeitsspeicher platzieren muss. In diesem Fall wird der **TYMED** -Member der **STGMEDIUM** -Struktur auf TYMED_ISTREAM festgelegt, und die Datei wird durch eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle dargestellt. Bei der Datei kann es sich auch um ein Speicher Objekt oder ein globales Speicher Objekt (TYMED_ISTORAGE oder TYMED_HGLOBAL) handeln. Das zugeordnete CFSTR_FILEDESCRIPTOR Format enthält eine [**Filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) -Struktur für jede Datei, die den Namen und die Attribute der Datei angibt.

Das Ziel behandelt die einem CFSTR_FILECONTENTS Format zugeordneten Daten so, als ob es sich um eine Datei handelt. Wenn das Ziel [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufruft, um die Daten zu extrahieren, wird eine bestimmte Datei angegeben, indem der **Lindex** -Member der [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur auf den NULL basierten Index der [**Filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) -Struktur der Datei im zugehörigen [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) Format festgelegt wird. Das Ziel verwendet dann den zurückgegebenen Schnittstellen Zeiger oder das globale Speicher handle, um die Daten zu extrahieren.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Dieser Format Bezeichner wird mit dem [CFSTR_FILECONTENTS](#cfstr_filecontents) -Format verwendet, um Daten als Gruppe von Dateien zu übertragen. Diese beiden Formate sind die bevorzugte Methode zum Übertragen von shellobjekten, die nicht als Dateisystem Dateien gespeichert werden. Diese Formate können z. b. verwendet werden, um eine Gruppe von e-Mail-Nachrichten als einzelne Dateien zu übertragen, obwohl jede e-Mail-Adresse tatsächlich als Datenblock in einer Datenbank gespeichert ist. Die Daten bestehen aus einer [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf eine [**filegroupdescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) -Struktur, auf die ein Array folgt, das eine [**Filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) -Struktur für jede Datei in der Gruppe enthält. Für jede **Datei deskriptorstruktur** gibt es ein separates CFSTR_FILECONTENTS Format, das den Inhalt der Datei enthält. Legen Sie den **Lindex** -Wert der [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur auf den NULL basierten Index der **Filedescriptor** -Struktur der Datei fest, um das CFSTR_FILECONTENTS Format einer bestimmten Datei zu identifizieren.

Das CFSTR_FILEDESCRIPTOR Format wird häufig verwendet, um Daten zu übertragen, als ob es sich um eine Gruppe von Dateien handelt, unabhängig davon, wie Sie tatsächlich gespeichert wird. Aus Sicht des Ziels stellt jedes CFSTR_FILECONTENTS Format eine einzelne Datei dar und wird entsprechend behandelt. Die Quelle kann die Daten jedoch in beliebiger Weise speichern. Während ein CSFTR_FILECONTENTS Format einer einzelnen Datei entsprechen kann, kann es beispielsweise auch Daten darstellen, die von der Quelle aus einer Datenbank oder einem Textdokument extrahiert werden.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Dieser Format Bezeichner wird verwendet, um eine einzelne Datei zu übertragen. Die Daten bestehen aus einer [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf eine einzelne auf **null** endenden Zeichenfolge, die den voll qualifizierten Dateipfad der Datei enthält. Dieses Format wurde durch [CF_HDROP](#cf_hdrop)abgelöst, wird jedoch aus Gründen der Abwärtskompatibilität mit Windows 3,1-Anwendungen unterstützt.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Dieser Format Bezeichner wird verwendet, wenn eine Gruppe von Dateien im [CF_HDROP](#cf_hdrop) Format umbenannt und übertragen wird. Die Daten bestehen aus einer [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf ein Double- **null**-terminiertes Zeichen Array. Dieses Array enthält einen neuen Namen für jede Datei in derselben Reihenfolge, in der die Dateien im zugehörigen CF_HDROP Format aufgeführt sind. Das Format des Zeichen Arrays ist identisch mit dem, das von CF_HDROP zum Auflisten der übertragenen Dateien verwendet wird.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Dieser Format Bezeichner wird verwendet, um einen Pfad auf einem bereitgestellten Volume zu übertragen. Sie ähnelt [CF_HDROP](#cf_hdrop), aber Sie enthält nur einen einzigen Pfad und kann die längeren Pfad Zeichenfolgen verarbeiten, die möglicherweise erforderlich sind, um einen Pfad darzustellen, wenn das Volume in einem Ordner bereitgestellt wird. Die Daten bestehen aus einer [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf eine einzelne auf **null** endenden Zeichenfolge, die den voll qualifizierten Dateipfad enthält. Die Pfad Zeichenfolge muss mit \\ dem Zeichen ' ' enden, gefolgt von dem abschließenden **null**-Zeichen.

Vor Windows 2000 konnten Volumes nur auf Laufwerk Buchstaben eingebunden werden. Für Windows 2000-Systeme und spätere Systeme mit einem NTFS-formatierten Laufwerk können Sie auch Volumes in leeren Ordnern einbinden. Diese Funktion ermöglicht es, ein Volume bereitzustellen, ohne einen Laufwerk Buchstaben zu übernehmen. Das bereitgestellte Volume kann alle derzeit unterstützten Formate verwenden, einschließlich FAT, FAT32, NTFS und CDFS.

Sie können Seiten zu einem Eigenschaften Blatt für Laufwerks Eigenschaften hinzufügen, indem Sie einen [Eigenschaften Blatt Handler](propsheet-handlers.md)implementieren. Wenn das Volume auf einen Laufwerk Buchstaben eingebunden ist, übergibt die Shell Pfadinformationen mit dem [CF_HDROP](#cf_hdrop) -Format an den Handler. Bei Windows 2000 und neueren Systemen wird das CF_HDROP Format verwendet, wenn ein Volume wie bei früheren Systemen auf einem Laufwerk Buchstaben bereitgestellt wird. Wenn ein Volume jedoch in einem Ordner bereitgestellt wird, wird der [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) -Format Bezeichner anstelle von CF_HDROP verwendet.

Wenn nur Laufwerksbuchstaben zum Einbinden von Volumes verwendet werden, werden nur [CF_HDROP](#cf_hdrop) verwendet, und vorhandene Eigenschaften Blatt Handler funktionieren wie bei früheren Systemen. Wenn Sie jedoch möchten, dass Ihr Handler eine Seite für Volumes anzeigt, die in Ordnern und Laufwerk Buchstaben eingebunden sind, muss der Handler sowohl das CSFTR_MOUNTEDVOLUME-als auch das CF_HDROP-Format verstehen können.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Dieser Format Bezeichner wird verwendet, wenn die Speicherorte von einem oder mehreren vorhandenen Namespace Objekten übertragen werden. Es wird auf die gleiche Weise wie [CF_HDROP](#cf_hdrop)verwendet, aber es enthält pidls anstelle von Dateisystem Pfaden. Mithilfe von pidls kann das CFSTR_SHELLIDLIST-Format sowohl virtuelle Objekte als auch Dateisystem Objekte verarbeiten. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf eine [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) -Struktur.

Der **aoffset** -Member der [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) -Struktur ist ein Array, das Offsets zum Anfang der [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur für jede PIDL enthält, die übertragen wird. Um eine bestimmte PIDL zu extrahieren, bestimmen Sie zuerst den Index. Fügen Sie dann der Adresse der **CIDA** -Struktur den **aoffset** -Wert hinzu, der diesem Index entspricht.

Das erste Element von **aoffset** enthält einen Offset zur voll qualifizierten PIDL eines übergeordneten Ordners. Wenn diese PIDL leer ist, ist der übergeordnete Ordner der Desktop. Jedes der verbleibenden Elemente des Arrays enthält einen Offset zu einer der zu übertragenden pidls. Alle diese pidls sind relativ zur PIDL des übergeordneten Ordners.

Die folgenden beiden Makros können zum Abrufen von pidls aus einer [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) -Struktur verwendet werden. Der erste übernimmt einen Zeiger auf die-Struktur und ruft die PIDL des übergeordneten Ordners ab. Der zweite-Wert übernimmt einen Zeiger auf die-Struktur und ruft eine der anderen pidls ab, die durch den NULL basierten Index identifiziert werden.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> Der von diesen Makros zurückgegebene Wert ist ein Zeiger auf die [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur der PIDL. Da diese Strukturen die Länge variieren, müssen Sie das Ende der Struktur ermitteln, indem Sie die [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Strukturen der **itemidlist** -Struktur durchlaufen, bis Sie den 2-Byte- **null** -Wert erreichen, der das Ende markiert.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Dieser Format Bezeichner wird mit Formaten wie [CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)und [CFSTR_FILECONTENTS](#cfstr_filecontents) verwendet, um die Position einer Gruppe von Objekten nach einer Übertragung anzugeben. Die Daten bestehen aus einer [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf ein Array von [**Punkt**](/previous-versions//dd162805(v=vs.85)) Strukturen. Die erste-Struktur gibt die Bildschirm Koordinaten der oberen linken Ecke des Rechtecks, das die Gruppe einschließt, in Pixel an. Die übrigen Strukturen geben die Speicherorte der einzelnen Objekte relativ zur Position der Gruppe an. Sie müssen in derselben Reihenfolge vorliegen wie die, die zum Auflisten der Objekte im zugeordneten Format verwendet wurde.

## <a name="formats-for-transferring-virtual-objects"></a>Formate für das Übertragen von virtuellen Objekten

Das CFSTR_SHELLIDLIST-Format kann verwendet werden, um sowohl das Dateisystem als auch virtuelle Objekte zu übertragen. Es gibt jedoch auch mehrere spezielle Formate zum übertragen bestimmter Typen von virtuellen Objekten.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (veraltet)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Diese Format-ID wird verwendet, wenn Netzwerkressourcen übertragen werden, z. b. eine Domäne oder ein Server. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf eine [**nresarray**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) -Struktur. Der **Nr** -Member dieser Struktur gibt eine [**artresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) -Struktur an, deren **lpremutename** -Member eine **null**-terminierte Zeichenfolge enthält, die die Netzwerkressource identifiziert. Das Ablage Ziel kann dann die Daten mit allen WNET-API-Funktionen [(Windows Networking)](../wnet/windows-networking-wnet-.md) , wie z. b. [**wnetaddconnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona), zum Ausführen von Netzwerk Vorgängen für das Objekt verwenden.

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Dieser Format Bezeichner wird beim Übertragen der anzeigen Amen von Druckern verwendet. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf eine Zeichenfolge im gleichen Format wie bei [CF_HDROP](#cf_hdrop). Der **pfiles** -Member der [**dropfiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) -Struktur enthält jedoch einen oder mehrere anzeigen Amen von Druckern anstelle von Dateipfaden.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Dieser Format Bezeichner ersetzt [CFSTR_SHELLURL (veraltet)](#cfstr_shellurl-deprecated). Wenn Sie möchten, dass Ihre Anwendung Zwischenablage-URLs bearbeitet, verwenden Sie CFSTR_INETURL anstelle von CFSTR_SHELLURL (veraltet). Dieses Format gibt die beste Darstellung einer einzelnen URL in der Zwischenablage an. Wenn Unicode nicht definiert ist, ruft die Anwendung die CF_TEXT/CFSTR_SHELLURL-Version der URL ab. Wenn Unicode definiert ist, ruft die Anwendung die CF_UNICODE Version der URL ab.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (veraltet)

> [!Note]  
> Der Format Bezeichner ist veraltet. Verwenden Sie stattdessen CFSTR_INETURL.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formate für die Kommunikation zwischen Quelle und Ziel

Diese Format Bezeichner ermöglichen die Kommunikation zwischen Quelle und Ziel. Die Formate unterstützen die Daten und haben Anwendungen ein höheres Maß an Kontrolle über Verschiebe-und Kopiervorgänge oder Drag & Drop-Vorgänge mit shellobjekten.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [Dragwindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Dieser Format Bezeichner wird von einem Datenobjekt verwendet, um anzugeben, ob es sich um eine Drag & Drop-Schleife handelt. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf einen **DWORD** -Wert. Wenn der **DWORD** -Wert ungleich 0 (null) ist, befindet sich das Datenobjekt innerhalb einer Drag & Drop-Schleife. Wenn der Wert auf 0 (null) festgelegt ist, befindet sich das Datenobjekt nicht innerhalb einer Drag & Drop-Schleife.

Einige Drop-Ziele können [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufrufen und versuchen, Daten zu extrahieren, während sich das Objekt noch innerhalb der Drag & Drop-Schleife befindet. Das vollständige Rendering des-Objekts für jedes derartige vorkommen kann dazu führen, dass der Zieh Cursor abwartet. Wenn das Datenobjekt [CFSTR_INDRAGLOOP](#cfstr_indragloop)unterstützt, kann das Ziel stattdessen dieses Format verwenden, um den Status der Drag & Drop-Schleife zu überprüfen und das speicherintensive Rendering des Objekts zu vermeiden, bis es tatsächlich gelöscht wird. Die Formate, die Speicher intensiv zum renderingelement sind, sollten weiterhin im [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Enumerator und in Aufrufen von [**IDataObject:: QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata)enthalten sein. Wenn das Datenobjekt nicht CFSTR_INDRAGLOOP festgelegt wird, sollte es so agieren, als wäre der Wert auf 0 (null) festgelegt.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Version 5,0.](versions.md) Mit diesem Format Bezeichner kann eine Ablage Quelle die [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) -Methode des Datenobjekts aufrufen, um das Ergebnis einer shelldatenübertragung zu ermitteln. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf ein DWORD, das einen [**dropffect**](../com/dropeffect-constants.md) -Wert enthält.

Der [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) -Format Bezeichner war für das Ziel vorgesehen, dem Datenobjekt anzugeben, welcher Vorgang tatsächlich durchgeführt wurde. Die Shell verwendet jedoch nach Möglichkeit [optimierte](datascenarios.md) Verschiebungen für Dateisystem Objekte. In diesem Fall legt die Shell normalerweise den CFSTR_PERFORMEDDROPEFFECT Wert auf DROPEFFECT_NONE fest, um das Datenobjekt anzugeben, dass die ursprünglichen Daten gelöscht wurden. Daher kann die Quelle den CFSTR_PERFORMEDDROPEFFECT Wert nicht verwenden, um zu bestimmen, welcher Vorgang stattfindet. Obwohl die meisten Quellen diese Informationen nicht benötigen, gibt es einige Ausnahmen. Obwohl durch optimierte Verschiebungen beispielsweise die Notwendigkeit einer Quelle zum Löschen von Daten entfällt, muss die Quelle möglicherweise trotzdem eine verwandte Datenbank aktualisieren, um anzugeben, dass die Dateien verschoben oder kopiert wurden.

Wenn eine Quelle wissen muss, welcher Vorgang stattfindet, kann Sie die [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) -Methode des Datenobjekts aufrufen und das CFSTR_LOGICALPERFORMEDDROPEFFECT Format anfordern. Dieses Format spiegelt im Grunde wider, was aus der Sicht des Benutzers geschieht, nachdem der Vorgang beendet wurde. Wenn eine neue Datei erstellt und die ursprüngliche Datei gelöscht wird, wird dem Benutzer ein Verschiebungs Vorgang angezeigt, und der Datenwert des Formats wird auf DROPEFFECT_MOVE festgelegt. Wenn die ursprüngliche Datei noch vorhanden ist, wird dem Benutzer ein Kopiervorgang angezeigt, und der Datenwert des Formats wird auf DROPEFFECT_COPY festgelegt. Wenn ein Link erstellt wurde, wird der Datenwert des Formats DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

Dieser Format Bezeichner wird vom Ziel verwendet, um das Datenobjekt über seine [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode zu informieren, dass ein Löschvorgang erfolgreich ausgeführt wurde. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf ein **DWORD** , das einen [**dropffect**](../com/dropeffect-constants.md) -Wert enthält. Dieses Format wird verwendet, um das Datenobjekt zu benachrichtigen, dass es den Ausschneide Vorgang beenden und ggf. die ursprünglichen Daten löschen soll. Weitere Informationen finden Sie unter [Delete-on-Copy-Vorgänge](datascenarios.md).

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

Dieser Format Bezeichner wird vom Ziel verwendet, um das Datenobjekt über die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode des Ergebnisses einer Datenübertragung zu informieren. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf ein **DWORD** -Element, das auf den entsprechenden [**droetffect**](../com/dropeffect-constants.md) -Wert festgelegt ist, normalerweise DROPEFFECT_MOVE oder DROPEFFECT_COPY.

Dieses Format wird normalerweise verwendet, wenn das Ergebnis eines Vorgangs entweder verschoben oder kopiert werden kann, z. b. bei einem [optimierten](datascenarios.md) verschiebe-oder Löschvorgang. Er bietet eine zuverlässige Möglichkeit für das Ziel, dem Datenobjekt mitzuteilen, was tatsächlich passiert ist. Es wurde eingeführt, weil der von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) zurückgegebene Wert von *pdweffect* nicht zuverlässig anzeigt, welcher Vorgang durchgeführt wurde. Das [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) -Format ist die zuverlässige Möglichkeit, um anzugeben, dass eine nicht optimierte Verschiebung stattfindet.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

Dieser Format Bezeichner wird von der Quelle verwendet, um anzugeben, ob die bevorzugte Methode für die Datenübertragung verschoben oder kopiert werden soll. Ein Ablage Ziel fordert dieses Format durch Aufrufen der [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) -Methode des Datenobjekts an. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf einen **DWORD** -Wert. Dieser Wert wird auf DROPEFFECT_MOVE festgelegt, wenn ein Verschiebungs Vorgang bevorzugt wird, oder DROPEFFECT_COPY, wenn ein Kopiervorgang bevorzugt wird.

Diese Funktion wird verwendet, wenn eine Quelle entweder einen verschiebe-oder Kopiervorgang unterstützt. Er verwendet das [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) -Format, um seine Präferenz an das Ziel zu übermitteln. Da das Ziel nicht zur Einhaltung der Anforderung verpflichtet ist, muss das Ziel die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode der Quelle mit einem [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) Format aufrufen, um dem Datenobjekt mitzuteilen, welcher Vorgang tatsächlich ausgeführt wurde.

Bei einem [Delete-on-Paste-](datascenarios.md) Vorgang wird das CFSTR_PREFERREDDROPFORMAT Format verwendet, um dem Ziel mitzuteilen, ob die Quelle einen Ausschneiden oder eine Kopie durchgeführt hat. Mit einem Drag & Drop-Vorgang können Sie CFSTR_PREFERREDDROPFORMAT verwenden, um die Aktion der Shell anzugeben. Wenn dieses Format nicht vorhanden ist, führt die Shell basierend auf dem Kontext eine Standardaktion aus. Wenn ein Benutzer beispielsweise eine Datei von einem Volume zieht und auf einem anderen Volume löscht, wird die Datei mit der Standardaktion der Shell kopiert. Wenn Sie ein CFSTR_PREFERREDDROPFORMAT Format in das Datenobjekt einschließen, können Sie die Standardaktion überschreiben und die Shell explizit anweisen, die Datei zu kopieren, zu verschieben oder zu verknüpfen. Wenn der Benutzer das Ziehen mit der rechten Schaltfläche auswählt, CFSTR_PREFERREDDROPFORMAT den Standardbefehl im [Drag](context-menu-handlers.md) & amp; Drop-Kontextmenü angibt. Der Benutzer kann weiterhin andere Befehle im Menü auswählen.

Vor Microsoft Internet Explorer 4,0 hat eine Anwendung angegeben, dass Verknüpfungs Dateitypen übertragen wurden, indem FD_LINKUI im **dwFlags** -Member der [**Filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) -Struktur festgelegt wurde. Ziele mussten dann einen potenziell zeitaufwändigen Aufruf von [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) verwenden, um herauszufinden, ob das FD_LINKUI-Flag festgelegt wurde. Die bevorzugte Methode, um anzugeben, dass Verknüpfungen übertragen werden, besteht darin, das CFSTR_PREFERREDDROPEFFECT Format zu verwenden, das auf DROPEFFECT_LINK festgelegt ist. Aus Gründen der Abwärtskompatibilität mit älteren Systemen sollten Quellen jedoch weiterhin das FD_LINKUI-Flag festlegen.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Dieser Format Bezeichner wird von einem Ziel verwendet, um die zugehörige CLSID für die Quelle bereitzustellen. Bei den Daten handelt es sich um eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf die CLSID-GUID des Ablage Ziels.

Dieses Format wird hauptsächlich verwendet, um zuzulassen, dass Objekte gelöscht werden, indem Sie Sie in den Papierkorb ziehen. Wenn ein Objekt im Papierkorb abgelegt wird, wird die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode der Quelle mit einem CFSTR_TARGETCLSID-Format aufgerufen, das auf die CLSID des Papierkorbs (CLSID_RecycleBin) festgelegt ist. Die Quelle kann dann das ursprüngliche Objekt löschen.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Dieser Format Bezeichner wird von Windows Internet Explorer und der Windows-Shell verwendet, um einen Mechanismus bereitzustellen, mit dem Drag & Drop-Vorgänge, die aus Internet Explorer stammen, in Verbindung mit dem [**URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) -Flag blockiert werden.

**CFSTR_UNTRUSTEDDRAGDROP** wird von der Quelle eines Drag & Drop-Vorgangs hinzugefügt, um anzugeben, dass das Datenobjekt möglicherweise nicht vertrauenswürdige Daten enthält. Die Daten werden durch eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur dargestellt, die ein globales Speicher Objekt enthält. Der **HGLOBAL** -Member der Struktur verweist auf ein **DWORD** , das auf ein entsprechendes [**URL-Aktionsflag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) festgelegt ist, um eine Richtlinien Überprüfung durch die [**iinternetsecuritymanager::P rocess UrlAction**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) -Methode zu bewirken, wobei das [**PUAF_ENFORCERESTRICTED**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85)) -Flag verwendet wird.

### <a name="dragwindow"></a>Dragwindow

Dieses Format wird in einem Drag & Drop-Vorgang verwendet, um das Zieh Bild (Fenster) eines Objekts zu identifizieren, sodass seine visuellen Informationen dynamisch aktualisiert werden können. Wenn ein Objekt über ein Ablage Ziel gezogen wird, aktualisiert eine Anwendung Ihre [**dropdescription**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) -Struktur in Reaktion auf die [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) -oder [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) -Methode. Die **dropdescription** wird mit einem neuen [**dropimagetype**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) -Wert aktualisiert, der die Dekoration angibt, die auf das visuelle Element des Zieh Fensters angewendet werden soll. beispielsweise ein Hinweis darauf, dass die Datei kopiert wird, anstatt verschoben zu werden, oder dass das Objekt an diesem Speicherort nicht gelöscht werden kann. Bis das Objekt jedoch eine [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) Nachricht empfängt, werden die visuellen Elemente nicht aktualisiert. Dieses Format gibt das **HWND** des Empfänger Zieh Fensters an den Absender der **DDWM_UPDATEWINDOW** Nachricht an.

Die Zwischenablage Daten sind vom Typ [**TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed). Dabei handelt es sich um eine **DWORD** -Darstellung eines **HWND**. Die Daten können an die **ulongtohandle** -Funktion, die in basetsd. h definiert ist, weitergegeben werden, um ein 64-Bit- **HWND** zur Verwendung auf 64-Bit-Fenstern bereitzustellen.

Für dieses Format ist die Einbindung von "shlobj. h" nicht erforderlich.

 

 
