---
description: Die Vorgehensweise zum Implementieren einer Namespace Erweiterung ähnelt der Vorgehensweise für alle anderen in-Process-Component Object Model (com)-Objekte.
title: Implementieren der grundlegenden Ordner Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a45b8011-5355-429b-8935-4a7bdb5d2316
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05f5d2e4c21a923856c7324ad2d407230fa7595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980001"
---
# <a name="implementing-the-basic-folder-object-interfaces"></a>Implementieren der grundlegenden Ordner Objekt Schnittstellen

Die Vorgehensweise zum Implementieren einer Namespace Erweiterung ähnelt der Vorgehensweise für alle anderen in-Process-Component Object Model (com)-Objekte. Alle Erweiterungen müssen drei primäre Schnittstellen unterstützen, die Windows-Explorer die grundlegenden Informationen bereitstellen, die erforderlich sind, um die Ordner der Erweiterung in der Strukturansicht anzuzeigen. Um die Funktionen von Windows Explorer vollständig nutzen zu können, muss Ihre Erweiterung aber auch eine oder mehrere optionale Schnittstellen verfügbar machen, die komplexere Features unterstützen, wie z. b. Kontextmenüs oder Drag & amp; Drop, und eine Ordneransicht bereitstellen.

In diesem Dokument wird erläutert, wie die primären und optionalen Schnittstellen implementiert werden, die Windows Explorer zum Aufrufen von Informationen über die Inhalte ihrer Erweiterung aufruft. Eine Erläuterung zur Implementierung einer Ordneransicht und zum Anpassen von Windows-Explorer finden Sie unter [Implementieren einer Ordneransicht](../lwef/nse-folderview.md).

-   [Grundlegende Implementierung und Registrierung](#basic-implementation-and-registration)
    -   [Registrieren einer Erweiterung](#registering-an-extension)
-   [Behandeln von pidls](#handling-pidls)
    -   [Erstellen einer shitemid-Struktur](#creating-an-shitemid-structure)
    -   [Erstellen einer PIDL](#constructing-a-pidl)
    -   [Interpretieren von pidls](#interpreting-pidls)
-   [Implementieren der primären Schnittstellen](#implementing-the-primary-interfaces)
    -   [Ipersistfolder-Schnittstelle](#ipersistfolder-interface)
    -   [IShellFolder-Schnittstelle](#ishellfolder-interface)
    -   [Ienumittellist-Schnittstelle](#ienumidlist-interface)
-   [Implementieren der optionalen Schnittstellen](#implementing-the-optional-interfaces)
    -   [Iextracticon](#iextracticon)
    -   [IContextMenu](#icontextmenu)
    -   [Iqueryinfo](#iqueryinfo)
    -   [IDataObject und IDropTarget](#idataobject-and-idroptarget)
-   [Arbeiten mit der standardmäßigen Shell-Ordner Ansichts Implementierung](#working-with-the-default-shell-folder-view-implementation)

## <a name="basic-implementation-and-registration"></a>Grundlegende Implementierung und Registrierung

Als Prozess interner com-Server muss die DLL mehrere Standardfunktionen und-Schnittstellen verfügbar machen:

-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)
-   [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Diese Funktionen und Schnittstellen werden auf die gleiche Weise wie für die meisten anderen COM-Objekte implementiert. Weitere Informationen finden Sie in der [com-Dokumentation](../com/the-component-object-model.md).

### <a name="registering-an-extension"></a>Registrieren einer Erweiterung

Wie bei allen COM-Objekten müssen Sie eine GUID für die Klassen-ID (CLSID) für die Erweiterung erstellen. Registrieren Sie das Objekt, indem Sie einen Unterschlüssel der **HKEY \_ Classes \_ root** \\ **CLSID** mit dem Namen für die CLSID der Erweiterung erstellen. Die dll muss als Prozess interner Server registriert sein und das Apartment Thread Modell angeben. Sie können das Verhalten des Stamm Ordners einer Erweiterung anpassen, indem Sie dem CLSID-Schlüssel der Erweiterung eine Vielzahl von unter Schlüsseln und Werten hinzufügen.

Einige dieser Werte gelten nur für Erweiterungen mit virtuellen Verknüpfungs Punkten. Diese Werte gelten nicht für Erweiterungen, deren Verknüpfungs Punkte Dateisystem Ordner sind. Weitere Informationen finden Sie unter [angeben des Speicher Orts einer Namespace Erweiterung](nse-junction.md). Um das Verhalten einer Erweiterung mit einem virtuellen Verknüpfungs Punkt zu ändern, fügen Sie dem CLSID-Schlüssel der Erweiterung mindestens einen der folgenden Werte hinzu:

-   Wantsforparamesing. Der namens Name für eine Erweiterung mit einem virtuellen Verknüpfungs Punkt weist normalerweise das folgende Format auf: {*GUID*}. Erweiterungen dieses Typs enthalten normalerweise virtuelle Elemente. Einige Erweiterungen, z. b. eigene Dokumente, entsprechen jedoch tatsächlich Dateisystem Ordnern, auch wenn Sie über virtuelle Verknüpfungs Punkte verfügen. Wenn die Erweiterung Dateisystem Objekte auf diese Weise darstellt, können Sie den Wert wantsforbising festlegen. Windows-Explorer fordert dann den Namen des Stamm Ordners an, indem er die [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) -Methode des Ordner Objekts mit *uFlags* , die auf **shgdn- \_ forcsing** festgelegt sind, und *PIDL* auf einen einzelnen leeren Zeiger auf eine Element Bezeichner-Liste (PIDL) festgelegt hat. Eine leere PIDL enthält nur ein Terminator. Die Methode sollte dann den Namen des Stamm Ordners:: {*GUID*}-Parser zurückgeben.
-   Hidefolderverbs. Die Verben, die unter **HKEY \_ Classes \_ root** \\ **Folder** registriert sind, sind normalerweise allen Erweiterungen zugeordnet. Sie werden im Kontextmenü der Erweiterung angezeigt und können von [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)aufgerufen werden. Um zu verhindern, dass diese Verben ihrer Erweiterung zugeordnet werden, legen Sie den Wert hidefolderverbs fest.
-   Hideasdelete. Wenn ein Benutzer versucht, die Erweiterung zu löschen, wird die Erweiterung stattdessen von Windows-Explorer ausgeblendet.
-   Hideasdeleteperuser. Dieser Wert hat die gleiche Wirkung wie hideasdelete, aber auf Benutzerbasis. Die Erweiterung ist nur für Benutzer verborgen, die versucht haben, Sie zu löschen. Die Erweiterung ist für alle anderen Benutzer sichtbar.
-   Queryforoverlay. Legen Sie diesen Wert fest, um anzugeben, dass das Symbol des Stamm Ordners eine Symbol Überlagerung aufweisen kann. Das Folder-Objekt muss die [**ishellienoverlay**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishelliconoverlay) -Schnittstelle unterstützen. Bevor Windows Explorer das Symbol des Stamm Ordners anzeigt, wird ein Überlagerungs Symbol angefordert, indem eine der beiden **ishellienoverlay** -Methoden aufgerufen wird, bei der *pidlitem* auf eine leere PIDL festgelegt ist.

Die verbleibenden Werte und Unterschlüssel gelten für alle Erweiterungen:

-   Um den anzeigen amen des Ordners für den Verknüpfungs Punkt der Erweiterung anzugeben, legen Sie den Standardwert des CLSID-unter Schlüssels der Erweiterung auf eine entsprechende Zeichenfolge fest.
-   Wenn der Cursor auf einen Ordner zeigt, wird in der Regel ein InfoTipp angezeigt, in dem der Inhalt des Ordners beschrieben wird. Um einen InfoTipp für den Stamm Ordner Ihrer Erweiterung anzugeben, erstellen Sie einen InfoTipp **reg \_ SZ** -Wert für den CLSID-Schlüssel der Erweiterung, und legen Sie ihn auf eine entsprechende Zeichenfolge fest.
-   Um ein benutzerdefiniertes Symbol für den Stamm Ordner Ihrer Erweiterung anzugeben, erstellen Sie einen Unterschlüssel für den CLSID-Unterschlüssel der Erweiterung namens **DefaultIcon**. Legen Sie den Standardwert von **DefaultIcon** auf einen **reg \_ SZ** -Wert fest, der den Namen der Datei enthält, in der das Symbol enthalten ist, gefolgt von einem Komma, gefolgt von einem Minuszeichen, gefolgt vom Index des Symbols in dieser Datei.
-   Standardmäßig enthält das Kontextmenü des Stamm Ordners der Erweiterung die Elemente, die unter **HKEY \_ Classes \_ root \\ Folder** definiert sind. Wenn Sie die entsprechenden sfgao xxx-Flags festgelegt haben, werden die Elemente **Löschen**, **Umbenennen** und **Eigenschaften** hinzugefügt \_ . Sie können dem Kontextmenü des Stamm Ordners weitere Elemente hinzufügen oder vorhandene Elemente außer Kraft setzen, ähnlich wie für einen [Dateityp](fa-file-types.md). Erstellen Sie unter dem CLSID-Schlüssel der Erweiterung einen **shellunterschlüssel** , und definieren Sie die Befehle, wie unter Erweitern von Kontext [Menüs](context.md)erläutert.
-   Wenn Sie eine flexiblere Methode zum Behandeln des Kontextmenüs des Stamm Ordners benötigen, können Sie einen Kontext [Menü Handler](context-menu-handlers.md)implementieren. Um den Kontextmenü Handler zu registrieren, erstellen Sie unter dem CLSID-Schlüssel der Erweiterung einen **shellex** -Schlüssel. Registrieren Sie die CLSID des Handlers wie bei einem herkömmlichen [Erstellen von Shellerweiterungs Handlern](handlers.md).
-   Wenn Sie dem Eigenschaften Blatt des Stamm Ordners eine Seite hinzufügen möchten, geben Sie dem Ordner das **sfgao \_ haspropsheet** -Attribut, und implementieren Sie einen [Eigenschaften Blatt Handler](propsheet-handlers.md). Um den Eigenschaften Blatt Handler zu registrieren, erstellen Sie unter dem CLSID-Schlüssel der Erweiterung einen **shellex** -Schlüssel. Registrieren Sie die CLSID des Handlers wie bei einem herkömmlichen [Erstellen von Shellerweiterungs Handlern](handlers.md).
-   Fügen Sie dem CLSID-Unterschlüssel der Erweiterung einen **ShellFolder** -Unterschlüssel hinzu, um die Attribute des Stamm Ordners anzugeben. Erstellen Sie einen Attribut Wert, und legen Sie ihn auf die geeignete Kombination von [**sfgao \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) -Flags fest.

In der folgenden Tabelle werden einige häufig verwendete Attribute für Stamm Ordner aufgelistet.



| Flag                | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                       |
|---------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sfgao- \_ Ordner       | 0x20000000 | Der Stamm Ordner der Erweiterung enthält ein oder mehrere Elemente.                                                                                                                                                                                                                                                           |
| sfgao \_ hassubfolder | 0x80000000 | Der Stamm Ordner der Erweiterung enthält mindestens einen Unterordner. In Windows-Explorer wird ein Pluszeichen (+) neben dem Ordnersymbol platziert.                                                                                                                                                                               |
| sfgao- \_ Kerzen    | 0x00000020 | Der Stamm Ordner der Erweiterung kann vom Benutzer gelöscht werden. Das Kontextmenü des Ordners enthält ein Element **Löschen** . Dieses Flag sollte für Verknüpfungs Punkte festgelegt werden, die unter einem der [virtuellen Ordner](nse-junction.md)abgelegt werden.                                                                                 |
| sfgao \_ canrename    | 0x00000010 | Der Stamm Ordner der Erweiterung kann vom Benutzer umbenannt werden. Das Kontextmenü des Ordners enthält ein Element zum **Umbenennen** .                                                                                                                                                                                                   |
| sfgao \_ haspropsheet | 0x00000040 | Der Stamm Ordner der Erweiterung verfügt über ein Eigenschaften Blatt " **Eigenschaften** ". Das Kontextmenü des Ordners enthält ein **Eigenschaften** Element. Um das Eigenschaften Blatt bereitzustellen, müssen Sie einen [Eigenschaften Blatt Handler](propsheet-handlers.md)implementieren. Registrieren Sie den Handler unter dem CLSID-Schlüssel der Erweiterung, wie bereits erläutert. |



 

Das folgende Beispiel zeigt den CLSID-Registrierungs Eintrag für eine Erweiterung mit dem anzeigen Amen MyExtension. Die Erweiterung verfügt über ein benutzerdefiniertes Symbol, das in der dll der Erweiterung mit einem Index von 1 enthalten ist. Der **sfgao- \_ Ordner**, **sfgao \_ hassubfolder** und **sfgao- \_ Kerzen** Attribute werden festgelegt.

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         (Default) = MyExtension
         InfoTip = Some appropriate text
      DefaultIcon
         (Default) = c:\MyDir\MyExtension.dll,-1
      InProcServer32
         (Default) = c:\MyDir\MyExtension.dll
         ThreadingModel = Apartment
      ShellFolder
         Attributes = 0xA00000020
```

## <a name="handling-pidls"></a>Behandeln von pidls

Jedes Element im Shellnamespace muss eine eindeutige PIDL aufweisen. Windows-Explorer weist Ihrem Stamm Ordner eine PIDL zu und übergibt den Wert während der Initialisierung an Ihre Erweiterung. Ihre Erweiterung ist dann dafür verantwortlich, jedem Ihrer Objekte eine ordnungsgemäß konstruierte PIDL zuzuweisen und diese pidls auf Anforderung an Windows-Explorer zu übergeben. Wenn die Shell eine PIDL verwendet, um eines der Objekte der Erweiterung zu identifizieren, muss die Erweiterung die PIDL interpretieren und das jeweilige Objekt identifizieren können. In ihrer Erweiterung müssen jedem Objekt auch ein [**Anzeige Name**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof) und ein *namens Name* zugewiesen werden. Da pidls von praktisch jeder Ordner Schnittstelle verwendet werden, implementieren Erweiterungen in der Regel einen einzelnen *PIDL-Manager* , um all diese Aufgaben auszuführen.

Der Begriff PIDL ist für eine [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur oder einen Zeiger auf eine solche Struktur, abhängig vom Kontext, kurz. Wie deklariert, verfügt eine **itemidlist** -Struktur über einen einzelnen Member, eine [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur. Die **itemidlist** -Struktur eines Objekts ist tatsächlich ein gepacktes Array aus zwei oder mehr **shitemid** -Strukturen. Die Reihenfolge dieser Strukturen definiert einen Pfad über den Namespace, ähnlich wie c: \\ mydirectory \\ MyFile einen Pfad durch das Dateisystem definiert. In der Regel besteht die PIDL eines Objekts aus einer Reihe von **shitemid** -Strukturen, die den Ordnern entsprechen, die den Namespace Pfad definieren, gefolgt von der **shitemid** -Struktur des Objekts, gefolgt von einem Abschluss Zeichen.

Das Abschluss Zeichen ist eine [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur, bei der der *CB* -Member auf **null** festgelegt ist. Das Abschluss Zeichen ist erforderlich, da die Anzahl der **shitemid** -Strukturen in der PIDL eines Objekts von der Position des Objekts im Shellnamespace und vom Startpunkt des Pfads abhängt. Außerdem kann die Größe der verschiedenen **shitemid** -Strukturen variieren. Wenn Sie eine PIDL erhalten, haben Sie keine einfache Möglichkeit, ihre Größe oder sogar die Gesamtzahl der **shitemid** -Strukturen zu bestimmen. Stattdessen müssen Sie das gepackte Array (Struktur nach Struktur) "durchlaufen", bis Sie das Abschluss Zeichen erreichen.

Zum Erstellen einer PIDL muss Ihre Anwendung folgende Aktionen ausführen:

1.  Erstellen Sie für jedes seiner Objekte eine [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur.
2.  Assemblieren Sie die relevanten [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Strukturen in eine PIDL.

### <a name="creating-an-shitemid-structure"></a>Erstellen einer shitemid-Struktur

Die [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur eines Objekts identifiziert das Objekt in seinem Ordner eindeutig. Tatsächlich besteht ein PIDL-Typ, der von vielen der [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Methoden verwendet wird, nur aus der **shitemid** -Struktur des Objekts, gefolgt von einem Abschluss Zeichen. Die Definition einer **shitemid** -Struktur lautet wie folgt:


```C++
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



Der *Abid* -Member ist der Bezeichner des Objekts. Da die Länge von *Abid* nicht definiert ist und variieren kann, wird das *CB* -Element auf die Größe der [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur in Bytes festgelegt.

Da weder die Länge noch der Inhalt von *Abid* standardisiert ist, können Sie ein beliebiges Schema verwenden, das Sie Ihren Objekten *Abid* -Werte zuweisen möchten. Die einzige Anforderung besteht darin, dass Sie nicht zwei Objekte im gleichen Ordner mit identischen Werten haben können. Aus Leistungsgründen sollte die [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur jedoch **DWORD**-bündig sein. Mit anderen Worten, Sie sollten Ihre *Abid* -Werte so erstellen, dass *CB* ein ganzzahliges Vielfaches von 4 ist.

In der Regel verweist *Abid* auf eine Erweiterungs definierte Struktur. Zusätzlich zur Objekt-ID wird diese Struktur häufig verwendet, um eine Vielzahl von verknüpften Informationen, wie z. b. den Typ oder die Attribute des Objekts, zu speichern. Die Ordner Objekte Ihrer Erweiterung können dann schnell die Informationen aus der PIDL extrahieren, anstatt Sie Abfragen zu müssen.

> [!Note]  
> Einer der wichtigsten Aspekte beim Entwerfen einer Datenstruktur für eine PIDL ist, dass die Struktur dauerhaft und transportierbar ist. Im Kontext von pidls lautet die Bedeutung dieser Begriffe:
>
> -   Permanenten. Das System platziert häufig pidls in verschiedenen Typen von langfristiger Speicherung, wie z. b. Verknüpfungs Dateien. Anschließend können diese pidls später aus dem Speicher wieder hergestellt werden, möglicherweise nachdem das System neu gestartet wurde. Eine PIDL, die aus dem Speicher wieder hergestellt wurde, muss weiterhin gültig und für Ihre Erweiterung aussagekräftig sein. Diese Anforderung bedeutet beispielsweise, dass Sie keine Zeiger oder Handles in der PIDL-Struktur verwenden sollten. Pidls, die diesen Datentyp enthalten, sind normalerweise bedeutungslos, wenn Sie vom System später aus dem Speicher wieder hergestellt werden.
> -   Austauschen. Eine PIDL muss beim Transport von einem Computer zu einem anderen sinnvoll bleiben. Beispielsweise kann eine PIDL in eine Verknüpfungs Datei geschrieben, auf eine Diskette kopiert und auf einen anderen Computer übertragen werden. Diese PIDL sollte weiterhin für Ihre Erweiterung sinnvoll sein, die auf dem zweiten Computer ausgeführt wird. Um beispielsweise sicherzustellen, dass Ihre pidls transportierbar sind, verwenden Sie entweder ANSI-oder Unicode-Zeichen explizit. Vermeiden Sie Datentypen wie **TCHAR** oder **LPTSTR**. Wenn Sie diese Datentypen verwenden, kann eine auf einem Computer mit einer Unicode-Version der Erweiterung erstellte PIDL nicht durch eine ANSI-Version dieser Erweiterung gelesen werden, die auf einem anderen Computer ausgeführt wird.

 

Die folgende Deklaration zeigt ein einfaches Beispiel für eine Datenstruktur.


```C++
typedef struct tagMYPIDLDATA {
  USHORT cb;
  DWORD dwType;
  WCHAR wszDisplayName[40];
} MYPIDLDATA, *LPMYPIDLDATA;
```



Das **CB** -Element wird auf die Größe der **mypidldata** -Struktur festgelegt. Dieser Member macht **mypidldata** zu einer gültigen [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur in und von sich selbst. Die restlichen Member entsprechen dem **Abid** -Element einer **shitemid** -Struktur und enthalten private Daten. Der **dwType** -Member ist ein Erweiterungs definierter Wert, der den Objekttyp angibt. In diesem Beispiel wird **dwType** für Ordner auf **true** und andernfalls **false** festgelegt. Mit diesem Member können Sie beispielsweise schnell feststellen, ob es sich bei dem Objekt um einen Ordner handelt. Der **wszdisplayname** -Member enthält den anzeigen amen des Objekts. Da Sie nicht denselben anzeigen Amen zwei verschiedenen Objekten im selben Ordner zuweisen würden, fungiert der Anzeige Name auch als Objekt-ID. In diesem Beispiel ist **wszdisplayname** auf 40 Zeichen festgelegt, um sicherzustellen, dass die **shitemid** -Struktur **DWORD**-ausgerichtet wird. Wenn Sie die Größe Ihrer pidls begrenzen möchten, können Sie stattdessen ein Zeichen Array variabler Länge verwenden und den Wert von CB entsprechend anpassen. Füllt die Anzeige \\ Zeichenfolge mit ausreichenden ' 0 '-Zeichen auf, um die **DWORD** -Ausrichtung der Struktur beizubehalten. Andere Member, die nützlich sein können, um in die Struktur einzufügen, beinhalten die Größe, Attribute oder den Namen des Objekts.

### <a name="constructing-a-pidl"></a>Erstellen einer PIDL

Nachdem Sie [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Strukturen für Ihre Objekte definiert haben, können Sie diese verwenden, um eine PIDL zu erstellen. Pidls können für eine Vielzahl von Zwecken erstellt werden, aber die meisten Aufgaben verwenden einen von zwei Arten von PIDL. Die einfachste, eine PIDL auf einzelner Ebene, identifiziert das Objekt relativ zum übergeordneten Ordner. Diese Art von PIDL wird von vielen der [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Methoden verwendet. Eine PIDL einer einzelnen Ebene enthält die **shitemid** -Struktur des Objekts, gefolgt von einem Abschluss Zeichen. Eine voll qualifizierte PIDL definiert einen Pfad der Namespace Hierarchie vom Desktop zum Objekt. Diese Art von PIDL beginnt beim Desktop und enthält eine **shitemid** -Struktur für jeden Ordner im Pfad, gefolgt vom-Objekt und dem-Abschluss Zeichen. Eine voll qualifizierte PIDL identifiziert das Objekt innerhalb des gesamten shellnamespaces eindeutig.

Die einfachste Möglichkeit zum Erstellen einer PIDL besteht darin, direkt mit der [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur zu arbeiten. Erstellen Sie eine **itemidlist** -Struktur, und weisen Sie ausreichend Arbeitsspeicher zu, um alle [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Strukturen zu speichern. Die Adresse dieser Struktur verweist auf die anfängliche **shitemid** -Struktur. Definieren Sie Werte für die Elemente dieser anfangs Struktur, und fügen Sie dann beliebig viele zusätzliche **shitemid** -Strukturen in der entsprechenden Reihenfolge an. Im folgenden Verfahren wird das Erstellen einer PIDL auf einer einzelnen Ebene beschrieben. Sie enthält zwei **shitemid** -Strukturen – eine **mypidldata** -Struktur gefolgt von einem Abschluss Zeichen:

1.  Verwenden Sie die [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion, um Arbeitsspeicher für die PIDL zuzuweisen. Weisen Sie ausreichend Arbeitsspeicher für Ihre privaten Daten sowie einen **UShort** (zwei Bytes) für das Abschluss Zeichen zu. Wandeln Sie das Ergebnis in lpmypidldata um.
2.  Legen Sie den CB-Member der ersten **mypidldata** -Struktur auf die Größe der Struktur fest. In diesem Beispiel würden Sie **CB** auf sizeof (mypidldata) festlegen. Wenn Sie eine Struktur mit variabler Länge verwenden möchten, müssen Sie den Wert von **CB** berechnen.
3.  Weisen Sie den privaten Datenmembern geeignete Werte zu.
4.  Berechnen Sie die Adresse der nächsten [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur. Wandeln Sie die Adresse der aktuellen mypidldata-Struktur in LPBYTE um, und fügen Sie diesen Wert dem Wert von **CB** hinzu, der in Schritt 3 festgelegt wurde.
5.  In diesem Fall ist die nächste [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur das Abschluss Zeichen. Legen Sie den **CB** -Member der-Struktur auf NULL fest.

Für längere pidls weisen Sie ausreichenden Arbeitsspeicher zu, und wiederholen Sie die Schritte 3-5 für jede weitere [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur.

Die folgende Beispiel Funktion nimmt den Typ und den anzeigen Amen eines Objekts an und gibt die PIDL der einzelnen Ebene des-Objekts zurück. Die-Funktion geht davon aus, dass der Anzeige Name, einschließlich des abschließenden **null** -Zeichens, nicht die Anzahl von Zeichen überschreitet, die für die **mypidldata** -Struktur deklariert wurden. Wenn sich diese Annahme als fehlerhaft herausstellt, schneidet die [**stringcbcopyw**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) -Funktion den anzeigen Amen ab. Die Variable " **g \_ pmalloc** " ist ein [**imzuordnungszeiger**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) , der an anderer Stelle erstellt und in einer globalen Variablen gespeichert wird.


```C++
LPITEMIDLIST CreatePIDL(DWORD dwType, LPCWSTR pwszDisplayName)
{
    LPMYPIDLDATA   pidlOut;
    USHORT         uSize;

    pidlOut = NULL;

    //Calculate the size of the MYPIDLDATA structure.
    uSize = sizeof(MYPIDLDATA);

    // Allocate enough memory for the PIDL to hold a MYPIDLDATA structure 
    // plus the terminator
    pidlOut = (LPMYPIDLDATA)m_pMalloc->Alloc(uSize + sizeof(USHORT));

    if(pidlOut)
    {
       //Assign values to the members of the MYPIDLDATA structure
       //that is the PIDL's first SHITEMID structure
       pidlOut->cb = uSize;
       pidlOut->dwType = dwType;
       hr = StringCbCopyW(pidlOut->wszDisplayName, 
                          sizeof(pidlOut->wszDisplayName), pwszDisplayName);
       
       // TODO: Add error handling here to verify the HRESULT returned 
       // by StringCbCopyW.

       //Advance the pointer to the start of the next SHITEMID structure.
       pidlOut = (LPMYPIDLDATA)((LPBYTE)pidlOut + pidlOut->cb);

       //Create the terminating null character by setting cb to 0.
       pidlOut->cb = 0;
    }

    return pidlOut;
```



Eine voll qualifizierte PIDL muss über [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Strukturen für jedes Objekt vom Desktop zum Objekt verfügen. Die Erweiterung erhält eine voll qualifizierte PIDL für Ihren Stamm Ordner, wenn die Shell [**ipersistfolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize)aufruft. Um eine voll qualifizierte PIDL für ein Objekt zu erstellen, nehmen Sie die PIDL, die die Shell dem Stamm Ordner zugewiesen hat, an, und fügen Sie die **shitemid** -Strukturen an, die erforderlich sind, um Sie aus dem Stamm Ordner zum Objekt zu gelangen.

### <a name="interpreting-pidls"></a>Interpretieren von pidls

Wenn die Shell oder eine Anwendung eine der Schnittstellen der Erweiterung aufruft, um Informationen zu einem Objekt anzufordern, wird das Objekt in der Regel durch eine PIDL identifiziert. Einige Methoden, z. b. [**IShellFolder:: getuiobjectof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), verwenden pidls, die relativ zum übergeordneten Ordner sind und leicht interpretiert werden können. Allerdings erhält Ihre Erweiterung wahrscheinlich auch voll qualifizierte pidls. Der PIDL-Manager muss dann bestimmen, auf welche Objekte die PIDL verweist.

Was die Aufgabe der Zuordnung eines Objekts zu einer voll qualifizierten PIDL erschwert, besteht darin, dass eine oder mehrere der anfänglichen [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Strukturen in der PIDL zu Objekten gehören können, die sich außerhalb ihrer Erweiterung im Shell-Namespace befinden. Sie haben keine Möglichkeit, die Bedeutung des *Abid* -Members dieser Strukturen zu interpretieren. Die Erweiterung muss die Liste der **shitemid** -Strukturen "durchlaufen", bis Sie die Struktur erreichen, die dem Stamm Ordner entspricht. Danach wissen Sie, wie die Informationen in den **shitemid** -Strukturen interpretiert werden.

Nehmen Sie zum Durchlaufen der PIDL den ersten *CB* -Wert an, und fügen Sie ihn der Adresse der PIDL hinzu, um den Zeiger auf den Anfang der nächsten [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur zu setzen. Er zeigt dann auf das *CB* -Element dieser Struktur, das Sie verwenden können, um den Zeiger auf den Anfang der nächsten **shitemid** -Struktur zu verschieben, usw. Überprüfen Sie jedes Mal, wenn Sie den Zeiger verschieben, die **shitemid** -Struktur, um zu bestimmen, ob Sie den Stamm des Namespace ihrer Erweiterung erreicht haben.

## <a name="implementing-the-primary-interfaces"></a>Implementieren der primären Schnittstellen

Wie bei allen COM-Objekten ist das Implementieren einer Erweiterung größtenteils eine Frage der Implementierung einer Auflistung von Schnittstellen. In diesem Abschnitt werden die drei primären Schnittstellen erläutert, die von allen Erweiterungen implementiert werden müssen. Sie werden für die Initialisierung und zum Bereitstellen von grundlegenden Informationen zum Inhalt der Erweiterung in Windows-Explorer verwendet. Diese Schnittstellen und eine [Ordneransicht](../lwef/nse-folderview.md)sind alles, was für eine funktionale Erweiterung erforderlich ist. Um jedoch die Features von Windows Explorer voll ausnutzen zu können, implementieren die meisten Erweiterungen auch eine oder mehrere optionale Schnittstellen.

### <a name="ipersistfolder-interface"></a>Ipersistfolder-Schnittstelle

Die [**ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) -Schnittstelle wird aufgerufen, um ein neues Ordner Objekt zu initialisieren. Die [**ipersistfolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) -Methode weist dem neuen-Objekt eine voll qualifizierte PIDL zu. Diese PIDL für die spätere Verwendung speichern. Beispielsweise muss ein Ordner Objekt diese PIDL verwenden, um voll qualifizierte pidls für die untergeordneten Elemente des Objekts zu erstellen. Der Ersteller des Ordner Objekts kann auch [**ipersistent:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) aufrufen, um die CLSID des Objekts anzufordern.

In der Regel wird ein Ordner Objekt von der [**IShellFolder:: BindTo Object**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) -Methode des übergeordneten Ordners erstellt und initialisiert. Wenn ein Benutzer jedoch die Erweiterung durchsucht, erstellt und initialisiert Windows-Explorer das Stamm Ordner Objekt der Erweiterung. Die PIDL, die das Stamm Ordner Objekt über [**ipersistfolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) empfängt, enthält den Pfad vom Desktop zum Stamm Ordner, den Sie benötigen, um voll qualifizierte pidls für Ihre Erweiterung zu erstellen.

### <a name="ishellfolder-interface"></a>IShellFolder-Schnittstelle

Die Shell behandelt eine Erweiterung als hierarchisch sortiertes Auflistung von Ordner Objekten. Die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle ist das Kernstück jeder Erweiterungs Implementierung. Es stellt ein Ordner Objekt dar und bietet Windows-Explorer einen Großteil der Informationen, die erforderlich sind, um den Inhalt des Ordners anzuzeigen.

" [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) " ist in der Regel die einzige andere Ordner Schnittstelle als " [**ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) ", die direkt von einem Ordner Objekt verfügbar gemacht wird. Während Windows-Explorer eine Vielzahl von erforderlichen und optionalen Schnittstellen verwendet, um Informationen über den Inhalt des Ordners abzurufen, erhält er mithilfe von **IShellFolder** Zeiger auf diese Schnittstellen.

Windows-Explorer Ruft die CLSID des Stamm Ordners ihrer Erweiterung auf verschiedene Weise ab. Weitere Informationen finden Sie unter Angeben des Speicher [Orts einer Namespace Erweiterung](nse-junction.md) oder [Anzeigen einer Self-Contained Sicht einer Namespace Erweiterung](nse-view.md). Windows-Explorer verwendet diese CLSID dann, um eine Instanz des Stamm Ordners zu erstellen und zu initialisieren und eine [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle abzufragen. Die Erweiterung erstellt ein Ordner Objekt, das den Stamm Ordner darstellt, und gibt die **IShellFolder** -Schnittstelle des Objekts zurück. Ein Großteil der übrigen Interaktionen zwischen ihrer Erweiterung und Windows Explorer erfolgt über **IShellFolder**. Der Windows-Explorer ruft **IShellFolder** auf:

-   Fordern Sie ein Objekt an, das den Inhalt des Stamm Ordners aufzählen kann.
-   Abrufen verschiedener Arten von Informationen über den Inhalt des Stamm Ordners.
-   Fordern Sie ein Objekt an, das eine der optionalen Schnittstellen verfügbar macht. Diese Schnittstellen können dann nach zusätzlichen Informationen, z. b. Symbolen oder Kontextmenüs, abgefragt werden.
-   Fordern Sie ein Ordner Objekt an, das einen Unterordner des Stamm Ordners darstellt.

Wenn ein Benutzer einen Unterordner des Stamm Ordners öffnet, ruft Windows Explorer [**IShellFolder:: bindtoken Object**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject)auf. Die Erweiterung erstellt und initialisiert ein neues Ordner Objekt, um den Unterordner darzustellen, und gibt die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle zurück. Windows-Explorer ruft diese Schnittstelle dann für verschiedene Arten von Informationen auf, usw., bis der Benutzer beschließt, an einer anderen Stelle im Shell-Namespace zu navigieren oder Windows-Explorer zu schließen.

Im restlichen Teil dieses Abschnitts werden die wichtigeren [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Methoden und deren Implementierung kurz erläutert.

### <a name="enumobjects"></a>EnumObjects

Vor dem Anzeigen des Inhalts eines Ordners in der Strukturansicht muss Windows-Explorer zunächst ermitteln, was der Ordner enthält, indem er die [**IShellFolder:: erumubjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) -Methode aufrufen. Diese Methode erstellt ein Standardmäßiges OLE-Enumerationsobjekt, das eine [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) -Schnittstelle verfügbar macht und den Schnittstellen Zeiger zurückgibt Die **ienumittellist** -Schnittstelle ermöglicht Windows-Explorer das Abrufen der pidls aller Objekte, die im Ordner enthalten sind. Diese pidls werden dann verwendet, um Informationen über die Objekte zu erhalten, die im Ordner enthalten sind. Weitere Informationen finden Sie unter [ienumittellist-Schnittstelle](#ienumidlist-interface).

> [!Note]  
> Die [**ienumittellist:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) -Methode sollte nur pidls zurückgeben, die relativ zum übergeordneten Ordner sind. Die PIDL sollte nur die [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur des Objekts, gefolgt von einem Abschluss Zeichen, enthalten.

 

### <a name="createviewobject"></a>"Ansichts Objekt"

Bevor der Inhalt eines Ordners angezeigt wird, ruft Windows-Explorer diese Methode auf, um einen Zeiger auf eine [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Schnittstelle anzufordern. Diese Schnittstelle wird von Windows-Explorer zum Verwalten der Ordneransicht verwendet. Erstellen Sie ein Ordner Ansichts Objekt, und geben Sie dessen **ishellview** -Schnittstelle zurück

Die [**IShellFolder:: deateviewobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) -Methode wird auch aufgerufen, um eine der optionalen Schnittstellen (z. b. [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)) für den Ordner selbst anzufordern. Die Implementierung dieser Methode sollte ein Objekt erstellen, das die angeforderte Schnittstelle verfügbar macht und den Schnittstellen Zeiger zurückgibt. Wenn Windows-Explorer eine optionale Schnittstelle für eines der im Ordner enthaltenen Objekte benötigt, wird [**IShellFolder:: getuiobjectof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)aufgerufen.

### <a name="getuiobjectof"></a>Getuiobjectof

Obwohl grundlegende Informationen über den Inhalt eines Ordners über die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Methoden verfügbar sind, kann Ihre Erweiterung Windows-Explorer auch verschiedene Arten zusätzlicher Informationen bereitstellen. Beispielsweise können Sie Symbole für den Inhalt eines Ordners oder das Kontextmenü eines Objekts angeben. Windows-Explorer Ruft die [**IShellFolder:: getuiobjectof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) -Methode auf, um zu versuchen, zusätzliche Informationen über ein Objekt abzurufen, das in einem Ordner enthalten ist. Windows-Explorer gibt an, für welches Objekt die Informationen und die IID der entsprechenden Schnittstelle benötigt werden. Das Folder-Objekt erstellt dann ein-Objekt, das die angeforderte Schnittstelle verfügbar macht und den Schnittstellen Zeiger zurückgibt.

Wenn die Erweiterung Benutzern das Übertragen von Objekten mit Drag & Drop oder der Zwischenablage ermöglicht, ruft Windows-Explorer [**IShellFolder:: getuiobjectof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) auf, um eine [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -oder [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle anzufordern. Weitere Informationen finden Sie unter [übertragen von shellobjekten mit Drag & Drop und der Zwischenablage](dragdrop.md).

Windows-Explorer ruft [**IShellFolder:: deateviewobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) auf, wenn die gleiche Art von Informationen zum Ordner selbst benötigt wird.

### <a name="bindtoobject"></a>Bindjeobject

Windows-Explorer Ruft die [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) -Methode auf, wenn ein Benutzer versucht, einen der Unterordner ihrer Erweiterung zu öffnen. Wenn *riid* auf IID \_ IShellFolder festgelegt ist, sollten Sie ein Ordner Objekt, das den Unterordner darstellt, erstellen und initialisieren und die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Objekts zurückgeben.

> [!Note]  
> Zurzeit ruft Windows-Explorer diese Methode nur auf, um eine [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle anzufordern. Gehen Sie jedoch nicht davon aus, dass dies immer der Fall ist. Sie sollten den Wert von *riid* immer überprüfen, bevor Sie fortfahren.

 

### <a name="getdisplaynameof"></a>GetDisplayNameOf

Windows-Explorer Ruft die [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) -Methode auf, um die PIDL von einem der Objekte des Ordners in einen Namen zu konvertieren. Diese PIDL muss relativ zum übergeordneten Ordner des Objekts sein. Das heißt, es muss eine einzelne [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur aufweisen, die nicht **null** ist. Da es mehr als eine Möglichkeit gibt, Objekte zu benennen, gibt Windows-Explorer den Typ des Namens an, indem ein oder mehrere [**shgdnf**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf) -Flags im *uFlags* -Parameter festgelegt werden. Einer von zwei Werten, **shgdn \_ Normal** oder **shgdn \_ InFolder**, wird festgelegt, um anzugeben, ob der Name relativ zum Ordner oder relativ zum Desktop sein soll. Einer der anderen drei Werte: **shgdn \_ forediting**, **shgdn \_ foraddressbar** oder **shgdn \_ fortiersing** kann festgelegt werden, um anzugeben, wofür der Name verwendet werden soll.

Sie müssen den Namen in Form einer Struktur vom Typ " [**Strauch**](/windows/desktop/api/Shtypes/ns-shtypes-strret) " zurückgeben. Wenn die **shgdn- \_ Bearbeitung**, die **shgdn- \_ foraddressbar** und die **shgdn- \_ forenverarbeitung** nicht festgelegt sind, geben Sie den anzeigen amen des Objekts zurück. Wenn das Flag " **shgdn \_ forparamesing** " festgelegt ist, fordert Windows-Explorer einen Namen für die Unterzeichnung an. Analyse Namen werden an [**IShellFolder übergeben::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) , um die PIDL eines Objekts abzurufen, auch wenn Sie sich möglicherweise mindestens eine Ebene unterhalb des aktuellen Ordners in der Namespace Hierarchie befindet. Der namens Name eines Dateisystem Objekts ist beispielsweise der Pfad. Sie können den voll qualifizierten Pfad eines beliebigen Objekts im Dateisystem an die **IShellFolder::P arsedisplayname** -Methode des Desktops übergeben, und die voll qualifizierte PIDL des Objekts wird zurückgegeben.

Obwohl es sich bei den namens Namen um Text Zeichenfolgen handelt, müssen Sie den anzeigen Amen nicht unbedingt einschließen. Sie sollten Analyse Namen basierend auf dem, was effizient funktioniert, wenn [**IShellFolder::P armendisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) aufgerufen wird, zuweisen. Beispielsweise sind viele virtuelle Ordner der Shell nicht Teil des Dateisystems und verfügen nicht über einen voll qualifizierten Pfad. Stattdessen wird jedem Ordner eine GUID zugewiesen, und der namens Name hat folgendes Format:: {GUID}. Unabhängig davon, welches Schema Sie verwenden, sollte es in der Lage sein, eine zuverlässige "Roundtrip" zu erhalten. Wenn ein Aufrufer beispielsweise einen Analyse Namen an **IShellFolder::P arsedisplayname** übergibt, um die PIDL eines Objekts abzurufen, und diese PIDL an [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) übergibt, wobei das Flag für die **shgdn \_** -Enumeration festgelegt ist, sollte der Aufrufer den ursprünglichen Analyse Namen wiederherstellen.

### <a name="getattributesof"></a>Getattributesof

Windows-Explorer Ruft die [**IShellFolder:: getattributesof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) -Methode auf, um die Attribute von einem oder mehreren Elementen zu bestimmen, die in einem Ordner Objekt enthalten sind. Der Wert von *cidl* gibt die Anzahl der Elemente in der Abfrage an, und *apidl* verweist auf eine Liste Ihrer pidls.

Da das Testen einiger Attribute zeitaufwändig sein kann, schränkt Windows-Explorer die Abfrage in der Regel auf eine Teilmenge der verfügbaren Flags ein, indem ihre Werte in *rfginout* festgelegt werden. Ihre Methode sollte nur auf die Attribute testen, deren Flags in *rfginout* festgelegt sind. Lassen Sie die gültigen Flags festgelegt, und löschen Sie den Rest. Wenn mehr als ein Element in der Abfrage enthalten ist, legen Sie nur die Flags fest, die für alle Elemente gelten.

> [!Note]  
> Die Attribute müssen ordnungsgemäß festgelegt werden, damit ein Element ordnungsgemäß angezeigt wird. Wenn es sich bei einem Element beispielsweise um einen Ordner mit Unterordnern handelt, müssen Sie das **sfgao \_ hassubfolder** -Flag festlegen. Andernfalls zeigt Windows-Explorer in der Strukturansicht nicht neben dem Symbol des Elements ein Pluszeichen an.

 

### <a name="parsedisplayname"></a>Name des Parametern

Die [**IShellFolder::P arcdisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) -Methode ist in gewisser Hinsicht ein Spiegelbild von [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). Diese Methode wird am häufigsten verwendet, um den Namen des-Objekts in die zugeordnete PIDL zu konvertieren. Der namens Name kann auf jedes Objekt verweisen, das sich unterhalb des Ordners in der Namespace Hierarchie befindet. Die zurückgegebene PIDL ist relativ zum Ordner Objekt, das die Methode verfügbar macht und in der Regel nicht voll qualifiziert ist. Mit anderen Worten: Obwohl die PIDL mehrere [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Strukturen enthalten kann, ist der erste Wert der des Objekts selbst oder der erste Unterordner im Pfad vom Ordner zum Objekt. Der Aufrufer muss diese PIDL an die voll qualifizierte PIDL des Ordners anfügen, um eine voll qualifizierte PIDL für das Objekt zu erhalten.

[**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) kann auch aufgerufen werden, um die Attribute eines Objekts anzufordern. Da das Ermitteln aller anwendbaren Attribute zeitaufwändig sein kann, legt der Aufrufer nur die [**sfgao \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) -Flags fest, die Informationen darstellen, an denen der Aufrufer interessiert ist. Sie sollten bestimmen, welche dieser Attribute für das Objekt zutreffen, und die verbleibenden Flags löschen.

### <a name="ienumidlist-interface"></a>Ienumittellist-Schnittstelle

Wenn Windows Explorer die Objekte auflisten muss, die in einem Ordner enthalten sind, ruft er [**IShellFolder:: enumerationsobjekte**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects)auf. Das Folder-Objekt muss ein Enumerationsobjekt erstellen, das die [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) -Schnittstelle verfügbar macht und diesen Schnittstellen Zeiger zurückgibt. Der Windows-Explorer verwendet in der Regel **ienumittellist** , um die pidls aller im Ordner enthaltenen Objekte aufzulisten.

[**Ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) ist eine standardmäßige OLE-Enumerationsschnittstelle und wird auf die übliche Weise implementiert. Beachten Sie jedoch, dass die von Ihnen zurückgegebenen pidls relativ zum Ordner sein müssen und nur die [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur des Objekts und ein Abschluss Zeichen enthalten müssen.

## <a name="implementing-the-optional-interfaces"></a>Implementieren der optionalen Schnittstellen

Es gibt eine Reihe optionaler Shellschnittstellen, die von den Ordner Objekten der Erweiterung unterstützt werden können. Viele von Ihnen, wie z. b. [**iextracticon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona), ermöglichen es Ihnen, verschiedene Aspekte der Art und Weise anzupassen, in der der Benutzer die Erweiterung anzeigt. Andere, wie z. b. [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), ermöglichen es ihrer Erweiterung, Features wie Drag & Drop zu unterstützen.

Keine der optionalen Schnittstellen wird direkt von einem Ordner Objekt verfügbar gemacht. Stattdessen ruft Windows Explorer eine von zwei [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Methoden auf, um eine Schnittstelle anzufordern:

-   Windows-Explorer Ruft den [**IShellFolder:: getuiobjectof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) eines Ordner Objekts auf, um eine Schnittstelle für eines der im Ordner enthaltenen Objekte anzufordern.
-   Windows-Explorer Ruft das [**IShellFolder::**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) -Objekt eines Ordner Objekts auf, um eine Schnittstelle für den Ordner selbst anzufordern.

Um die Informationen bereitzustellen, erstellt das Ordner Objekt ein Objekt, das die angeforderte Schnittstelle verfügbar macht und den Schnittstellen Zeiger zurückgibt. Windows-Explorer ruft dann diese Schnittstelle auf, um die erforderlichen Informationen abzurufen. In diesem Abschnitt werden die am häufigsten verwendeten optionalen Schnittstellen erläutert.

### <a name="iextracticon"></a>Iextracticon

Windows-Explorer fordert eine [**iextracticon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) -Schnittstelle an, bevor der Inhalt eines Ordners angezeigt wird. Die-Schnittstelle ermöglicht der Erweiterung die Angabe benutzerdefinierter Symbole für die Objekte, die im Ordner enthalten sind. Andernfalls werden die standardmäßigen Datei-und Ordner Symbole verwendet. Um ein benutzerdefiniertes Symbol bereitzustellen, erstellen Sie ein Symbol Extraktions Objekt, das **iextracticon** verfügbar macht und einen Zeiger auf diese Schnittstelle zurückgibt. Weitere Informationen finden Sie in der Referenz Dokumentation zu **iextracticon** oder [Erstellen von Symbol Handlern](./how-to-create-icon-handlers.md).

### <a name="icontextmenu"></a>IContextMenu

Wenn ein Benutzer mit der rechten Maustaste auf ein Objekt klickt, fordert Windows Explorer eine [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstelle an. Um Kontextmenüs für die Objekte bereitzustellen, erstellen Sie ein menühandlerobjekt, und geben Sie seine **IContextMenu** -Schnittstelle zurück.

Die Prozeduren zum Erstellen eines menühandlerobjekts ähneln denen, die zum Erstellen einer menühandlershellerweiterung verwendet werden. Weitere Informationen finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md) oder der [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)-, [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)-oder [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) -Referenz.

### <a name="iqueryinfo"></a>Iqueryinfo

Windows Explorer Ruft die [**iqueryinfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) -Schnittstelle auf, um eine Infotipp-Text Zeichenfolge abzurufen.

### <a name="idataobject-and-idroptarget"></a>IDataObject und IDropTarget

Wenn Ihre Objekte von Windows Explorer angezeigt werden, kann ein Ordner Objekt nicht direkt erkennen, wenn ein Benutzer versucht, ein Objekt auszuschneiden, zu kopieren oder zu ziehen. Stattdessen fordert Windows Explorer eine [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle an. Um zuzulassen, dass das Objekt übertragen werden kann, erstellen Sie ein Datenobjekt und geben einen Zeiger auf seine **IDataObject** -Schnittstelle zurück.

Ebenso kann ein Benutzer versuchen, ein Datenobjekt in einer Windows Explorer-Darstellung eines ihrer Objekte zu löschen, z. b. als Symbol oder Adress leisten Pfad. Windows-Explorer fordert dann eine [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle an. Damit das Datenobjekt gelöscht werden kann, erstellen Sie ein Objekt, das eine **IDropTarget** -Schnittstelle verfügbar macht und den Schnittstellen Zeiger zurückgibt.

Die Verarbeitung von Datenübertragungen ist einer der schwierigeren Aspekte beim Schreiben von Namespace Erweiterungen. Eine ausführliche Erläuterung finden Sie unter [übertragen von shellobjekten mit Drag & Drop und der Zwischenablage](dragdrop.md).

## <a name="working-with-the-default-shell-folder-view-implementation"></a>Arbeiten mit der standardmäßigen Shell-Ordner Ansichts Implementierung

Datenquellen, die das standardmäßige shellordneransichtsobjekt (defview) verwenden, müssen diese Schnittstellen implementieren:

-   [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)
-   [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)
-   [**Ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)
-   [**IPersistFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)

Optional können Sie auch [**IPersistFolder3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3)implementieren.

 

 
