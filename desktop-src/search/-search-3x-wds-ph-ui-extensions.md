---
description: Um sicherzustellen, dass Ihre Daten während der Suche indiziert und dem Benutzer ordnungsgemäß angezeigt werden, müssen Sie shelldatenspeicher (auch als Shellnamespace Erweiterungen bezeichnet) und Dateityp Handler (auch als Shellerweiterungen, Erweiterungs Handler oder Shellerweiterungs Handler bezeichnet) implementieren.
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Hinzufügen von Symbolen, Vorschauen und Kontextmenüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525532"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a>Hinzufügen von Symbolen, Vorschauen und Kontextmenüs

Um sicherzustellen, dass Ihre Daten während der Suche indiziert und dem Benutzer ordnungsgemäß angezeigt werden, müssen Sie shelldatenspeicher (auch als [Shellnamespace Erweiterungen](../shell/nse-works.md)bezeichnet) und Dateityp Handler (auch als Shellerweiterungen, [Erweiterungs Handler](../shell/handlers.md)oder Shellerweiterungs Handler bezeichnet) implementieren.

In diesem Thema werden die folgenden Schnittstellen beschrieben:

-   [Implementieren von Dateityp Handlern](#implementing-file-type-handlers)
    -   [IPersist](#ipersist)
    -   [Ipersistfolder](#ipersistfolder)
    -   [IShellFolder](#ishellfolder)
    -   [IContextMenu](#icontextmenu)
    -   [Iextracticon](#iextracticon)
    -   [IPreviewHandler](#ipreviewhandler)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-file-type-handlers"></a>Implementieren von Dateityp Handlern

Diese Shellerweiterungen oder Dateityp Handler stellen den Benutzern die folgenden Shellfunktionen bereit:

-   Die Ergebnis Ansicht zeigt ein bestimmtes Symbol für den Elementtyp an.
-   In der Ergebnis Ansicht wird eine Vorschau des Elements angezeigt, wenn der Benutzer das Element auswählt.
-   Benutzer können auf Elemente doppelklicken, um Ereignisse wie das Öffnen der Datei zu initiieren.
-   Benutzer können mit der rechten Maustaste auf Elemente klicken, um auf ein Kontextmenü (Kontextmenü) zuzugreifen.
-   Benutzer können Elemente per Drag & amp; Drop verschieben.

Wie alle Component Object Model (com)-Objekte müssen Dateityp Handler eine [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle und eine Klassenfactory implementieren.

In Windows XP oder früheren Versionen sollten Handler außerdem Folgendes implementieren:

-   Beide [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   Oder [ishellextinit-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

In Windows Vista wurden die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) und die [ishellextinit-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) durch die folgenden drei Schnittstellen ersetzt, damit die Shell den Handler initialisieren kann:

-   [IInitializeWithStream-Schnittstelle](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [IInitializeWithItem-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IInitializeWithFile-Schnittstelle](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

Zum Bereitstellen eines angemessenen Benutzer Erlebnisses müssen Sie einen Shell-Datenspeicher mit Ihrem Protokollhandler bereitstellen. Der Datenspeicher dient dann als "Factory" für Symbol Handler, Verknüpfungen von Menü Handlern, Vorschau Handlern usw. Für die [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)sind minimale Implementierungen der [ipersistent-Schnitt](/windows/desktop/api/objidl/nn-objidl-ipersist) Stelle und die [ipersistfolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) -Schnittstelle erforderlich, und eine minimale Implementierung der IShellFolder-Schnittstelle ist für " [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) " und " [iextracticon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)" erforderlich.

> [!Note]  
> Der gleiche Klassen Bezeichner (CLSID) sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.

 

Weitere Informationen zum Erstellen eines Shell-Datenspeicher zur Unterstützung eines Protokoll Handlers finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="ipersist"></a>IPersist

Die **ipersistent** -Schnittstelle definiert die einzelne **GetClassID-** Methode, die für die Bereitstellung der CLSID eines Objekts konzipiert ist, das im System dauerhaft gespeichert werden kann.



| Methode     | BESCHREIBUNG                                      |
|------------|--------------------------------------------------|
| GetClassID | Gibt die CLSID des shelldatenspeicher-Objekts zurück. |



 

### <a name="ipersistfolder"></a>Ipersistfolder

Die **ipersistfolder** -Schnittstelle wird verwendet, um Shellordner Objekte zu initialisieren. Die Implementierung dieser Schnittstelle, die von **ipersistent** abgeleitet wird, ist die Art und Weise, wie der Ordner im Shellnamespace informiert wird. Sie verwenden diese Schnittstelle nicht direkt. Sie wird von der Dateisystem Implementierung der [IShellFolder:: BindTo Object-Methode](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) verwendet, wenn ein shellordnerobjekt initialisiert wird.



| Methode     | BESCHREIBUNG                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| Initialisieren | Weist ein shellordnerobjekt an, sich auf der Grundlage der bestandenen Informationen selbst zu initialisieren, und gibt S OK zurück. \_ |



 

### <a name="ishellfolder"></a>IShellFolder

Die [IShellFolder-Schnittstellen](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Schnittstelle wird zum Verwalten von Ordnern verwendet, und eine partielle Implementierung ist erforderlich, damit die Symbol-und Kontext Schnittstellen, die für einen Protokollhandler implementiert werden, in der Benutzeroberfläche der Windows-Suchergebnisse ordnungsgemäß Verhalten. Der größte Teil der erforderlichen Funktionalität wird durch die **getuiobjectof** -Methode verfügbar gemacht. Diese Methode ermöglicht es einem Add-in, die **iextracticon** -Schnittstelle und die **IContextMenu** -Schnittstelle abzufragen.

Die [IShellFolder-Schnittstellen](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Schnittstelle verwendet pidls anstelle von URLs. Im Gegensatz zu den Anforderungen eines kompletten Shell-Datenspeicher kann für Add-Ins eine einfache IDL-Struktur verwendet werden, die nur die URL enthält.

Die folgenden Methoden der [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) müssen implementiert werden. Fünf dieser Methoden erfordern eine minimale Implementierung.



| Methode           | BESCHREIBUNG                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bindjeobject     | Gibt E \_ notimpl zurück.                                                                                                                                                                                                                                                            |
| Bindungsspeicher    | Gibt E \_ notimpl zurück.                                                                                                                                                                                                                                                            |
| "Ansichts Objekt" | Gibt E \_ notimpl zurück.                                                                                                                                                                                                                                                            |
| Setnameof        | Gibt E \_ notimpl zurück.                                                                                                                                                                                                                                                            |
| Name des Parametern | Konvertiert eine URL in die PIDL-Struktur.                                                                                                                                                                                                                                          |
| Compareids       | Vergleicht zwei PIDL-Werte.                                                                                                                                                                                                                                                      |
| GetDisplayNameOf | Gibt die URL für eine PIDL zurück.                                                                                                                                                                                                                                                    |
| Getuiobjectof    | Diese Methode ähnelt der [IUnknown:: QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Wenn ein Symbol angefordert wird, fordert der Aufrufer die IID \_ iextracticon an. Wenn ein Kontextmenü angefordert wird, fordert der Aufrufer das IID \_ IContextMenu an. |



 

**IShellFolder** wird nicht zum Auflisten von Ordnern verwendet. Dies bedeutet, dass der Anzeige Name eines Ordners die physische URL ist. Dies kann sich in Zukunft ändern.

### <a name="icontextmenu"></a>IContextMenu

Wenn die Windows-Suche Ergebnisse für den Benutzer anzeigt, kann der Benutzer mit der rechten Maustaste auf ein Element klicken und ein Kontextmenü sehen, das von der **IContextMenu** -Schnittstelle definiert wird. Kontextmenüs werden auch als Kontextmenüs bezeichnet.

Die Standardaktion im Kontextmenü ist dieselbe Aktion, die ausgeführt wird, wenn auf das Element Doppel geklickt wird. Ohne die entsprechenden **IShellFolder** -oder **IContextMenu** -Schnittstellen für das Element besteht das Standardverhalten eines Doppelklick Ereignisses darin, die URL als Argument an die [ShellExecute-Funktions](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) Funktion zu übergeben.

Weitere Informationen zum Erstellen von Kontextmenü Handlern finden Sie unter [Erstellen von Kontextmenü](../shell/context-menu-handlers.md) Handlern und [Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md) für Beispielcode.

### <a name="iextracticon"></a>Iextracticon

**Iextracticon** Ruft ein Symbol für die Windows Search-Benutzeroberfläche basierend auf der URL in der PIDL ab, die von Ihrem Protokollhandler bereitgestellt wird.

Weitere Informationen zum Erstellen von Symbol Handlern finden Sie unter [Erstellen von Symbol Handlern](../shell/how-to-create-icon-handlers.md) und [Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md) für Beispielcode.

### <a name="ipreviewhandler"></a>IPreviewHandler

[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) rendert eine umfangreiche Vorschauversion eines ausgewählten Elements in Windows-Explorer. Vorschau Versionen sind in Windows Search 4,0 oder Windows Vista mit der Windows-Desktop Suche 3. x verfügbar.

So erstellen Sie einen benutzerdefinierten Vorschau Handler:

1.  Implementieren Sie einen [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) , der einen [IStream](/windows/win32/api/objidl/nn-objidl-istream)annimmt, und befolgen Sie die Richtlinien, die in [Vorschau Handlern](../shell/preview-handlers.md)bereitgestellt werden.
2.  Registrieren Sie Ihren Vorschau Handler:

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  Führen Sie die folgenden beiden Schritte aus, um einen Shellordner für Ihre URL zu implementieren:
    1.  Behandeln Sie [iqueryassociation](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) in der [IShellFolder:: getuiobjectof-Methode](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), und geben Sie Ihre Zuordnung für Ihre shellelemente zurück, wie im folgenden Codebeispiel gezeigt.

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  Nachdem die Shell den Shellordner abgefragt hat, damit der Datenstrom den Vorschau Handler initialisiert, navigieren Sie zu Ihrer [IShellFolder:: BindToObject-Methoden](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) Methode, behandeln IID \_ IStream und geben einen [IStream](/windows/win32/api/objidl/nn-objidl-istream) an Ihre URL zurück.

Um einen vorhandenen Vorschau Handler für den Dateityp wiederzuverwenden, führen Sie die folgenden beiden Schritte aus:

1.  Registrieren Sie diesen Vorschau Handler für Ihren Dateityp mithilfe der CLSID des vorhandenen Vorschau Handlers anstelle <Ihrer \_ PreviewHandler- \_ GUID>.
2.  Implementieren Sie einen Shellordner.

Weitere Informationen zum Erstellen von Vorschau Handlern finden Sie unter [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) -und [Vorschau Handler](../shell/preview-handlers.md).

## <a name="additional-resources"></a>Weitere Ressourcen

-   Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
-   Weitere Informationen zum Erstellen von Handlern finden Sie unter [Registrieren von Shellerweiterungen](../shell/reg-shell-exts.md), [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md), [Kontextmenü](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell-Namespace Erweiterungen](../shell/nse-works.md) und [Vorschau Handler](../shell/preview-handlers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Grundlegendes zu Protokoll Handlern](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Code Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Erstellen eines Suchconnector für einen Protokoll Handler](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debuggen von Protokoll Handlern](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
