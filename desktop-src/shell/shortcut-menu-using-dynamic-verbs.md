---
description: Kontextmenühandler werden auch als Kontextmenühandler oder Verbhandler bezeichnet. Ein Kontextmenühandler ist ein Typ von Dateityphandler.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Anpassen eines Kontextmenüs mit dynamischen Verben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b33361be5a89480e05bb42bd760b63517bf0b06c9828cae36a36ecddce1e9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968309"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Anpassen eines Kontextmenüs mit dynamischen Verben

Kontextmenühandler werden auch als Kontextmenühandler oder Verbhandler bezeichnet. Ein Kontextmenühandler ist ein Typ von Dateityphandler.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu statischen und dynamischen Verben](#about-static-and-dynamic-verbs)
-   [Funktionsweise von Kontextmenühandlern mit dynamischen Verben](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Vermeiden von Kollisionen aufgrund von nicht qualifizierten Verbnamen](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Registrieren eines Kontextmenühandlers mit einem dynamischen Verb](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implementieren der IContextMenu-Schnittstelle](#implementing-the-icontextmenu-interface)
    -   [IContextMenu::GetCommandString-Methode](#icontextmenugetcommandstring-method)
    -   [IContextMenu::InvokeCommand-Methode](#icontextmenuinvokecommand-method)
    -   [IContextMenu::QueryContextMenu-Methode](#icontextmenuquerycontextmenu-method)
-   [Zugehörige Themen](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>Informationen zu statischen und dynamischen Verben

Es wird dringend empfohlen, ein Kontextmenü mit einer der statischen Verbmethoden zu implementieren. Es wird empfohlen, die Anweisungen im Abschnitt "Anpassen eines Kontextmenüs mit statischen Verben" unter Erstellen von [Kontextmenühandlern zu befolgen.](context-menu-handlers.md) Informationen zum Abrufen des dynamischen Verhaltens für statische Verben in Windows 7 und höher finden Sie unter "Getting Dynamic Behavior for Static Verbs" (Abrufen des dynamischen Verhaltens für statische Verben) in Creating Context Menu Handlers (Erstellen [von Kontextmenühandlern).](context-menu-handlers.md) Ausführliche Informationen zur Implementierung statischer Verben und zu den zu vermeidenden dynamischen Verben finden Sie unter Auswählen eines statischen oder dynamischen [Verbs für das Kontextmenü.](shortcut-choose-method.md)

Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie ein dynamisches Verb für den Dateityp registrieren, befolgen Sie die Anweisungen weiter unten in diesem Thema.

> [!Note]  
> Beim Registrieren von Handlern, die im Kontext von 32-Bit-Anwendungen funktionieren, gibt es besondere Überlegungen für 64-Bit-Windows: Wenn Shell-Verben im Kontext einer 32-Bit-Anwendung aufgerufen werden, leitet das WOW64-Subsystem den Dateisystemzugriff auf einige Pfade um. Wenn ihr .exe-Handler in einem dieser Pfade gespeichert ist, kann in diesem Kontext nicht darauf zugegriffen werden. Speichern Sie daher ihre .exe entweder in einem Pfad, der nicht umgeleitet wird, oder speichern Sie eine Stubversion Ihrer .exe, die die echte Version startet.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Funktionsweise von Kontextmenühandlern mit dynamischen Verben

Neben [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)exportieren Kontextmenühandler die folgenden zusätzlichen Schnittstellen, um das Messaging zu verarbeiten, das zum Implementieren von vom Besitzer gezeichneten Menüelementen erforderlich ist:

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatorisch)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatorisch)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)

Weitere Informationen zu vom Besitzer gezeichneten Menüelementen finden Sie im Abschnitt Erstellen Owner-Drawn *Menüelemente* unter [Verwenden von Menüs.](../menurc/using-menus.md)

Shell verwendet die [**IShellExtInit-Schnittstelle,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) um den Handler zu initialisieren. Wenn die Shell [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)aufruft, übergibt sie ein Datenobjekt mit dem Namen des Objekts und einen Zeiger auf eine Elementbezeichnerliste (PIDL) des Ordners, der die Datei enthält. Der *hkeyProgID-Parameter* ist der Registrierungsspeicherort, unter dem das Kontextmenühandle registriert wird. Die **IShellExtInit::Initialize-Methode** muss den Dateinamen aus dem Datenobjekt extrahieren und den Namen und den Zeiger des Ordners auf eine Elementbezeichnerliste (PIDL) zur späteren Verwendung speichern. Weitere Informationen zur Handlerin initialisierung finden Sie unter [Implementing IShellExtInit ( Implementieren von IShellExtInit](handlers.md)).

Wenn Verben in einem Kontextmenü angezeigt werden, werden sie zuerst entdeckt, dann dem Benutzer angezeigt und schließlich aufgerufen. In der folgenden Liste werden diese drei Schritte ausführlicher beschrieben:

1.  Die Shell ruft [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)auf, die einen Satz von Verben zurückgibt, die auf dem Zustand der Elemente oder des Systems basieren können.
2.  Das System übergibt ein **HMENU-Handle,** mit dem die Methode Dem Kontextmenü Elemente hinzufügen kann.
3.  Wenn der Benutzer auf eines der Elemente des Handlers klickt, ruft die Shell [**IContextMenu::InvokeCommand auf.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) Der Handler kann dann den entsprechenden Befehl ausführen.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Vermeiden von Kollisionen aufgrund von nicht qualifizierten Verbnamen

Da Verben pro Typ registriert werden, kann derselbe Verbname für Verben für verschiedene Elemente verwendet werden. Dadurch können Anwendungen unabhängig vom Elementtyp auf allgemeine Verben verweisen. Diese Funktionalität ist zwar nützlich, aber die Verwendung von nicht qualifizierten Namen kann zu Kollisionen mit mehreren unabhängigen Softwareherstellern (INDEPENDENT Software Vendors, ISVs) führen, die denselben Verbnamen auswählen. Um dies zu vermeiden, stellen Sie Verben immer den ISV-Namen wie folgt voran:

`ISV_Name.verb`

Verwenden Sie immer eine anwendungsspezifische ProgID. Durch die Übernahme der Konvention zum Zuordnen der Dateinamenerweiterung zu einem isv bereitgestellten ProgID werden potenzielle Kollisionen vermieden. Da einige Elementtypen diese Zuordnung jedoch nicht verwenden, ist es notwendig, herstellerspezifische Namen zu verwenden. Beim Hinzufügen eines Verbs zu einer vorhandenen ProgID, bei der dieses Verb möglicherweise bereits registriert ist, müssen Sie zuerst den Registrierungsschlüssel für das alte Verb entfernen, bevor Sie Ihr eigenes Verb hinzufügen. Sie müssen dies tun, um zu vermeiden, dass die Verbinformationen aus den beiden Verben zusammengeführt werden. Anderst führt dies zu unvorhersehbarem Verhalten.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Registrieren eines Kontextmenühandlers mit einem dynamischen Verb

Kontextmenühandler sind entweder einem Dateityp oder einem Ordner zugeordnet. Bei Dateitypen wird der Handler unter dem folgenden Unterschlüssel registriert.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Um einen Kontextmenühandler entweder einem Dateityp oder einem Ordner zu zuordnen, erstellen Sie zunächst einen Unterschlüssel unter dem **Unterschlüssel ContextMenuHandlers.** Benennen Sie den Unterschlüssel für den Handler, und legen Sie den Standardwert des Unterschlüssels auf die Zeichenfolgenform der Klassenbezeichner-GUID (CLSID) des Handlers fest.

Um dann einen Kontextmenühandler verschiedenen Arten von Ordnern zu zuordnen, registrieren Sie den Handler auf die gleiche Weise wie für einen Dateityp, aber unter dem *Unterschlüssel FolderType,* wie im folgenden Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Weitere Informationen dazu, für welche Ordnertypen Sie Handler registrieren können, finden Sie unter [Registrieren von Shell-Erweiterungshandlern.](handlers.md)

Wenn einem Dateityp ein Kontextmenü zugeordnet ist, wird durch Doppelklicken auf ein Objekt normalerweise der Standardbefehl gestartet, und die [**IContextMenu::QueryContextMenu-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) des Handlers wird nicht aufgerufen. Um anzugeben, dass die **IContextMenu::QueryContextMenu-Methode** des Handlers aufgerufen werden soll, wenn auf ein Objekt doppelklickt, erstellen Sie einen Unterschlüssel unter dem CLSID-Unterschlüssel des **Handlers,** wie hier gezeigt.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Wenn auf ein Objekt, das dem Handler zugeordnet ist, doppelt geklickt wird, wird [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) aufgerufen, und das **\_ CMF-Flag DEFAULTONLY** wird im *uFlags-Parameter* festgelegt.

Kontextmenühandler sollten den **Unterschlüssel MayChangeDefaultMenu** nur festlegen, wenn sie möglicherweise das Standardverb des Kontextmenüs ändern müssen. Das Festlegen dieses Unterschlüssels zwingt das System, die DLL des Handlers zu laden, wenn auf ein zugeordnetes Element doppelklickt. Wenn ihr Handler das Standardverb nicht ändert, sollten Sie diesen Unterschlüssel nicht festlegen, da dies dazu führt, dass das System die DLL unnötigerweise geladen.

Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Kontextmenühandler für einen .myp-Dateityp aktivieren. Der **CLSID-Unterschlüssel** des Handlers enthält einen **MayChangeDefaultMenu-Unterschlüssel,** um zu gewährleisten, dass der Handler aufgerufen wird, wenn der Benutzer auf ein verknüpftes Objekt doppelklickt.

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

[**IContextMenu ist**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) die leistungsfähigste, aber auch die komplizierteste Zu implementierende Methode. Es wird dringend empfohlen, ein Verb mithilfe einer der statischen Verbmethoden zu implementieren. Weitere Informationen finden Sie unter Auswählen eines statischen oder [dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md). [**IContextMenu verfügt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) über drei Methoden, **GetCommandString,** **InvokeCommand** und **QueryContextMenu,** die hier ausführlich erläutert werden.

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu::GetCommandString-Methode

Die [**IContextMenu::GetCommandString-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) des Handlers wird verwendet, um den kanonischen Namen für ein Verb zurück zu geben. Diese Methode ist optional. Wenn Windows-Explorer in Windows XP und früheren Versionen von Windows Windows über eine Statusleiste verfügt, wird diese Methode verwendet, um den Hilfetext abzurufen, der in der Statusleiste für ein Menüelement angezeigt wird.

Der *idCmd-Parameter* enthält den Bezeichneroffset des Befehls, der beim Aufrufen [**von IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) definiert wurde. Wenn eine Hilfezeichenfolge angefordert wird, *werden uFlags* auf **GCS \_ HELPTEXTW festgelegt.** Kopieren Sie die Hilfezeichenfolge in den *Puffer pszName,* und geben Sie sie in **pwstr um.** Die Verbzeichenfolge wird durch Festlegen von *uFlags auf* **GCS \_ VERBW angefordert.** Kopieren Sie die entsprechende Zeichenfolge wie bei der Hilfezeichenfolge in *pszName.* Die **GCS \_ VALIDATEA-** und **GCS \_ VALIDATEW-Flags** werden nicht von Kontextmenühandlern verwendet.

Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu::GetCommandString,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) die dem [**IContextMenu::QueryContextMenu-Beispiel**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) entspricht, das im [Abschnitt IContextMenu::QueryContextMenu-Methode](#icontextmenuquerycontextmenu-method) dieses Themas angegeben ist. Da der Handler nur ein Menüelement hinzufügt, kann nur ein Satz von Zeichenfolgen zurückgegeben werden. Die -Methode testet, *ob idCmd* gültig ist, und gibt die angeforderte Zeichenfolge zurück.

Die [**StringCchCopy-Funktion**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) wird verwendet, um die angeforderte Zeichenfolge in *pszName* zu kopieren, um sicherzustellen, dass die kopierte Zeichenfolge nicht die größe des puffers überschreitet, die von *cchName angegeben wird.* In diesem Beispiel wird nur die Unterstützung für die Unicode-Werte von *uFlags* implementiert, da seit Windows 2000 nur diese im Windows-Explorer verwendet wurden.


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



### <a name="icontextmenuinvokecommand-method"></a>IContextMenu::InvokeCommand-Methode

Diese Methode wird aufgerufen, wenn ein Benutzer auf ein Menüelement klickt, um den Handler anweise, den zugeordneten Befehl auszuführen. Der *pici-Parameter* zeigt auf eine -Struktur, die die erforderlichen Informationen enthält.

*Obwohl pici* in Shlobj.h als [**CMINVOKECOMMANDINFO-Struktur**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) deklariert ist, verweist sie in der Praxis häufig auf eine [**CMINVOKECOMMANDINFOEX-Struktur.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) Diese Struktur ist eine erweiterte Version von **CMINVOKECOMMANDINFO** und verfügt über mehrere zusätzliche Member, die es ermöglichen, Unicode-Zeichenfolgen zu übergeben.

Überprüfen Sie **das cbSize-Member** von *pici,* um zu bestimmen, welche Struktur übergeben wurde. Wenn es sich um eine [**CMINVOKECOMMANDINFOEX-Struktur**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) handelt und für das **fMask-Element** das **UNICODE-Flag CMIC \_ MASK \_** festgelegt ist, cast *pici* in **CMINVOKECOMMANDINFOEX.** Dadurch kann Ihre Anwendung die Unicode-Informationen verwenden, die in den letzten fünf Membern der -Struktur enthalten sind.

Der **lpVerb-** oder **lpVerbW-Member** der -Struktur wird verwendet, um den auszuführenden Befehl zu identifizieren. Befehle werden auf eine der beiden folgenden Arten identifiziert:

-   Durch die Verbzeichenfolge des Befehls
-   Durch den Bezeichneroffset des Befehls

Um zwischen diesen beiden Fällen zu unterscheiden, überprüfen Sie das Wort in hoher Reihenfolge **von lpVerb** für den ANSI-Fall oder **lpVerbW** für den Unicode-Fall. Wenn das Wort in hoher Reihenfolge ungleich 0 (null) ist, enthält **lpVerb** oder **lpVerbW** eine Verbzeichenfolge. Wenn das Wort in hoher Reihenfolge 0 (null) ist, befindet sich der Befehlsoffset im Wort mit niedriger Reihenfolge von **lpVerb.**

Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu::InvokeCommand,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) die den Vor- und Nachher-Beispielen [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) und [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) entspricht. Die -Methode bestimmt zunächst, welche Struktur übergeben wird. Anschließend wird bestimmt, ob der Befehl durch seinen Offset oder sein Verb identifiziert wird. Wenn **lpVerb** oder **lpVerbW** ein gültiges Verb oder offset enthält, zeigt die Methode ein Meldungsfeld an.


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



### <a name="icontextmenuquerycontextmenu-method"></a>IContextMenu::QueryContextMenu-Methode

Die Shell ruft [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) auf, um dem Kontextmenühandler das Hinzufügen seiner Menüelemente zum Menü zu ermöglichen. Er übergibt das **HMENU-Handle** im *hmenu-Parameter.* Der *indexMenu-Parameter* wird auf den Index festgelegt, der für das erste hinzuzufügende Menüelement verwendet werden soll.

Alle vom Handler hinzugefügten Menüelemente müssen über Bezeichner verfügen, die zwischen den Werten in den *Parametern idCmdFirst* und *idCmdLast* liegen. In der Regel wird der erste Befehlsbezeichner auf *idCmdFirst* festgelegt, der für jeden zusätzlichen Befehl um eins (1) erhöht wird. Diese Vorgehensweise hilft Ihnen, die Überschreitung von *idCmdLast* zu vermeiden und maximiert die Anzahl der verfügbaren Bezeichner für den Fall, dass die Shell mehr als einen Handler aufruft.

Der *Befehlsoffset* eines Elementbezeichners ist der Unterschied zwischen dem Bezeichner und dem Wert in *idCmdFirst.* Store den Offset jedes Elements, das ihr Handler dem Kontextmenü hinzufügt, da die Shell es möglicherweise zum Identifizieren des Elements verwendet, wenn anschließend [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) oder [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)aufgerufen wird.

Außerdem sollten Sie jedem befehl, den Sie hinzufügen, ein [Verb](launch.md) zuweisen. Ein Verb ist eine Zeichenfolge, die anstelle des Offsets verwendet werden kann, um den Befehl zu identifizieren, wenn [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird. Sie wird auch von Funktionen wie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwendet, um Kontextmenübefehle auszuführen.

Es gibt drei Flags, die über den *uFlags-Parameter* übergeben werden können, die für Kontextmenühandler relevant sind. Diese werden in der folgenden Tabelle beschrieben.



| Flag             | Beschreibung                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | Der Benutzer hat den Standardbefehl ausgewählt, in der Regel durch Doppelklicken auf das Objekt. [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) sollte die Steuerung an die Shell zurückgeben, ohne das Menü zu ändern. |
| CMF \_ NODEFAULT   | Kein Element im Menü sollte das Standardelement sein. Die -Methode sollte ihre Befehle dem Menü hinzufügen.                                                                                                                          |
| CMF \_ NORMAL      | Das Kontextmenü wird normal angezeigt. Die -Methode sollte ihre Befehle dem Menü hinzufügen.                                                                                                                            |



 

Verwenden Sie entweder [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) oder [**InsertMenuItem,**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) um der Liste Menüelemente hinzuzufügen. Geben Sie dann einen **HRESULT-Wert zurück,** wobei der Schweregrad auf **SEVERITY \_ SUCCESS** festgelegt ist. Legen Sie den Codewert auf den Offset des größten zugewiesenen Befehlsbezeichners zuzüglich eines (1) fest. Angenommen, *idCmdFirst* ist auf 5 festgelegt, und Sie fügen dem Menü drei Elemente mit den Befehlsbezeichnern 5, 7 und 8 hinzu. Der Rückgabewert sollte `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` sein.

Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu::QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) die einen einzelnen Befehl einfügt. Der Bezeichneroffset für den Befehl ist IDM \_ DISPLAY, der auf 0 (null) festgelegt ist. Die Variablen **m \_ pszVerb** und **m \_ pwszVerb** sind private Variablen, die verwendet werden, um die zugeordnete sprachunabhängige Verbzeichenfolge sowohl im ANSI- als auch im Unicode-Format zu speichern.


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



Weitere Aufgaben zur Implementierung von Verben finden Sie unter [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontextmenüs und Kontextmenühandler](context-menu.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Bewährte Methoden für Kontextmenühandler und Verben für mehrfache Auswahl](verbs-best-practices.md)
</dt> <dt>

[Erstellen von Kontextmenühandlern](context-menu-handlers.md)
</dt> <dt>

[Kontextmenüreferenz](context-menu-reference.md)
</dt> </dl>

 

 
