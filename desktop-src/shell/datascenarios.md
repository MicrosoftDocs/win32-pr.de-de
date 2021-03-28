---
description: In diesem Dokument werden gängige Szenarios für die Shell-Datenübertragung vorgestellt und erläutert, wie Sie in Ihrer Anwendung implementiert werden.
ms.assetid: 7fce555c-a93d-4414-9119-7ae9acdd4d89
title: Behandeln von Shelldatenübertragungs-Szenarien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35855b66e4108580d5bac305855837563ca59785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977313"
---
# <a name="handling-shell-data-transfer-scenarios"></a>Behandeln von Shelldatenübertragungs-Szenarien

Das [shelldatenobjektdokument](dataobject.md) erläutert den allgemeinen Ansatz, der zum Übertragen von shelldaten mit Drag & Drop oder der Zwischenablage verwendet wird. Zum Implementieren von shelldatenübertragungen in Ihrer Anwendung müssen Sie jedoch auch verstehen, wie Sie diese allgemeinen Prinzipien und Techniken auf die Vielzahl von Methoden anwenden können, mit denen shelldaten übertragen werden können. In diesem Dokument werden gängige Szenarios für die Shell-Datenübertragung vorgestellt und erläutert, wie Sie in Ihrer Anwendung implementiert werden.

-   [Allgemeine Richtlinien](#general-guidelines)
-   [Kopieren von Dateinamen aus der Zwischenablage in eine Anwendung](#copying-file-names-from-the-clipboard-to-an-application)
    -   [Extrahieren der Dateinamen aus dem Datenobjekt](#extracting-the-file-names-from-the-data-object)
-   [Kopieren des Inhalts einer gelöschten Datei in eine Anwendung](#copying-the-contents-of-a-dropped-file-into-an-application)
    -   [Verwenden des cfstr \_ File Contents-Formats zum Extrahieren von Daten aus einer Datei](/windows)
-   [Verarbeiten optimierter Verschiebungs Vorgänge](#handling-optimized-move-operations)
-   [Behandeln von Lösch Vorgängen](#handling-delete-on-paste-operations)
-   [Übertragen von Daten in und aus virtuellen Ordnern](#transfering-data-to-and-from-virtual-folders)
    -   [Akzeptieren von Daten aus einem virtuellen Ordner](#accepting-data-from-a-virtual-folder)
    -   [Übertragen von Daten in eine und aus einer Namespace Erweiterung](#transferring-data-to-and-from-a-namespace-extension)
-   [Löschen von Dateien im Papierkorb](#dropping-files-on-the-recycle-bin)
-   [Erstellen und Importieren von Schrott Dateien](#creating-and-importing-scrap-files)
    -   [Roundtrip-Unterstützung](#round-trip-support)
    -   [Zwischengespeicherte Datenformate](#cached-data-formats)
    -   [Verzögertes Rendering](#delayed-rendering)
-   [Asynchrones ziehen und Ablegen von shellobjekten](#dragging-and-dropping-shell-objects-asynchronously)
    -   [Verwenden von iasyncoperation/idataobjectasynccapability](#using-iasyncoperationidataobjectasynccapability)

> [!Note]  
> Obwohl in jedem dieser Szenarien eine bestimmte Datenübertragungs Operation erläutert wird, gelten viele davon für eine Reihe von verwandten Szenarios. Der primäre Unterschied zwischen den meisten Zwischenablage-und Drag & Drop-Übertragungen ist beispielsweise die Art und Weise, in der das Datenobjekt beim Ziel ankommt. Wenn das Ziel über einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts verfügt, sind die Verfahren zum Extrahieren von Informationen größtenteils identisch für beide Daten Übertragungs Typen. Einige der Szenarien sind jedoch auf eine bestimmte Art von Vorgang beschränkt. Ausführliche Informationen finden Sie in den einzelnen Szenarios.

 

## <a name="general-guidelines"></a>Allgemeine Richtlinien

In den folgenden Abschnitten wird ein einzelnes, relativ spezifisches Datenübertragungs Szenario erläutert. Allerdings sind Datenübertragungen oft komplexer und können Aspekte mehrerer Szenarien beinhalten. In der Regel wissen Sie im Voraus nicht, welches Szenario Sie tatsächlich behandeln müssen. Im folgenden finden Sie einige allgemeine Richtlinien, die Sie berücksichtigen sollten.

Für Datenquellen:

-   Die shellzwischenablage Formate mit Ausnahme von [CF \_ HDROP](clipboard.md)sind nicht vordefiniert. Jedes Format, das Sie verwenden möchten, muss durch Aufrufen von [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)registriert werden.
-   Die Formate in den Datenobjekten werden in der von der Quelle bevorzugten Reihenfolge bereitgestellt. Zählen Sie das Datenobjekt auf, und wählen Sie das erste aus, das Sie verwenden können.
-   Schließen Sie beliebig viele Formate ein, die Sie unterstützen können. Im allgemeinen wissen Sie nicht, wo das Datenobjekt gelöscht wird. Diese Vorgehensweise verbessert die Wahrscheinlichkeit, dass das Datenobjekt ein Format enthält, das das Ablage Ziel annehmen kann.
-   Vorhandene Dateien sollten im [CF- \_ HDROP](clipboard.md) -Format angeboten werden.
-   Stellen Sie Datei ähnliche Daten mit [cfstr file \_ Content](clipboard.md) / [cfstr \_ Filedescriptor](clipboard.md) -Formaten zur Verfügung. Diese Vorgehensweise ermöglicht es dem Ziel, eine Datei aus einem Datenobjekt zu erstellen, ohne dass Informationen über den zugrunde liegenden Datenspeicher benötigt werden. Normalerweise sollten Sie die Daten als [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle darstellen. Dieser Datenübertragungsmechanismus ist flexibler als ein globales Speicher Objekt und beansprucht viel weniger Arbeitsspeicher.
-   Drag sources sollte beim Ziehen von shellelementen das Format [cfstr \_ shellidlist](clipboard.md) bieten. Datenobjekte für Elemente können entweder über die [**IShellFolder:: getuiobjectof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) -Methode oder die [**IShellItem:: bindtohandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) -Methode abgerufen werden. Datenquellen können eine standardmäßige Datenobjekt Implementierung erstellen, die das Format [cfstr \_ shellidlist](clipboard.md) mithilfe von [**shkreatedataobject**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject)unterstützt.
-   Ablage Ziele, die die Elemente, die mit dem shellelement-Programmiermodell gezogen werden, als Grund für Elemente verwenden möchten, können ein IDataObject mithilfe von [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)in ein [**ishellitemarray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) konvertieren.
-   Standard-Feedback Cursor verwenden.
-   Unterstützung von left und Right Drag.
-   Verwenden Sie das Datenobjekt selbst aus einem eingebetteten Objekt. Diese Vorgehensweise ermöglicht es Ihrer Anwendung, beliebige zusätzliche Formate abzurufen, die das Datenobjekt bereitstellen muss, und vermeidet eine zusätzliche Ebene der Kapselung. Beispielsweise wird ein eingebettetes Objekt von Server a aus Server/Container B gezogen und für den Container C gelöscht. c sollte ein eingebettetes Objekt von Server a erstellen, kein eingebettetes Objekt von Server B, das ein eingebettetes Objekt von Server a enthält.
-   Beachten Sie, dass die Shell beim Verschieben von Dateien [optimierte](#handling-optimized-move-operations) Verschiebe [-oder Lösch](#handling-delete-on-paste-operations) Vorgänge verwenden kann. Die Anwendung sollte diese Vorgänge erkennen und entsprechend reagieren können.

Für Datenziele:

-   Die shellzwischenablage Formate mit Ausnahme von [CF \_ HDROP](clipboard.md)sind nicht vordefiniert. Jedes Format, das Sie verwenden möchten, muss durch Aufrufen von [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)registriert werden.
-   Implementieren und Registrieren eines OLE Drop-Ziels. Vermeiden Sie nach Möglichkeit die Verwendung von Windows 3,1-Zielen oder der [**WM- \_ dropfiles**](wm-dropfiles.md) -Nachricht.
-   Die Formate, die in einem Datenobjekt enthalten sind, variieren in Abhängigkeit davon, woher das Objekt stammt. Da Sie im Allgemeinen nicht wissen, wo ein Datenobjekt stammt, gehen Sie nicht davon aus, dass ein bestimmtes Format vorhanden ist. Das Datenobjekt sollte die Formate in der Reihenfolge der Qualität auflisten, beginnend mit dem besten. Um also das beste verfügbare Format zu erhalten, zählen Anwendungen normalerweise zu den verfügbaren Formaten und verwenden das erste Format in der Enumeration, das Sie unterstützen können.
-   Unterstützung für den rechten Zieh Vorgang. Sie können das Kontextmenü des Zieh Vorgangs anpassen, indem Sie einen [Drag & Drop-Handler](context-menu-handlers.md)erstellen.
-   Wenn Ihre Anwendung vorhandene Dateien annimmt, muss Sie in der Lage sein, das [CF- \_ HDROP](clipboard.md) -Format zu verarbeiten.
-   Im Allgemeinen sollten Anwendungen, die Dateien akzeptieren, auch die cfstr [ \_ FileContent](clipboard.md)- / [ \_ Filedescriptor](clipboard.md) -Formate verarbeiten. Obwohl Dateien aus dem Dateisystem das [CF- \_ HDROP](clipboard.md) -Format aufweisen, verwenden Dateien von Anbietern, wie z. b. Namespace Erweiterungen, in der Regel [cfstr \_ FileContent](clipboard.md) / [cfstr \_ Filedescriptor](clipboard.md). Beispiele hierfür sind Windows CE Ordner, File Transfer Protocol (FTP)-Ordner, Webordner und CAB-Ordner. Die Quelle implementiert normalerweise eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle, um Daten aus Ihrem Speicher als Datei darzustellen.
-   Beachten Sie, dass die Shell beim Verschieben von Dateien [optimierte](#handling-optimized-move-operations) Verschiebe [-oder Lösch](#handling-delete-on-paste-operations) Vorgänge verwenden kann. Die Anwendung sollte diese Vorgänge erkennen und entsprechend reagieren können.

## <a name="copying-file-names-from-the-clipboard-to-an-application"></a>Kopieren von Dateinamen aus der Zwischenablage in eine Anwendung

**Szenario:** Ein Benutzer wählt eine oder mehrere Dateien im Windows-Explorer aus und kopiert sie in die Zwischenablage. Die Anwendung extrahiert die Dateinamen und fügt Sie in das Dokument ein.

Dieses Szenario könnte beispielsweise verwendet werden, um es einem Benutzer zu ermöglichen, einen HTML-Link zu erstellen, indem Sie die Datei Ausschnitten und in Ihre Anwendung einfügen. Die Anwendung kann dann den Dateinamen aus dem Datenobjekt extrahieren und verarbeiten, um ein Anchor-Tag zu erstellen.

Wenn ein Benutzer eine Datei in Windows-Explorer auswählt und in die Zwischenablage kopiert, erstellt die Shell ein Datenobjekt. Anschließend wird [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) aufgerufen, um einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts in der Zwischenablage zu platzieren.

Wenn der Benutzer den Befehl **Einfügen** aus dem Menü oder der Symbolleiste Ihrer Anwendung auswählt:

1.  Rufen Sie [**olegetclipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) auf, um die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts abzurufen.
2.  Rufen Sie [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) auf, um ein Enumeratorobjekt anzufordern.
3.  Verwenden Sie die [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) -Schnittstelle des Enumeratorobjekts, um die Formate aufzulisten, die im Datenobjekt enthalten sind.

> [!Note]  
> Die letzten beiden Schritte in diesem Verfahren sind aus Gründen der Vollständigkeit enthalten. Sie sind in der Regel für einfache Dateiübertragungen nicht erforderlich. Alle Datenobjekte, die für diesen Datentyp verwendet werden, sollten das [CF- \_ HDROP](clipboard.md) -Format enthalten, das verwendet werden kann, um die Namen der Dateien zu bestimmen, die im Objekt enthalten sind. Bei allgemeineren Datenübertragungen sollten Sie jedoch die Formate auflisten und das beste auswählen, das von Ihrer Anwendung verarbeitet werden kann.

 

### <a name="extracting-the-file-names-from-the-data-object"></a>Extrahieren der Dateinamen aus dem Datenobjekt

Der nächste Schritt besteht darin, einen oder mehrere Dateinamen aus dem Datenobjekt zu extrahieren und in Ihre Anwendung einzufügen. Beachten Sie, dass das in diesem Abschnitt beschriebene Verfahren zum Extrahieren eines Datei namens aus einem Datenobjekt auch für Drag & Drop-Übertragungen gilt.

Die einfachste Methode zum Abrufen von Dateinamen aus einem Datenobjekt ist das [CF- \_ HDROP](clipboard.md) -Format:

1.  Aufrufen von [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Legen Sie **den cfFormat** -Member [**der FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur auf [CF \_ HDROP](clipboard.md) und den **TYMED** -Member auf [TYMED \_ HGLOBAL](dataobject.md)fest. Der **dwAspect** -Member ist normalerweise auf den dvaspesinhalt festgelegt \_ . Wenn Sie jedoch den Pfad der Datei im kurzen Format (8,3) benötigen, legen Sie **dwAspect** auf dvaspekt Short fest \_ .

    Wenn [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) zurückgibt, verweist der **HGLOBAL** -Member der [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur auf ein globales Speicher Objekt, das die Daten enthält.

2.  Erstellen Sie eine HDROP-Variable, und legen Sie Sie auf den **HGLOBAL** -Member der [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur fest. Die HDROP-Variable ist nun ein Handle für eine [**dropfiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) -Struktur, auf die eine Double-NULL-terminierte Zeichenfolge mit den voll qualifizierten Dateipfaden der kopierten Dateien folgt.
3.  Bestimmen Sie, wie viele Dateipfade in der Liste aufgeführt sind, indem Sie [**dragqueryfile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) aufrufen, wobei der *ifile* -Parameter auf 0xFFFFFFFF festgelegt ist. Die-Funktion gibt die Anzahl der Dateipfade in der Liste zurück. Der null basierte Index des Dateipfads in dieser Liste wird im nächsten Schritt verwendet, um einen bestimmten Pfad zu identifizieren.
4.  Extrahieren Sie die Dateipfade aus dem globalen Speicher Objekt, indem Sie [**dragqueryfile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) einmal für jede Datei aufrufen, wobei *ifile* auf den Index der Datei festgelegt ist.
5.  Verarbeiten Sie die Dateipfade nach Bedarf, und fügen Sie Sie in Ihre Anwendung ein.
6.  Aufrufen von [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) und übergeben des Zeigers an die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die Sie in Schritt 1 an [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) übergeben haben. Nachdem Sie die Struktur freigegeben haben, ist der HDROP-Wert, den Sie in Schritt 2 erstellt haben, nicht mehr gültig und sollte nicht verwendet werden.

## <a name="copying-the-contents-of-a-dropped-file-into-an-application"></a>Kopieren des Inhalts einer gelöschten Datei in eine Anwendung

**Szenario:** Ein Benutzer zieht eine oder mehrere Dateien aus Windows-Explorer und löscht Sie im Fenster Ihrer Anwendung. Die Anwendung extrahiert den Inhalt der Datei (en) und fügt Sie in die Anwendung ein.

In diesem Szenario werden Drag & Drop verwendet, um die Dateien aus Windows-Explorer in die Anwendung zu übertragen. Vor dem-Vorgang muss Ihre Anwendung folgende Aktionen ausführen:

1.  Wenden Sie [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) an, um alle benötigten shellzwischenablage Formate zu registrieren.
2.  Wenden Sie [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) an, um ein Zielfenster und die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle Ihrer Anwendung zu registrieren.

Nachdem der Benutzer den Vorgang initiiert hat, wählen Sie eine oder mehrere Dateien aus, und ziehen Sie die folgenden Schritte:

1.  Windows-Explorer erstellt ein Datenobjekt und lädt die unterstützten Formate in dieses Objekt.
2.  Windows-Explorer ruft [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) auf, um die Drag-Schleife zu initiieren.
3.  Wenn das Zieh Bild das Zielfenster erreicht, benachrichtigt das System Sie durch Aufrufen von [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).
4.  Um zu ermitteln, was das Datenobjekt enthält, rufen Sie die [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) -Methode des Datenobjekts auf. Verwenden Sie das von der-Methode zurückgegebene Enumeratorobjekt, um die Formate aufzulisten, die im Datenobjekt enthalten sind. Wenn die Anwendung keines dieser Formate akzeptieren soll, geben Sie dropffect \_ None zurück. Im Rahmen dieses Szenarios sollte Ihre Anwendung alle Datenobjekte ignorieren, die keine Formate enthalten, die zum Übertragen von Dateien verwendet werden, wie z. b. [CF \_ HDROP](clipboard.md).
5.  Wenn der Benutzer die Daten löscht, ruft das System [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)auf.
6.  Verwenden Sie die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle, um den Inhalt der Dateien zu extrahieren.

Es gibt verschiedene Möglichkeiten, den Inhalt eines shellobjekts aus einem Datenobjekt zu extrahieren. Verwenden Sie in der Regel die folgende Reihenfolge:

-   Wenn die Datei ein [CF- \_ Text](clipboard.md) Format enthält, sind die Daten ANSI-Text. Sie können das CF- \_ Text Format verwenden, um die Daten zu extrahieren, anstatt die Datei selbst zu öffnen.
-   Wenn die Datei ein verknüpftes oder eingebettetes OLE-Objekt enthält, enthält das Datenobjekt ein CF- \_ embeddedObject-Format. Verwenden Sie OLE-Standardtechniken, um die Daten zu extrahieren. [Schrott Dateien](#creating-and-importing-scrap-files) enthalten immer ein CF \_ embeddedObject-Format.
-   Wenn das Shellobjekt aus dem Dateisystem besteht, enthält das Datenobjekt ein [CF- \_ HDROP](clipboard.md) -Format mit den Namen der Dateien. Extrahieren Sie den Dateinamen aus [CF \_ HDROP](clipboard.md) , und rufen Sie [**olecreatefromfile**](/windows/win32/api/ole2/nf-ole2-olecreatefromfile) auf, um ein neues verknüpftes oder eingebettetes Objekt zu erstellen. Eine Erläuterung dazu, wie Sie einen Dateinamen aus einem [CF- \_ HDROP](clipboard.md) -Format abrufen, finden Sie unter [Kopieren von Dateinamen aus der Zwischenablage in eine Anwendung](#copying-file-names-from-the-clipboard-to-an-application).
-   Wenn das Datenobjekt ein [cfstr \_ File Descriptor](clipboard.md) -Format enthält, können Sie den Inhalt einer Datei aus dem Format " [cfstr \_ fileContents](clipboard.md) " der Datei extrahieren. Eine Erläuterung dieses Verfahrens finden [Sie unter Verwenden des cfstr \_ File Contents-Formats zum Extrahieren von Daten aus einer Datei](/windows).
-   Vor der Shell- [Version 4,71](versions.md)hat eine Anwendung angegeben, dass Sie einen Verknüpfungs Dateityp übertragen hat, indem Sie **FD \_ linkui** im **dwFlags** -Member der [**Filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) -Struktur festgelegt hat. Für spätere Versionen der Shell ist die bevorzugte Methode, um anzugeben, dass Verknüpfungen übertragen werden, das Format " [cfstr \_ preferreddropeffect](clipboard.md) ", das auf den Link "DropEffect" festgelegt ist \_ . Diese Vorgehensweise ist viel effizienter als das Extrahieren der **Filedescriptor** -Struktur, nur um ein Flag zu überprüfen.

Wenn der Daten Extraktionsprozess langwierig ist, sollten Sie den Vorgang in einem Hintergrund Thread asynchron ausführen. Der primäre Thread kann dann ohne unnötige Verzögerungen fortfahren. Eine Erläuterung zum Verarbeiten der asynchronen Datenextraktion finden Sie unter [asynchrones ziehen und Ablegen von shellobjekten](#dragging-and-dropping-shell-objects-asynchronously).

### <a name="using-the-cfstr_filecontents-format-to-extract-data-from-a-file"></a>Verwenden des cfstr \_ File Contents-Formats zum Extrahieren von Daten aus einer Datei

Das Format [cfstr \_ fileContents](clipboard.md) bietet eine sehr flexible und leistungsstarke Möglichkeit, den Inhalt einer Datei zu übertragen. Es ist nicht einmal erforderlich, dass die Daten als einzelne Datei gespeichert werden. Für dieses Format ist lediglich erforderlich, dass das Datenobjekt die Daten für das Ziel wie eine-Datei präsentiert. Beispielsweise kann es sich bei den eigentlichen Daten um einen Abschnitt eines Textdokuments oder um einen Datenblock handeln, der aus einer Datenbank extrahiert wird. Das Ziel kann die Daten als Datei behandeln und muss nichts über den zugrunde liegenden Speichermechanismus wissen.

Namespace Erweiterungen verwenden normalerweise [cfstr \_ File Content](clipboard.md) , um Daten zu übertragen, da dieses Format keinen bestimmten Speichermechanismus annimmt. Eine Namespace Erweiterung kann einen beliebigen Speichermechanismus verwenden und dieses Format verwenden, um die Objekte den Anwendungen so darzustellen, als wären Sie Dateien.

Der Datenübertragungsmechanismus für [cfstr \_ FileContent](clipboard.md) ist normalerweise [TYMED \_ IStream](dataobject.md). Das übertragen eines [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstellen Zeigers erfordert viel weniger Arbeitsspeicher als das Laden der Daten in ein globales Speicher Objekt, und **IStream** ist eine einfachere Möglichkeit, um Daten darzustellen als [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage).

Ein [cfstr \_ File Contents](clipboard.md) -Format wird immer von einem [cfstr- \_ Filedescriptor](clipboard.md) -Format begleitet. Sie müssen den Inhalt dieses Formats zuerst überprüfen. Wenn mehr als eine Datei übertragen wird, enthält das Datenobjekt tatsächlich mehrere [cfstr \_ File Content](clipboard.md) -Formate, eine für jede Datei. Das Format [cfstr \_ Filedescriptor](clipboard.md) enthält den Namen und die Attribute der einzelnen Dateien und stellt einen Indexwert für jede Datei bereit, die erforderlich ist, um das [cfstr \_ File Contents](clipboard.md) -Format einer bestimmten Datei zu extrahieren.

So extrahieren Sie ein [cfstr \_ File Contents](clipboard.md) -Format:

1.  Extrahieren Sie das Format " [cfstr \_ Filedescriptor](clipboard.md) " als Wert für " [TYMED \_ HGLOBAL](dataobject.md) ".
2.  Der **HGLOBAL** -Member der zurückgegebenen [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur verweist auf ein globales Speicher Objekt. Sperren Sie das Objekt, indem Sie den **HGLOBAL** -Wert an [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock)übergeben.
3.  Wandeln Sie den von [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) zurückgegebenen Zeiger in einen [**filegroupdescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) -Zeiger um. Er verweist auf eine **filegroupdescriptor** -Struktur, auf die mindestens eine [**Filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) -Struktur folgt. Jede **Filedescriptor** -Struktur enthält eine Beschreibung einer Datei, die in einem der zugehörigen [cfstr \_ File Content](clipboard.md) -Formate enthalten ist.
4.  Überprüfen Sie die [**Filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) -Strukturen, um zu bestimmen, welcher der Datei entspricht, die Sie extrahieren möchten. Der null basierte Index dieser **Filedescriptor** -Struktur wird verwendet, um das Format der Datei " [cfstr \_ fileContents](clipboard.md) " der Datei zu identifizieren. Da die Größe eines globalen Speicherblocks nicht Byte genau ist, verwenden Sie die Member **nfilesizelow** und **nfilesizehigh** der Struktur, um zu bestimmen, wie viele Bytes die Datei im globalen Speicher Objekt darstellen.
5.  Rufen Sie [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) auf, wobei der **cfFormat** -Member der [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur auf den Wert [cfstr \_ fileContents](clipboard.md) festgelegt ist und der **Lindex** -Member auf den Index festgelegt ist, den Sie im vorherigen Schritt festgelegt haben. Der **TYMED** -Member ist in der Regel auf " [TYMED \_ HGLOBAL](dataobject.md) \| TYMED \_ IStream \| TYMED IStorage" festgelegt \_ . Das Datenobjekt kann dann seinen bevorzugten Datenübertragungsmechanismus auswählen.
6.  Die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur, die [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) zurückgibt, enthält einen Zeiger auf die Daten der Datei. Überprüfen Sie den **TYMED** -Member der-Struktur, um den Datenübertragungsmechanismus zu bestimmen.
7.  Wenn **TYMED** auf " [TYMED \_ IStream](dataobject.md) " oder "TYMED IStorage" festgelegt ist \_ , verwenden Sie die-Schnittstelle zum Extrahieren der Daten. Wenn **TYMED** auf TYMED HGLOBAL festgelegt ist \_ , sind die Daten in einem globalen Speicher Objekt enthalten. Eine Erläuterung zum Extrahieren von Daten aus einem globalen Speicher Objekt finden Sie im Abschnitt *Extrahieren eines globalen Speicher Objekts aus einem Datenobjekt* des Shell- [Datenobjekts](dataobject.md).
8.  Zum Entsperren des globalen Speicher Objekts, das Sie in Schritt 2 gesperrt haben, wird [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) aufgerufen.

## <a name="handling-optimized-move-operations"></a>Verarbeiten optimierter Verschiebungs Vorgänge

**Szenario:** Eine Datei wird mithilfe einer optimierten Verschiebung aus dem Dateisystem in eine Namespace Erweiterung verschoben.

Bei einem herkömmlichen Verschiebungs Vorgang erstellt das Ziel eine Kopie der Daten, und die Quelle löscht das Original. Diese Vorgehensweise kann ineffizient sein, da zwei Kopien der Daten erforderlich sind. Bei großen Objekten, z. b. Datenbanken, ist ein herkömmlicher Verschiebungs Vorgang möglicherweise nicht einmal praktikabel.

Bei einem optimierten Verschiebe Vorgang verwendet das Ziel das Verständnis, wie die Daten gespeichert werden, um den gesamten Verschiebungs Vorgang zu verarbeiten. Es gibt nie eine zweite Kopie der Daten, und die Quelle muss die ursprünglichen Daten nicht löschen. Shelldaten sind gut für optimierte Verschiebungen geeignet, da das Ziel den gesamten Vorgang mithilfe der Shell-API verarbeiten kann. Ein typisches Beispiel ist das Verschieben von Dateien. Wenn das Ziel den Pfad einer Datei aufweist, die verschoben werden soll, kann es [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) verwenden, um es zu verschieben. Es ist nicht erforderlich, dass die Quelle die ursprüngliche Datei löscht.

> [!Note]  
> Die Shell verwendet normalerweise eine optimierte Verschiebung, um Dateien zu verschieben. Zum ordnungsgemäßen verarbeiten von shelldatenübertragungen muss Ihre Anwendung in der Lage sein, eine optimierte Verschiebung zu erkennen und zu verarbeiten.

 

Optimierte Verschiebungen werden wie folgt behandelt:

1.  Die Quelle ruft [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) auf, wobei der *dweffect* -Parameter auf dropeer ffect Move festgelegt \_ ist, um anzugeben, dass die Quell Objekte verschoben werden können.
2.  Das Ziel empfängt den dropeer ffect-Verschiebungs \_ Wert über eine seiner [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Methoden, was darauf hinweist, dass eine Verschiebung zulässig ist.
3.  Das Ziel kopiert entweder das Objekt (nicht optimierte Verschiebung) oder verschiebt das Objekt (optimierte Verschiebung).
4.  Das Ziel teilt der Quelle dann mit, ob die ursprünglichen Daten gelöscht werden müssen.

    Eine optimierte Verschiebung ist der Standard Vorgang, bei dem die Daten vom Ziel gelöscht werden. So informieren Sie die Quelle, dass eine optimierte Verschiebung durchgeführt wurde:

    -   -   Das Ziel legt den Wert von *pdweffect* , der über seine [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Methode empfangen wurde, auf einen anderen Wert als dropeer ffect \_ Move fest. Er ist in der Regel auf "dropeer ffect \_ None" oder "dropeer" Kopieren festgelegt \_ . Der Wert wird von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)an die Quelle zurückgegeben.
        -   Das Ziel ruft außerdem die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode des Datenobjekts auf und übergibt ihm einen auf dropeer ffect None festgelegten [cfstr \_ performeddropeer ffect](clipboard.md) -Format Bezeichner \_ . Dieser Methoden Aufrufwert ist erforderlich, da einige Ablage Ziele den Parameter " *pdweffect* " von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) möglicherweise nicht ordnungsgemäß festlegen. Das [cfstr \_ performeddropeer ffect](clipboard.md) -Format ist die zuverlässige Möglichkeit, um anzugeben, dass eine optimierte Verschiebung stattfindet.

    Wenn das Ziel eine nicht optimierte Verschiebung durchgeführt hat, müssen die Daten von der Quelle gelöscht werden. So informieren Sie die Quelle, dass eine nicht optimierte Verschiebung durchgeführt wurde:

    -   -   Das Ziel legt den Wert von *pdweffect* fest, den er über seine [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Methode empfangen hat, auf dropffect \_ Move. Der Wert wird von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)an die Quelle zurückgegeben.
        -   Das Ziel ruft außerdem die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode des Datenobjekts auf und übergibt ihm einen auf dropffect-Verschiebungs Satz festgelegten [cfstr \_ performeddropeer ffect](clipboard.md) -Format Bezeichner \_ . Dieser Methoden Aufrufwert ist erforderlich, da einige Ablage Ziele den Parameter " *pdweffect* " von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) möglicherweise nicht ordnungsgemäß festlegen. Das [cfstr \_ performeddropeer ffect](clipboard.md) -Format ist die zuverlässige Möglichkeit, um anzugeben, dass eine nicht optimierte Verschiebung stattfindet.

5.  Die Quelle überprüft die beiden Werte, die vom Ziel zurückgegeben werden können. Wenn beide auf dropffect Move festgelegt sind \_ , wird die nicht optimierte Verschiebung durch Löschen der ursprünglichen Daten abgeschlossen. Andernfalls hat das Ziel eine optimierte Verschiebung durchgeführt, und die ursprünglichen Daten wurden gelöscht.

## <a name="handling-delete-on-paste-operations"></a>Behandeln von Lösch Vorgängen

**Szenario:** Mindestens eine Datei wird aus einem Ordner in Windows-Explorer ausgeschnitten und in eine Namespace Erweiterung eingefügt. In Windows-Explorer bleiben die Dateien hervorgehoben, bis Sie Feedback zum Ergebnis des Einfügevorgangs erhalten.

Wenn ein Benutzer in der Regel Daten schneidet, verschwindet er sofort aus der Ansicht. Dies ist möglicherweise nicht effizient und kann zu Problemen mit der Benutzerfreundlichkeit führen, wenn der Benutzer sich Gedanken darüber machen muss, was mit den Daten geschehen ist. Ein alternativer Ansatz ist die Verwendung eines DELETE-on-Paste-Vorgangs.

Bei einem DELETE-on-Copy-Vorgang werden die ausgewählten Daten nicht sofort aus der Ansicht entfernt. Stattdessen markiert die Quell Anwendung Sie als ausgewählt, möglicherweise durch Ändern der Schriftart oder der Hintergrundfarbe. Nachdem die Zielanwendung die Daten eingefügt hat, benachrichtigt Sie die Quelle über das Ergebnis des Vorgangs. Wenn das Ziel eine [optimierte Verschiebung](#handling-optimized-move-operations)durchgeführt hat, kann die Quelle die Anzeige einfach aktualisieren. Wenn das Ziel einen normalen Verschiebe Vorgang durchgeführt hat, muss die Quelle auch die Kopie der Daten löschen. Wenn beim Einfügen ein Fehler auftritt, stellt die Quell Anwendung die ausgewählten Daten in der ursprünglichen Darstellung wieder her.

> [!Note]  
> Die Shell verwendet normalerweise DELETE-on-Copy, wenn ein Ausschneide-/Einfügevorgang zum Verschieben von Dateien verwendet wird. Beim Einfügen von Lösch Vorgängen mit shellobjekten wird normalerweise eine [optimierte Verschiebung](#handling-optimized-move-operations) verwendet, um die Dateien zu verschieben. Damit die Shell-Datenübertragung ordnungsgemäß durchgeführt werden kann, muss Ihre Anwendung in der Lage sein, Vorgänge zum Löschen und einfügen zu erkennen und zu verarbeiten.

 

Die grundlegende Anforderung für DELETE-on-Paste besteht darin, dass das Ziel das Ergebnis des Vorgangs an die Quelle melden muss. Standardmäßige Zwischenablage Techniken können jedoch nicht zum Implementieren von DELETE-on-Paste verwendet werden, da Sie keine Möglichkeit bieten, mit der Quelle zu kommunizieren. Stattdessen verwendet die Zielanwendung die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode des Datenobjekts, um das Ergebnis an das Datenobjekt zu melden. Das Datenobjekt kann dann über eine private Schnittstelle mit der Quelle kommunizieren.

Das grundlegende Verfahren für eine DELETE-on-Paste-Operation lautet wie folgt:

1.  Die Quelle markiert die Bildschirm Anzeige der ausgewählten Daten.
2.  Die Quelle erstellt ein Datenobjekt. Dies weist auf einen Ausschneide Vorgang hin, indem das Format [cfstr \_ preferreddroetffect](clipboard.md) mit dem Datenwert dropffect Move hinzugefügt wird \_ .
3.  Die Quelle platziert das Datenobjekt mithilfe von [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard)in der Zwischenablage.
4.  Das Ziel Ruft das Datenobjekt mithilfe von [**olegetclipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)aus der Zwischenablage ab.
5.  Das Ziel extrahiert die [cfstr \_ preferreddropinffect](clipboard.md) -Daten. Wenn es nur auf dropffect Move festgelegt ist \_ , kann das Ziel entweder eine optimierte Verschiebung durchführen oder einfach die Daten kopieren.
6.  Wenn das Ziel keine optimierte Verschiebung durchführt, wird die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode aufgerufen, wobei das Format [cfstr \_ performeddropeer ffect](clipboard.md) auf dropeer ffect Move festgelegt ist \_ .
7.  Wenn das Einfügen abgeschlossen ist, ruft das Ziel die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode auf, wobei das Format [cfstr \_ pastesucc-](clipboard.md) Version auf dropeer ffect Move festgelegt ist \_ .
8.  Wenn die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode der Quelle mit dem auf dropffect verschieben festgelegten [cfstr- \_ pastesucc-](clipboard.md) Wert-Format aufgerufen wird \_ , muss überprüft werden, ob Sie auch das auf dropeer ffect Move festgelegte [cfstr \_ performeddropeer ffect](clipboard.md) -Format erhalten hat \_ . Wenn beide Formate vom Ziel gesendet werden, müssen die Daten von der Quelle gelöscht werden. Wenn nur das [cfstr- \_ pastesucc-](clipboard.md) Format empfangen wird, kann die Quelle einfach die Daten aus der Anzeige entfernen. Wenn bei der Übertragung ein Fehler auftritt, aktualisiert die Quelle die ursprüngliche Darstellung der Anzeige.

## <a name="transfering-data-to-and-from-virtual-folders"></a>Übertragen von Daten in und aus virtuellen Ordnern

**Szenario:** Ein Benutzer zieht ein Objekt aus oder löscht es in einem virtuellen Ordner.

Virtuelle Ordner enthalten Objekte, die im Allgemeinen nicht Teil des Dateisystems sind. Einige virtuelle Ordner, z. b. der Papierkorb, können Daten darstellen, die auf der Festplatte gespeichert sind, aber nicht als gewöhnliche Dateisystem Objekte. Einige können gespeicherte Daten darstellen, die sich auf einem Remote System befinden, z. b. ein Handheld-PC oder eine FTP-Site. Andere, wie z. b. der Ordner Drucker, enthalten Objekte, die keine gespeicherten Daten darstellen. Während einige virtuelle Ordner Teil des Systems sind, können Entwickler auch benutzerdefinierte virtuelle Ordner erstellen und installieren, indem Sie eine Namespace Erweiterung implementieren.

Unabhängig vom Datentyp oder der Art der Speicherung werden die Ordner-und Datei Objekte, die in einem virtuellen Ordner enthalten sind, von der Shell angezeigt, als wären Sie normale Dateien und Ordner. Es liegt in der Verantwortung des virtuellen Ordners, die darin enthaltenen Daten zu übernehmen und Sie der Shell entsprechend darzustellen. Diese Anforderung bedeutet, dass virtuelle Ordner normalerweise Drag & Drop-Datenübertragungen und Zwischenablage Daten übertragen.

Es gibt zwei Gruppen von Entwicklern, die sich mit der Datenübertragung zu und von virtuellen Ordnern befassen müssen:

-   Entwickler, deren Anwendungen Daten akzeptieren müssen, die von einem virtuellen Ordner übertragen werden.
-   Entwickler, deren Namespace Erweiterungen die Datenübertragung ordnungsgemäß unterstützen müssen.

### <a name="accepting-data-from-a-virtual-folder"></a>Akzeptieren von Daten aus einem virtuellen Ordner

Virtuelle Ordner können praktisch jeden Datentyp darstellen und können diese Daten in beliebiger Weise speichern. Einige virtuelle Ordner enthalten möglicherweise normale Dateisystem Dateien und-Ordner. Andere können beispielsweise alle Objekte in einem einzelnen Dokument oder in einer Datenbank packen.

Wenn ein Dateisystem Objekt an eine Anwendung übertragen wird, enthält das Datenobjekt normalerweise ein [CF- \_ HDROP](clipboard.md) -Format mit dem voll qualifizierten Pfad des Objekts. Die Anwendung kann diese Zeichenfolge extrahieren und die normalen Dateisystemfunktionen verwenden, um die Datei zu öffnen und die Daten zu extrahieren. Da virtuelle Ordner in der Regel jedoch keine normalen Dateisystem Objekte enthalten, verwenden Sie in der Regel nicht [CF \_ HDROP](clipboard.md).

Anstelle von [CF \_ HDROP](clipboard.md)werden Daten normalerweise aus virtuellen Ordnern mit den cfstr [ \_ Filedescriptor](clipboard.md)- / Formaten[cfstr \_ fileContents](clipboard.md) übertragen. Das Format " [cfstr \_ FileContent](clipboard.md) " hat gegenüber [CF \_ HDROP](clipboard.md)zwei Vorteile:

-   Es wird keine bestimmte Methode der Datenspeicherung angenommen.
-   Das Format ist flexibler. Es unterstützt drei Datenübertragungs Mechanismen: ein globales Speicher Objekt, eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle oder eine [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle.

Globale Speicher Objekte werden selten zum Übertragen von Daten in oder von virtuellen Objekten verwendet, da die Daten vollständig in den Arbeitsspeicher kopiert werden müssen. Die Übertragung eines Schnittstellen Zeigers erfordert fast keinen Arbeitsspeicher und ist viel effizienter. Bei sehr großen Dateien kann ein Schnittstellen Zeiger der einzige praktische Datenübertragungsmechanismus sein. Normalerweise werden Daten durch einen [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Zeiger dargestellt, da diese Schnittstelle etwas flexibler als [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage)ist. Das Ziel extrahiert den Zeiger aus dem Datenobjekt und verwendet die Schnittstellen Methoden, um die Daten zu extrahieren.

Weitere Informationen zur Handhabung der cfstr [ \_ Filedescriptor](clipboard.md)-Datei / [ \_ Inhalts](clipboard.md) Formate finden [Sie unter Verwenden des Datei \_ Inhalts Formats von cfstr zum Extrahieren von Daten aus einer Datei](/windows).

### <a name="transferring-data-to-and-from-a-namespace-extension"></a>Übertragen von Daten in eine und aus einer Namespace Erweiterung

Wenn Sie eine Namespace Erweiterung implementieren, werden Sie normalerweise Drag & Drop-Funktionen unterstützen. Befolgen Sie die Empfehlungen für Drop Sources und Targets, die unter [Allgemeine Richtlinien](#general-guidelines)erläutert werden. Insbesondere muss eine Namespace Erweiterung Folgendes ausführen:

-   Sie können die cfstr [ \_ Filedescriptor](clipboard.md) / [cfstr \_ FileContent](clipboard.md) -Formate verarbeiten. Diese beiden Formate werden normalerweise zum Übertragen von Objekten in und aus Namespace Erweiterungen verwendet.
-   Kann [optimierte](#handling-optimized-move-operations)Verschiebungen verarbeiten. Die Shell erwartet, dass Shellobjekte mit optimiertem Verschiebe Vorgang verschoben werden.
-   Kann einen [Lösch](#handling-delete-on-paste-operations) Vorgang verarbeiten. Die Shell verwendet DELETE-on-Copy, wenn Objekte mit einem Ausschneide-/Einfügevorgang aus der Shell verschoben werden.
-   Kann die Datenübertragung über eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -oder [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle verarbeiten. Die Datenübertragung zu oder von einem virtuellen Ordner erfolgt normalerweise durch Übertragung eines dieser beiden Schnittstellen Zeiger, in der Regel ein **IStream** -Zeiger. Das Ziel ruft dann die Schnittstellen Methoden auf, um die Daten zu extrahieren:
    -   -   Als Drop-Quelle muss die Namespace Erweiterung die Daten aus dem Speicher extrahieren und diese Schnittstelle an das Ziel übergeben.
        -   Als Drop-Ziel muss eine Namespace Erweiterung Daten von einer Quelle über diese Schnittstelle akzeptieren und ordnungsgemäß speichern.

## <a name="dropping-files-on-the-recycle-bin"></a>Löschen von Dateien im Papierkorb

**Szenario:** Der Benutzer löscht eine Datei im **Papierkorb**. Die ursprüngliche Datei wird von der Anwendung oder der Namespace Erweiterung gelöscht.

Der Papierkorb ist ein virtueller Ordner, der als Repository für Dateien verwendet wird, die nicht mehr benötigt werden. Solange der Papierkorb nicht geleert wurde, kann der Benutzer die Datei später wiederherstellen und an das Dateisystem zurückgeben.

Zum größten Teil funktioniert das Übertragen von shellobjekten in den Papierkorb ähnlich wie jeder andere Ordner. Wenn ein Benutzer jedoch eine Datei im **Papierkorb** löscht, muss die Quelle das Original löschen, auch wenn das Feedback aus dem Ordner einen Kopiervorgang angibt. Normalerweise kann eine Ablage Quelle nicht wissen, in welchem Ordner das Datenobjekt abgelegt wurde. Wenn jedoch für Windows 2000 und spätere Systeme ein Datenobjekt im **Papierkorb** abgelegt wird, ruft die Shell die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode des Datenobjekts mit einem [cfstr \_ targetclsid](clipboard.md) -Format auf, das auf den Klassen Bezeichner (CLSID) (CLSID) des Papierkorbs festgelegt ist \_ . Damit der Papierkorb ordnungsgemäß verarbeitet wird, sollte das Datenobjekt in der Lage sein, dieses Format zu erkennen und die Informationen über eine private Schnittstelle an die Quelle zu übermitteln.

> [!Note]  
> Wenn [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) mit dem Format " [cfstr \_ targetclsid](clipboard.md) " aufgerufen wird, das auf "CLSID RecycleBin" festgelegt ist \_ , sollte die Datenquelle alle geöffneten Handles für die Objekte schließen, die übertragen werden, bevor Sie von der Methode zurückgegeben werden. Andernfalls können Sie Freigabe Verletzungen erstellen.

 

## <a name="creating-and-importing-scrap-files"></a>Erstellen und Importieren von Schrott Dateien

**Szenario:** Ein Benutzer zieht einige Daten aus der Datendatei einer OLE-Anwendung und löscht Sie auf dem Desktop oder Windows-Explorer.

Mithilfe von Windows können Benutzer ein Objekt aus der Datendatei einer OLE-Anwendung ziehen und auf dem Desktop oder einem Dateisystem Ordner ablegen. Mit diesem Vorgang wird eine *Dumpdatei* erstellt, die die Daten oder einen Link zu den Daten enthält. Der Dateiname stammt aus dem Kurznamen, der für die CLSID des Objekts und den [CF- \_ Textdaten](clipboard.md) registriert ist. Damit die Shell eine Ablage Datei mit Daten erstellt, muss die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle der Anwendung das CF \_ embedsource-Zwischenablage Format unterstützen. Um eine Datei zu erstellen, die einen Link enthält, muss **IDataObject** das CF- \_ LinkSource-Format unterstützen.

Es gibt auch drei optionale Features, die eine Anwendung zur Unterstützung von Schrott Dateien implementieren kann:

-   Roundtrip-Unterstützung
-   Zwischengespeicherte Datenformate
-   Verzögertes Rendering

### <a name="round-trip-support"></a>Roundtrip-Unterstützung

Ein *Roundtrip* umfasst das übertragen eines Datenobjekts in einen anderen Container und dann zurück zum ursprünglichen Dokument. Beispielsweise kann ein Benutzer eine Gruppe von Zellen aus einer Kalkulations Tabelle auf den Desktop übertragen und dabei eine Dumpdatei mit den Daten erstellen. Wenn der Benutzer den Schrott dann wieder in die Kalkulations Tabelle überträgt, müssen die Daten in das Dokument integriert werden, so wie es vor der ursprünglichen Übertragung der Fall war.

Wenn die Shell die Schrott Datei erstellt, stellt Sie die Daten als Einbettungs Objekt dar. Wenn der Schrott an einen anderen Container übertragen wird, wird er als Einbettungs Objekt übertragen, auch wenn er an das ursprüngliche Dokument zurückgegeben wird. Ihre Anwendung ist dafür verantwortlich, das im Schrott enthaltene Datenformat zu ermitteln und die Daten bei Bedarf wieder in das systemeigene Format zu versetzen.

Um das Format des eingebetteten Objekts festzulegen, bestimmen Sie seine CLSID, indem Sie das CF \_ objectdescriptor-Format des Objekts abrufen. Wenn die CLSID ein Datenformat angibt, das der Anwendung angehört, sollte Sie die systemeigenen Daten übertragen, anstatt [**olecreatefromdata**](/windows/win32/api/ole2/nf-ole2-olecreatefromdata)aufrufen zu müssen.

### <a name="cached-data-formats"></a>Zwischengespeicherte Datenformate

Wenn die Shell eine Schrott Datei erstellt, wird die Registrierung auf die Liste der verfügbaren Formate überprüft. Standardmäßig sind zwei Formate verfügbar: CF \_ embedsource und CF \_ LinkSource. Es gibt jedoch eine Reihe von Szenarien, in denen Anwendungen möglicherweise Dateien in verschiedenen Formaten haben müssen:

-   , Um das Übertragen von Daten Auszüge an nicht-OLE-Container zuzulassen, wodurch eingebettete Objekt Formate nicht akzeptiert werden können.
-   , Damit Suites von Anwendungen mit einem privaten Format kommunizieren können.
-   , Um Roundtrips einfacher zu handhaben.

Anwendungen können dem Schrott Formate hinzufügen, indem Sie Sie in der Registrierung Zwischenspeichern. Es gibt zwei Arten von zwischengespeicherten Formaten:

-   Prioritäts Cache Formate. Für diese Formate werden die Daten vollständig aus dem Datenobjekt in den Schrott kopiert.
-   Verzögert gerenderte Formate. Für diese Formate wird das Datenobjekt nicht in den Schrott kopiert. Stattdessen wird das Rendering verzögert, bis ein Ziel die Daten anfordert. Das Verzögerungs Rendering wird im nächsten Abschnitt ausführlicher erläutert.

Zum Hinzufügen eines Prioritäts Caches oder eines verzögerten gerenderten Formats erstellen Sie unter dem **CLSID** -Schlüssel der Anwendung, bei der es sich um die Datenquelle handelt, einen **DataFormat** -Unterschlüssel. Erstellen Sie unter diesem Unterschlüssel einen **prioritycacheformats** -oder einen **Delta Format** -Unterschlüssel. Erstellen Sie für jeden Prioritäts Cache oder das verzögert gerenderte Format einen nummerierten Unterschlüssel, beginnend mit 0 (null). Legen Sie den Wert dieses Schlüssels entweder auf eine Zeichenfolge mit dem registrierten Namen des Formats oder einen \# X-Wert fest, wobei X die Format Nummer eines standardmäßigen Zwischenablage Formats darstellt.

Das folgende Beispiel zeigt zwischengespeicherte Formate für zwei Anwendungen. Die MyProg1-Anwendung hat das Rich-Text-Format als Prioritäts Cache Format und das private Format "My Format" als verzögert gerendertes Format. Die MyProg2-Anwendung hat das CF- \_ Bitmapformat ( \# 8) als Prioritäts Cache Format.

```
HKEY_CLASSES_ROOT
   CLSID
      {GUID}
         (Default) = MyProg1
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = Rich Text Format
            DelayRenderFormats
               0
                  (Default) = My Format
      {GUID}
         (Default) = MyProg2
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = #8
```

Weitere Formate können hinzugefügt werden, indem zusätzliche nummerierte Unterschlüssel erstellt werden.

### <a name="delayed-rendering"></a>Verzögertes Rendering

Ein verzögertes Renderingformat ermöglicht einer Anwendung, eine Schrott Datei zu erstellen, aber die Kosten für das Rendern der Daten zu verzögern, bis Sie von einem Ziel angefordert werden. Die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle eines Schrott Angebots bietet die verzögerten Renderingformate für das Ziel zusammen mit nativen und zwischengespeicherten Daten. Wenn das Ziel ein verzögertes Renderingformat anfordert, führt die Shell die Anwendung aus und stellt die Daten für das Ziel aus dem aktiven Objekt bereit.

> [!Note]  
> Da das verzögerte Rendering etwas riskant ist, sollte es mit Bedacht verwendet werden. Dies funktioniert nicht, wenn der Server nicht verfügbar ist, oder bei Anwendungen, die nicht OLE-fähig sind.

 

## <a name="dragging-and-dropping-shell-objects-asynchronously"></a>Asynchrones ziehen und Ablegen von shellobjekten

**Szenario:** Ein Benutzer überträgt einen großen Datenblock von der Quelle zum Ziel. Um zu vermeiden, dass beide Anwendungen für einen beträchtlichen Zeitraum blockiert werden, extrahiert das Ziel die Daten asynchron.

Normalerweise ist Drag & amp; Drop ein synchroner Vorgang. Kurz gesagt:

1.  Die Drop-Quelle ruft [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) auf und blockiert ihren primären Thread, bis die Funktion zurückgibt. Das Blockieren des primären Threads blockiert normalerweise die UI-Verarbeitung.
2.  Nachdem die [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Methode des Ziels aufgerufen wurde, extrahiert das Ziel die Daten aus dem Datenobjekt im primären Thread. Diese Prozedur blockiert normalerweise die UI-Verarbeitung des Ziels für die Dauer des Extraktions Vorgangs.
3.  Nachdem die Daten extrahiert wurden, gibt das Ziel den [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Rückruf zurück, das System gibt [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)zurück, und beide Threads können fortgesetzt werden.

Kurz gesagt, kann die synchrone Datenübertragung die primären Threads beider Anwendungen für einen beträchtlichen Zeitraum blockieren. Insbesondere müssen beide Threads warten, während die Daten vom Ziel extrahiert werden. Bei kleinen Datenmengen ist die Zeit, die zum Extrahieren von Daten erforderlich ist, gering, und die synchrone Datenübertragung funktioniert sehr gut. Das synchrone extrahieren großer Datenmengen kann jedoch zu langen Verzögerungen führen und die Benutzeroberfläche von Ziel und Quelle beeinträchtigen.

Die [**iasyncoperation**](/previous-versions//bb776309(v=vs.85)) / [**idataobjectasynccapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) -Schnittstelle ist eine optionale Schnittstelle, die von einem Datenobjekt implementiert werden kann. Sie ermöglicht dem Dropziel das asynchrone Extrahieren von Daten aus dem Datenobjekt in einem Hintergrund Thread. Nachdem die Datenextraktion an den Hintergrund Thread übergeben wurde, können die primären Threads beider Anwendungen fortgesetzt werden.

### <a name="using-iasyncoperationidataobjectasynccapability"></a>Verwenden von iasyncoperation/idataobjectasynccapability

> [!Note]  
> Die Schnittstelle wurde ursprünglich als " [**iasyncoperation**](/previous-versions//bb776309(v=vs.85))" bezeichnet, aber später in " [**idataobjectasynccapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)" geändert. Andernfalls sind die beiden Schnittstellen identisch.

 

Der Zweck von [**iasyncoperation**](/previous-versions//bb776309(v=vs.85)) / [**idataobjectasynccapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) besteht darin, dass die Drop-Quelle und das Ablage Ziel aushandeln, ob Daten asynchron extrahiert werden können. Im folgenden Verfahren wird erläutert, wie die Drop-Quelle die-Schnittstelle verwendet:

1.  Erstellen Sie ein Datenobjekt, das [**iasyncoperation**](/previous-versions//bb776309(v=vs.85)) / [**idataobjectasynccapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)verfügbar macht.
2.  Setzen Sie [**setasyncmode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode) mit *fdoopasync* auf **Variant \_ true** , um anzugeben, dass ein asynchroner Vorgang unterstützt wird.
3.  Nachdem [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) zurückgegeben wurde, wird [**inoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation)aufgerufen:
    -   Wenn [**inoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) fehlschlägt oder **Variant \_ false** zurückgibt, wurde eine normale synchrone Datenübertragung durchgeführt, und der Daten Extraktions Vorgang ist abgeschlossen. Die Quelle sollte alle erforderlichen Bereinigungs Schritte ausführen und den Vorgang fortsetzen.
    -   Wenn [**inoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) **Variant \_ true** zurückgibt, werden die Daten asynchron extrahiert. Bereinigungs Vorgänge sollten von [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation)behandelt werden.
4.  Geben Sie das Datenobjekt frei.
5.  Wenn die asynchrone Datenübertragung beendet ist, benachrichtigt das Datenobjekt die Quelle normalerweise über eine private Schnittstelle.

Im folgenden Verfahren wird erläutert, wie das Ablage Ziel die [**iasyncoperation**](/previous-versions//bb776309(v=vs.85)) / [**idataobjectasynccapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) -Schnittstelle zum asynchronen Extrahieren von Daten verwendet:

1.  Wenn das System [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)aufruft, rufen Sie [**IDataObject:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, und fordern Sie eine [**iasyncoperation**](/previous-versions//bb776309(v=vs.85)) / [**idataobjectasynccapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) -Schnittstelle (IID \_ iasyncoperation/IID \_ idataobjectasynccapability) aus dem Datenobjekt an.
2.  [**Getasyncmode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode)aufrufen. Wenn die Methode **Variant \_ true** zurückgibt, unterstützt das Datenobjekt die asynchrone Datenextraktion.
3.  Erstellen Sie einen separaten Thread zum Verarbeiten der Datenextraktion, und rufen Sie [**Startoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-startoperation)auf.
4.  Gibt den [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Rückruf zurück, wie bei einem normalen Datenübertragungs Vorgang. [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) gibt die Blockierung der Ablage Quelle zurück und entsperrt Sie. Nennen Sie [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) nicht, um das Ergebnis eines optimierten verschiebe-oder Löschvorgangs anzuzeigen. Warten Sie, bis der Vorgang abgeschlossen ist.
5.  Extrahieren Sie die Daten im Hintergrund Thread. Die Blockierung des primären Threads des Ziels wird aufgehoben und der Vorgang kann fortgesetzt werden.
6.  Wenn es sich bei der Datenübertragung um einen [optimierten](#handling-optimized-move-operations) Verschiebe [-oder Lösch](#handling-delete-on-paste-operations) Vorgang handelt, müssen Sie [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) aufrufen, um das Ergebnis anzugeben.
7.  Benachrichtigen Sie das Datenobjekt, dass die Extraktion abgeschlossen ist, indem Sie [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation)aufrufen.

 

 
