---
description: IContextMenu ist die leistungsfähigste, aber auch die komplizierteste Schnittstelle, die implementiert werden kann.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Implementieren der IContextMenu-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959691"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Implementieren der IContextMenu-Schnittstelle

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Schnittstelle, die implementiert werden kann. Es wird dringend empfohlen, dass Sie ein Verb mithilfe einer der statischen Verb-Methoden implementieren. Weitere Informationen finden Sie unter [Auswählen einer statischen oder dynamischen Kontextmenü Methode](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) verfügt über drei Methoden: [**getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)und [**querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), die hier ausführlich erläutert werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   C++

### <a name="prerequisites"></a>Voraussetzungen

-   Statisches Verb
-   Kontextmenü

## <a name="instructions"></a>Instructions

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu:: getcommandstring-Methode

Die [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) -Methode des Handlers wird verwendet, um den kanonischen Namen eines Verbs zurückzugeben. Diese Methode ist optional. In Windows XP und früheren Versionen von Windows wird diese Methode verwendet, um den Hilfetext abzurufen, der in der Statusleiste für ein Menü Element angezeigt wird, wenn Windows-Explorer über eine Status Leiste verfügt.

Der *idcmd* -Parameter enthält den bezeichneroffset des Befehls, der beim [**Aufrufen von IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) definiert wurde. Wenn eine Hilfe Zeichenfolge angefordert wird, wird *uFlags* auf **GCS \_ helptextw** festgelegt. Kopieren Sie die Hilfe Zeichenfolge in den *pszName* -Puffer, und wandeln Sie Sie in ein **pwstr** um. Die Verb Zeichenfolge wird angefordert, indem *uFlags* auf **GCS- \_ verbw** festgelegt wird. Kopieren Sie die entsprechende Zeichenfolge wie bei der Hilfe Zeichenfolge in *pszName*. Die **\_ validatew** -Flags für **GCS \_ validatea** und GCS werden von Kontextmenü Handlern nicht verwendet.

Das folgende Beispiel zeigt eine einfache Implementierung von [**getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , die dem im Abschnitt [IContextMenu:: querycontextmenu-Methode](shortcut-menu-using-dynamic-verbs.md) in diesem Thema angegebenen [**querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Beispiel entspricht. Da der Handler nur ein Menü Element hinzufügt, gibt es nur einen Satz von Zeichen folgen, die zurückgegeben werden können. Die-Methode testet, ob *idcmd* gültig ist, und gibt, wenn dies der Fall ist, die angeforderte Zeichenfolge zurück.

Die [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) -Funktion wird verwendet, um die angeforderte Zeichenfolge nach *pszName* zu kopieren, um sicherzustellen, dass die kopierte Zeichenfolge die Größe des durch *cchName* angegebenen Puffers nicht überschreitet. In diesem Beispiel wird die Unterstützung nur für die Unicode-Werte von *uFlags* implementiert, da nur diese seit Windows 2000 in Windows-Explorer verwendet wurden.


```
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
                // to discover the canonical name for the verb that is passed in
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

Diese Methode wird aufgerufen, wenn ein Benutzer auf ein Menü Element klickt, um den Handler anzuweisen, den zugehörigen Befehl auszuführen. Der *pici* -Parameter verweist auf eine-Struktur, die die zum Ausführen des Befehls erforderlichen Informationen enthält.

Obwohl *pici* in shlobj. h als [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) -Struktur deklariert ist, verweist es in der Praxis häufig auf eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur. Diese Struktur ist eine erweiterte Version von **cminvokecommandinfo** und verfügt über mehrere zusätzliche Member, die es ermöglichen, Unicode-Zeichen folgen zu übergeben.

Überprüfen Sie das **CBSIZE** -Member von *pici* , um zu bestimmen, welche Struktur übergeben wurde. Wenn es sich um eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur handelt und für den **fmask** -Member das **CMIC \_ mask- \_ Unicode** -Flag festgelegt ist, wandeln Sie *pici* in **cminvokecommandinfoex** um. Dadurch kann Ihre Anwendung die Unicode-Informationen verwenden, die in den letzten fünf Membern der Struktur enthalten sind.

Der **lpverb** -oder **lpverbw** -Member der Struktur wird verwendet, um den auszuführenden Befehl zu identifizieren. Befehle werden auf eine der beiden folgenden Arten identifiziert:

-   Durch die Verb Zeichenfolge des Befehls
-   Nach dem bezeichneroffset des Befehls

Um zwischen diesen beiden Fällen zu unterscheiden, überprüfen Sie das höchst wertige Wort **lpverb** für die ANSI-Groß-/Kleinschreibung oder **lpverbw** für den Unicode-Fall. Wenn das hochwertige Wort nicht NULL ist, enthält **lpverb** oder **lpverbw** eine Verb Zeichenfolge. Wenn das hochwertige Wort 0 (null) ist, befindet sich der Befehls Offset im nieder wertigen Wort **lpverb**.

Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , die den Beispielen " [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) " und " [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) " entspricht, die vor und nach diesem Abschnitt angegeben werden. Die-Methode bestimmt zunächst, welche Struktur an Sie übermittelt wird. Anschließend bestimmt er, ob der Befehl durch seinen Offset oder sein Verb gekennzeichnet wird. Wenn **lpverb** oder **lpverbw** ein gültiges Verb oder einen gültigen Offset enthält, zeigt die Methode ein Meldungs Feld an.


```
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

Der *Befehls Offset* eines Element Bezeichners ist der Unterschied zwischen dem Bezeichner und dem Wert in *idcmdfirst*. Speichern Sie den Offset der einzelnen Elemente, die der Handler dem Kontextmenü hinzufügt, da die Shell den Offset verwenden kann, um das Element zu identifizieren, wenn es anschließend [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) oder [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)aufruft.

Sie sollten jedem Befehl, den Sie hinzufügen, auch ein [Verb](launch.md) zuweisen. Ein Verb ist eine Zeichenfolge, die anstelle des Offsets verwendet werden kann, um den Befehl zu identifizieren, wenn [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird. Sie wird auch von Funktionen wie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Ausführen von Kontextmenü Befehlen verwendet.

Es gibt drei Flags, die über den *uFlags* -Parameter übergeben werden können, die für Kontextmenü Handler relevant sind. Diese werden in der folgenden Tabelle beschrieben.



| Flag             | Beschreibung                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DefaultOnly | Der Benutzer hat den Standardbefehl ausgewählt, in der Regel durch Doppelklicken auf das Objekt. [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) sollte die Steuerung an die Shell zurückgeben, ohne das Menü zu ändern. |
| CMF- \_ NODEFAULT   | Kein Element im Menü sollte das Standardelement sein. Die-Methode sollte Ihre Befehle dem Menü hinzufügen.                                                                                                                          |
| CMF \_ Normal      | Das Kontextmenü wird normal angezeigt. Die-Methode sollte Ihre Befehle dem Menü hinzufügen.                                                                                                                            |



 

Verwenden Sie entweder [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) oder [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) , um der Liste Menü Elemente hinzuzufügen. Geben Sie anschließend einen **HRESULT** -Wert mit dem Schweregrad \_ Success an. Legen Sie den Codewert auf den Offset des größten Befehls Bezeichners fest, der zugewiesen wurde, plus eins (1). Nehmen Sie beispielsweise an, dass *idcmdfirst* auf 5 festgelegt ist und Sie dem Menü drei Elemente mit den Befehls bezeichlern 5, 7 und 8 hinzufügen. Der Rückgabewert muss \_ HRESULT lauten (Schweregrad \_ Success, 0, 8 + 1).

Das folgende Beispiel zeigt eine einfache Implementierung von [**querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , die einen einzelnen Befehl einfügt. Der bezeichneroffset für den Befehl ist die IDM- \_ Anzeige, die auf 0 (null) festgelegt ist. Die Variablen **m \_ pszverb** und **m \_ pwszverb** sind private Variablen, die zum Speichern der zugeordneten sprachunabhängigen Verb Zeichenfolge im ANSI-und Unicode-Format verwendet werden.


```
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

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a>Bemerkungen

Informationen zu anderen Verb Implementierungsaufgaben finden Sie unter Erstellen von Kontext [Menü Handlern](context-menu-handlers.md).

 

 
