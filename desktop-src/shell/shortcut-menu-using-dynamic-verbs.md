---
description: Kontextmenü Handler werden auch als Kontextmenü Handler oder Verb Handler bezeichnet. Ein Kontextmenü Handler ist ein Typ eines Dateityp Handlers.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Anpassen eines Kontextmenüs mithilfe dynamischer Verben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980184"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Anpassen eines Kontextmenüs mithilfe dynamischer Verben

Kontextmenü Handler werden auch als Kontextmenü Handler oder Verb Handler bezeichnet. Ein Kontextmenü Handler ist ein Typ eines Dateityp Handlers.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu statischen und dynamischen Verben](#about-static-and-dynamic-verbs)
-   [Funktionsweise von Kontextmenü Handlern mit dynamischen Verben](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Vermeiden von Kollisionen aufgrund von nicht qualifizierten Verb Namen](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Registrieren eines Kontextmenü Handlers mit einem dynamischen Verb](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implementieren der IContextMenu-Schnittstelle](#implementing-the-icontextmenu-interface)
    -   [IContextMenu:: getcommandstring-Methode](#icontextmenugetcommandstring-method)
    -   [IContextMenu:: InvokeCommand-Methode](#icontextmenuinvokecommand-method)
    -   [IContextMenu:: querycontextmenu-Methode](#icontextmenuquerycontextmenu-method)
-   [Zugehörige Themen](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>Informationen zu statischen und dynamischen Verben

Wir empfehlen Ihnen dringend, ein Kontextmenü mit einer der statischen Verb-Methoden zu implementieren. Es wird empfohlen, die Anweisungen im Abschnitt "Anpassen eines Kontextmenüs mit statischen Verben" unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md)zu befolgen. Informationen zum dynamischen Verhalten von statischen Verben in Windows 7 und höher finden Sie unter "Get Dynamic Behavior for static Verbs" unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md). Ausführliche Informationen über die statische Verb-Implementierung und welche dynamischen Verben zu vermeiden sind, finden [Sie unter Auswählen eines statischen oder dynamischen Verbs für](shortcut-choose-method.md)das Kontextmenü.

Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie für den Dateityp ein dynamisches Verb registrieren, befolgen Sie die Anweisungen weiter unten in diesem Thema.

> [!Note]  
> Beim Registrieren von Handlern, die im Kontext von 32-Bit-Anwendungen funktionieren, gibt es spezielle Überlegungen für 64-Bit-Windows: Wenn Shellverben im Kontext einer 32-Bit-Anwendung aufgerufen werden, leitet das WOW64-Subsystem den Dateisystem Zugriff auf einige Pfade um. Wenn der exe-Handler in einem dieser Pfade gespeichert ist, kann in diesem Kontext nicht darauf zugegriffen werden. Als Problem Umgehung speichern Sie die exe-Datei in einem Pfad, der nicht umgeleitet wird, oder speichern Sie eine Stubversion der exe-Datei, die die tatsächliche Version gestartet hat.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Funktionsweise von Kontextmenü Handlern mit dynamischen Verben

Neben [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)exportieren Kontextmenü Handler die folgenden zusätzlichen Schnittstellen, um das Messaging zu verarbeiten, das zum Implementieren von vom Besitzer gezeichneten Menü Elementen erforderlich ist:

-   [**Ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatorisch)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatorisch)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)

Weitere Informationen zu Menü Elementen, die vom Besitzer gezeichnet werden, finden Sie im Abschnitt *Erstellen von Owner-Drawn Menü Elemente* in [Verwenden von Menüs](../menurc/using-menus.md).

Shell verwendet die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle zum Initialisieren des Handlers. Wenn die Shell [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)aufruft, übergibt Sie ein Datenobjekt mit dem Namen des Objekts und einem Zeiger auf eine Element Bezeichner-Liste (PIDL) des Ordners, der die Datei enthält. Der *hkeyprogid* -Parameter ist der Registrierungs Speicherort, unter dem das Handle des Kontextmenüs registriert wird. Die **ishellextinit:: Initialize** -Methode muss den Dateinamen aus dem Datenobjekt extrahieren und den Namen und den Zeiger des Ordners für die spätere Verwendung auf eine Element Bezeichner Liste (PIDL) speichern. Weitere Informationen zur Initialisierung von Handlern finden Sie unter [Implementieren von ishellextinit](handlers.md).

Wenn Verben in einem Kontextmenü angezeigt werden, werden Sie zuerst erkannt, dann dem Benutzer präsentiert und schließlich aufgerufen. In der folgenden Liste werden diese drei Schritte ausführlicher beschrieben:

1.  Die Shell ruft [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)auf, das eine Gruppe von Verben zurückgibt, die auf dem Zustand der Elemente oder des Systems basieren können.
2.  Das System übergibt ein **HMENU** -handle, das von der-Methode zum Hinzufügen von Elementen zum Kontextmenü verwendet werden kann.
3.  Wenn der Benutzer auf eines der Elemente des Handlers klickt, ruft die Shell [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)auf. Der Handler kann dann den entsprechenden Befehl ausführen.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Vermeiden von Kollisionen aufgrund von nicht qualifizierten Verb Namen

Da Verben pro Typ registriert sind, kann der gleiche Verb Name für Verben auf unterschiedlichen Elementen verwendet werden. Dies ermöglicht es Anwendungen, auf allgemeine Verben unabhängig vom Elementtyp zu verweisen. Diese Funktion ist zwar nützlich, aber die Verwendung von nicht qualifizierten Namen kann zu Konflikten mit mehreren unabhängigen Softwareanbietern (ISVs) führen, die denselben Verb Namen auswählen. Um dies zu vermeiden, stellen Sie immer wie folgt Verben mit dem ISV-Namen vor:

`ISV_Name.verb`

Verwenden Sie immer eine anwendungsspezifische ProgID. Durch die Übernahme der Konvention zum Mapping der Dateinamenerweiterung zu einem von ISV bereitgestellten ProgID werden potenzielle Konflikte vermieden. Da jedoch einige Elementtypen diese Zuordnung nicht verwenden, ist es erforderlich, dass Hersteller eindeutige Namen besitzen. Beim Hinzufügen eines Verbs zu einer vorhandenen ProgID, bei der das Verb möglicherweise bereits registriert ist, müssen Sie zuerst den Registrierungsschlüssel für das alte Verb entfernen, bevor Sie Ihr eigenes Verb hinzufügen. Sie müssen dies tun, um zu vermeiden, dass die Verb Informationen aus den beiden Verben zusammengeführt werden. Wenn dies nicht der Fall ist, führt dies zu unvorhersehbarem Verhalten.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Registrieren eines Kontextmenü Handlers mit einem dynamischen Verb

Kontextmenü Handler sind entweder einem Dateityp oder einem Ordner zugeordnet. Bei Dateitypen wird der Handler unter dem folgenden Unterschlüssel registriert.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Um einen Kontextmenü Handler entweder einem Dateityp oder einem Ordner zuzuordnen, erstellen Sie zunächst unter dem Unterschlüssel **ContextMenuHandlers** einen Unterschlüssel. Benennen Sie den Unterschlüssel für den Handler, und legen Sie den Standardwert des unter Schlüssels auf das Zeichen folgen Format der CLSID-GUID (Class Identifier) des Handlers fest.

Wenn Sie dann einem Kontextmenü Handler verschiedene Arten von Ordnern zuordnen möchten, registrieren Sie den Handler auf die gleiche Weise wie für einen Dateityp, aber unter dem *foldertype* -Unterschlüssel, wie im folgenden Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Weitere Informationen zu den Ordner Typen, für die Sie Handler registrieren können, finden Sie unter [Registrieren von Shellerweiterungs Handlern](handlers.md).

Wenn einem Dateityp ein Kontextmenü zugeordnet ist, wird durch Doppelklicken auf ein Objekt normalerweise der Standardbefehl gestartet, und die [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Methode des Handlers wird nicht aufgerufen. Um anzugeben, dass die **IContextMenu:: querycontextmenu** -Methode des Handlers aufgerufen werden soll, wenn auf ein Objekt Doppel geklickt wird, erstellen Sie einen Unterschlüssel unter dem **CLSID** -Unterschlüssel des Handlers, wie hier gezeigt.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Wenn ein Objekt, das dem Handler zugeordnet ist, doppelt geklickt wird, wird [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) mit dem **CMF-Flag \_ DefaultOnly** aufgerufen, das im *uFlags* -Parameter festgelegt ist.

Mit Kontextmenü Handlern sollte der Unterschlüssel " **maychangedefaultmenu** " nur dann festgelegt werden, wenn Sie möglicherweise das Standard Verb des Kontextmenüs ändern müssen. Das Festlegen dieses unter Schlüssels zwingt das Laden der DLL-Datei des Handlers, wenn auf ein zugeordnetes Element Doppel geklickt wird. Wenn Ihr Handler das Standardverb nicht ändert, sollten Sie diesen Unterschlüssel nicht festlegen, da dies dazu führt, dass das System die dll unnötig lädt.

Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Kontextmenü Handler für einen MYP-Dateityp aktivieren. Der **CLSID** -Unterschlüssel des Handlers enthält einen **maychangedefaultmenu** -Unterschlüssel, um sicherzustellen, dass der Handler aufgerufen wird, wenn der Benutzer auf ein verknüpftes Objekt doppelklickt.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a>Implementieren der IContextMenu-Schnittstelle

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Methode, die implementiert werden kann. Es wird dringend empfohlen, dass Sie ein Verb mithilfe einer der statischen Verb-Methoden implementieren. Weitere Informationen finden Sie unter [Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) verfügt über drei Methoden: **getcommandstring**, **InvokeCommand** und **querycontextmenu**, die hier ausführlich erläutert werden.

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu:: getcommandstring-Methode

Die [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) -Methode des Handlers wird verwendet, um den kanonischen Namen eines Verbs zurückzugeben. Diese Methode ist optional. In Windows XP und früheren Versionen von Windows wird diese Methode verwendet, um den Hilfetext abzurufen, der in der Statusleiste für ein Menü Element angezeigt wird, wenn Windows-Explorer über eine Status Leiste verfügt.

Der *idcmd* -Parameter enthält den bezeichneroffset des Befehls, der beim [**Aufrufen von IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) definiert wurde. Wenn eine Hilfe Zeichenfolge angefordert wird, wird *uFlags* auf **GCS \_ helptextw** festgelegt. Kopieren Sie die Hilfe Zeichenfolge in den *pszName* -Puffer, und wandeln Sie Sie in ein **pwstr** um. Die Verb Zeichenfolge wird angefordert, indem *uFlags* auf **GCS- \_ verbw** festgelegt wird. Kopieren Sie die entsprechende Zeichenfolge wie bei der Hilfe Zeichenfolge in *pszName*. Die **\_ validatew** -Flags für **GCS \_ validatea** und GCS werden von Kontextmenü Handlern nicht verwendet.

Im folgenden Beispiel wird eine einfache Implementierung von [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) veranschaulicht, die dem im Abschnitt [IContextMenu:: querycontextmenu-Methode](#icontextmenuquerycontextmenu-method) in diesem Thema angegebenen [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Beispiel entspricht. Da der Handler nur ein Menü Element hinzufügt, gibt es nur einen Satz von Zeichen folgen, die zurückgegeben werden können. Die-Methode testet, ob *idcmd* gültig ist, und gibt, wenn dies der Fall ist, die angeforderte Zeichenfolge zurück.

Die [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) -Funktion wird verwendet, um die angeforderte Zeichenfolge nach *pszName* zu kopieren, um sicherzustellen, dass die kopierte Zeichenfolge die Größe des durch *cchName* angegebenen Puffers nicht überschreitet. In diesem Beispiel wird nur die Unterstützung für die Unicode-Werte von *uFlags* implementiert, da nur diese seit Windows 2000 in Windows-Explorer verwendet wurden.


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a>IContextMenu:: InvokeCommand-Methode

Diese Methode wird aufgerufen, wenn ein Benutzer auf ein Menü Element klickt, um den Handler anzuweisen, den zugehörigen Befehl auszuführen. Der *pici* -Parameter verweist auf eine-Struktur, die die erforderlichen Informationen enthält.

Obwohl *pici* in shlobj. h als [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) -Struktur deklariert ist, verweist es in der Praxis häufig auf eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur. Diese Struktur ist eine erweiterte Version von **cminvokecommandinfo** und verfügt über mehrere zusätzliche Member, die es ermöglichen, Unicode-Zeichen folgen zu übergeben.

Überprüfen Sie das **CBSIZE** -Member von *pici* , um zu bestimmen, welche Struktur übergeben wurde. Wenn es sich um eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur handelt und für den **fmask** -Member das **CMIC \_ mask- \_ Unicode** -Flag festgelegt ist, wandeln Sie *pici* in **cminvokecommandinfoex** um. Dadurch kann Ihre Anwendung die Unicode-Informationen verwenden, die in den letzten fünf Membern der Struktur enthalten sind.

Der **lpverb** -oder **lpverbw** -Member der Struktur wird verwendet, um den auszuführenden Befehl zu identifizieren. Befehle werden auf eine der beiden folgenden Arten identifiziert:

-   Durch die Verb Zeichenfolge des Befehls
-   Nach dem bezeichneroffset des Befehls

Um zwischen diesen beiden Fällen zu unterscheiden, überprüfen Sie das höchst wertige Wort **lpverb** für die ANSI-Groß-/Kleinschreibung oder **lpverbw** für den Unicode-Fall. Wenn das hochwertige Wort nicht NULL ist, enthält **lpverb** oder **lpverbw** eine Verb Zeichenfolge. Wenn das hochwertige Wort 0 (null) ist, befindet sich der Befehls Offset im nieder wertigen Wort **lpverb**.

Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , die den Beispielen " [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) " und " [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) " entspricht, die vor und nach diesem Abschnitt angegeben werden. Die-Methode bestimmt zunächst, welche Struktur an Sie übermittelt wird. Anschließend bestimmt er, ob der Befehl durch seinen Offset oder sein Verb gekennzeichnet wird. Wenn **lpverb** oder **lpverbw** ein gültiges Verb oder einen gültigen Offset enthält, zeigt die Methode ein Meldungs Feld an.


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a>IContextMenu:: querycontextmenu-Methode

Die Shell ruft [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) auf, damit der Kontextmenü Handler dem Menü die Menü Elemente hinzufügen kann. Sie übergibt den **HMENU** -Handle im *HMENU* -Parameter. Der *indexmenu* -Parameter wird auf den Index festgelegt, der für das erste hinzu zufügende Menü Element verwendet werden soll.

Alle vom Handler hinzugefügten Menü Elemente müssen über Bezeichner verfügen, die zwischen den Werten in den Parametern *idcmdfirst* und *idcmdlast* liegen. In der Regel wird der erste Befehls Bezeichner auf *idcmdfirst* festgelegt, der für jeden zusätzlichen Befehl um eins (1) erhöht wird. Mit dieser Vorgehensweise können Sie die Überschreitung von *idcmdlast* vermeiden und die Anzahl der verfügbaren Bezeichner maximieren, falls die Shell mehr als einen Handler aufruft.

Der *Befehls Offset* eines Element Bezeichners ist der Unterschied zwischen dem Bezeichner und dem Wert in *idcmdfirst*. Speichern Sie den Offset der einzelnen Elemente, die der Handler dem Kontextmenü hinzufügt, da die Shell ihn möglicherweise zum Identifizieren des Elements verwendet, wenn es anschließend [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) oder [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)aufruft.

Sie sollten jedem Befehl, den Sie hinzufügen, auch ein [Verb](launch.md) zuweisen. Ein Verb ist eine Zeichenfolge, die anstelle des Offsets verwendet werden kann, um den Befehl zu identifizieren, wenn [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird. Sie wird auch von Funktionen wie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Ausführen von Kontextmenü Befehlen verwendet.

Es gibt drei Flags, die über den *uFlags* -Parameter übergeben werden können, die für Kontextmenü Handler relevant sind. Diese werden in der folgenden Tabelle beschrieben.



| Flag             | Beschreibung                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DefaultOnly | Der Benutzer hat den Standardbefehl ausgewählt, in der Regel durch Doppelklicken auf das Objekt. [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) sollte die Steuerung an die Shell zurückgeben, ohne das Menü zu ändern. |
| CMF- \_ NODEFAULT   | Kein Element im Menü sollte das Standardelement sein. Die-Methode sollte Ihre Befehle dem Menü hinzufügen.                                                                                                                          |
| CMF \_ Normal      | Das Kontextmenü wird normal angezeigt. Die-Methode sollte Ihre Befehle dem Menü hinzufügen.                                                                                                                            |



 

Verwenden Sie entweder [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) oder [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) , um der Liste Menü Elemente hinzuzufügen. Geben Sie anschließend einen **HRESULT** -Wert mit dem schwere **Grad \_ Success** an. Legen Sie den Codewert auf den Offset des größten Befehls Bezeichners fest, der zugewiesen wurde, plus eins (1). Nehmen Sie beispielsweise an, dass *idcmdfirst* auf 5 festgelegt ist und Sie dem Menü drei Elemente mit den Befehls bezeichlern 5, 7 und 8 hinzufügen. Der Rückgabewert muss sein `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .

Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , mit der ein einzelner Befehl eingefügt wird. Der bezeichneroffset für den Befehl ist die IDM- \_ Anzeige, die auf 0 (null) festgelegt ist. Die Variablen **m \_ pszverb** und **m \_ pwszverb** sind private Variablen, die zum Speichern der zugeordneten sprachunabhängigen Verb Zeichenfolge im ANSI-und Unicode-Format verwendet werden.


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



Informationen zu anderen Verb Implementierungsaufgaben finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontextmenüs und Kontextmenü Handler](context-menu.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben](verbs-best-practices.md)
</dt> <dt>

[Erstellen von Kontextmenü Handlern](context-menu-handlers.md)
</dt> <dt>

[Verweis auf das Kontextmenü](context-menu-reference.md)
</dt> </dl>

 

 
