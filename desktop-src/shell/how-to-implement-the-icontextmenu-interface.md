---
description: IContextMenu ist die leistungsfähigste, aber auch die komplizierteste Zu implementierende Schnittstelle.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Implementieren der IContextMenu-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44ec65d95a4f6d67a9f15e10f5720be21c3b6c57fba5d0cf920bd12be54f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223467"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Implementieren der IContextMenu-Schnittstelle

[**IContextMenu ist**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) die leistungsfähigste, aber auch die komplizierteste Zu implementierende Schnittstelle. Es wird dringend empfohlen, ein Verb mithilfe einer der statischen Verbmethoden zu implementieren. Weitere Informationen finden Sie unter [Auswählen einer statischen oder dynamischen Kontextmenümethode.](shortcut-choose-method.md) [**IContextMenu verfügt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) über drei Methoden, [**GetCommandString,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)und [**QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)die hier ausführlich erläutert werden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   C++

### <a name="prerequisites"></a>Voraussetzungen

-   Statisches Verb
-   Kontextmenü

## <a name="instructions"></a>Anweisungen

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu::GetCommandString-Methode

Die [**IContextMenu::GetCommandString-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) des Handlers wird verwendet, um den kanonischen Namen für ein Verb zurück zu geben. Diese Methode ist optional. Wenn Windows XP und frühere Versionen von Windows Windows über eine Statusleiste verfügt, wird diese Methode verwendet, um den Hilfetext abzurufen, der in der Statusleiste für ein Menüelement angezeigt wird.

Der *idCmd-Parameter* enthält den Bezeichneroffset des Befehls, der beim Aufrufen [**von IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) definiert wurde. Wenn eine Hilfezeichenfolge angefordert wird, *werden uFlags* auf **GCS \_ HELPTEXTW festgelegt.** Kopieren Sie die Hilfezeichenfolge in den *Puffer pszName,* und geben Sie sie in **pwstr um.** Die Verbzeichenfolge wird durch Festlegen von *uFlags auf* **GCS \_ VERBW angefordert.** Kopieren Sie die entsprechende Zeichenfolge wie bei der Hilfezeichenfolge in *pszName.* Die **GCS \_ VALIDATEA-** und **GCS \_ VALIDATEW-Flags** werden nicht von Kontextmenühandlern verwendet.

Das folgende Beispiel zeigt eine einfache Implementierung von [**GetCommandString,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) die dem [**QueryContextMenu-Beispiel**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) entspricht, das im [Abschnitt IContextMenu::QueryContextMenu-Methode](shortcut-menu-using-dynamic-verbs.md) dieses Themas angegeben ist. Da der Handler nur ein Menüelement hinzufügt, kann nur ein Satz von Zeichenfolgen zurückgegeben werden. Die -Methode testet, *ob idCmd* gültig ist, und gibt die angeforderte Zeichenfolge zurück.

Die [**StringCchCopy-Funktion**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) wird verwendet, um die angeforderte Zeichenfolge in *pszName* zu kopieren, um sicherzustellen, dass die kopierte Zeichenfolge nicht die größe des puffers überschreitet, die von *cchName angegeben wird.* In diesem Beispiel wird die Unterstützung nur für die Unicode-Werte von *uFlags* implementiert, da seit Windows 2000 nur diese im Windows-Explorer verwendet wurden.


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



### <a name="icontextmenuinvokecommand-method"></a>IContextMenu::InvokeCommand-Methode

Diese Methode wird aufgerufen, wenn ein Benutzer auf ein Menüelement klickt, um den Handler anweise, den zugeordneten Befehl auszuführen. Der *pici-Parameter* verweist auf eine -Struktur, die die informationen enthält, die zum Ausführen des Befehls erforderlich sind.

*Obwohl pici* in Shlobj.h als [**CMINVOKECOMMANDINFO-Struktur**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) deklariert ist, verweist sie in der Praxis häufig auf eine [**CMINVOKECOMMANDINFOEX-Struktur.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) Diese Struktur ist eine erweiterte Version von **CMINVOKECOMMANDINFO** und verfügt über mehrere zusätzliche Member, die es ermöglichen, Unicode-Zeichenfolgen zu übergeben.

Überprüfen Sie **das cbSize-Member** von *pici,* um zu bestimmen, welche Struktur übergeben wurde. Wenn es sich um eine [**CMINVOKECOMMANDINFOEX-Struktur**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) handelt und für das **fMask-Element** das **UNICODE-Flag CMIC \_ MASK \_** festgelegt ist, cast *pici* in **CMINVOKECOMMANDINFOEX.** Dadurch kann Ihre Anwendung die Unicode-Informationen verwenden, die in den letzten fünf Membern der -Struktur enthalten sind.

Der **lpVerb-** oder **lpVerbW-Member** der -Struktur wird verwendet, um den auszuführenden Befehl zu identifizieren. Befehle werden auf eine der beiden folgenden Arten identifiziert:

-   Durch die Verbzeichenfolge des Befehls
-   Durch den Bezeichneroffset des Befehls

Um zwischen diesen beiden Fällen zu unterscheiden, überprüfen Sie das obere Wort **lpVerb** für den ANSI-Fall oder **lpVerbW** für den Unicode-Fall. Wenn das hohe Wort ungleich null ist, enthält **lpVerb** oder **lpVerbW** eine Verbzeichenfolge. Wenn das hohe Wort 0 (null) ist, befindet sich der Befehlsoffset im niedrig geordneten Wort **lpVerb.**

Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu::InvokeCommand,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) die den Beispielen [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) und [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) entspricht, die vor und nach diesem Abschnitt angegeben wurden. Die -Methode bestimmt zuerst, welche Struktur übergeben wird. Anschließend wird bestimmt, ob der Befehl durch seinen Offset oder sein Verb identifiziert wird. Wenn **lpVerb oder** **lpVerbW ein** gültiges Verb oder offset enthält, zeigt die Methode ein Meldungsfeld an.


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



### <a name="icontextmenuquerycontextmenu-method"></a>IContextMenu::QueryContextMenu-Methode

Die Shell ruft [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) auf, um dem Kontextmenühandler das Hinzufügen seiner Menüelemente zum Menü zu ermöglichen. Er übergibt das **HMENU-Handle** im *hmenu-Parameter.* Der *indexMenu-Parameter* wird auf den Index festgelegt, der für das erste Menüelement verwendet werden soll, das hinzugefügt werden soll.

Alle Vom Handler hinzugefügten Menüelemente müssen über Bezeichner verfügen, die zwischen den Werten in den Parametern *idCmdFirst* und *idCmdLast liegen.* In der Regel wird der erste Befehlsbezeichner auf *idCmdFirst* festgelegt, der für jeden zusätzlichen Befehl um eins (1) erhöht wird. Diese Vorgehensweise hilft Ihnen, eine Überschreitung *von idCmdLast* zu vermeiden, und maximiert die Anzahl der verfügbaren Bezeichner, falls die Shell mehr als einen Handler aufruft.

Der Befehlsoffset eines *Elementbezeichners* ist der Unterschied zwischen dem Bezeichner und dem Wert in *idCmdFirst.* Store offset jedes Elements, das der Handler dem Kontextmenü hinzufügt, da die Shell möglicherweise den Offset zum Identifizieren des Elements verwendet, wenn sie anschließend [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) oder [**IContextMenu::InvokeCommand aufruft.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)

Außerdem sollten Sie jedem befehl, [den](launch.md) Sie hinzufügen, ein Verb zuweisen. Ein Verb ist eine Zeichenfolge, die anstelle des Offsets verwendet werden kann, um den Befehl zu identifizieren, wenn [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird. Sie wird auch von Funktionen wie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwendet, um Kontextmenübefehle auszuführen.

Es gibt drei Flags, die über den *uFlags-Parameter* übergeben werden können, die für Kontextmenühandler relevant sind. Diese werden in der folgenden Tabelle beschrieben.



| Flag             | Beschreibung                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | Der Benutzer hat den Standardbefehl ausgewählt, in der Regel durch Doppelklicken auf das Objekt. [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) sollte die Steuerung an die Shell zurückgeben, ohne das Menü zu ändern. |
| CMF \_ NODEFAULT   | Kein Element im Menü sollte das Standardelement sein. Die -Methode sollte ihre Befehle zum Menü hinzufügen.                                                                                                                          |
| CMF \_ NORMAL      | Das Kontextmenü wird normal angezeigt. Die -Methode sollte ihre Befehle zum Menü hinzufügen.                                                                                                                            |



 

Verwenden Sie [**entweder InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) oder [**InsertMenuItem,**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) um der Liste Menüelemente hinzuzufügen. Geben Sie dann einen **HRESULT-Wert** zurück, bei dem der Schweregrad auf SCHWEREGRAD ERFOLGREICH \_ festgelegt ist. Legen Sie den Codewert auf den Offset des größten zugewiesenen Befehlsbezeichners plus einen (1) fest. Angenommen, *idCmdFirst* ist auf 5 festgelegt, und Sie fügen dem Menü drei Elemente mit befehlsbezeichnern 5, 7 und 8 hinzu. Der Rückgabewert sollte MAKE \_ HRESULT(SEVERITY \_ SUCCESS, 0, 8 + 1) sein.

Das folgende Beispiel zeigt eine einfache Implementierung von [**QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) die einen einzelnen Befehl einfüge. Der Bezeichneroffset für den Befehl ist IDM \_ DISPLAY, der auf 0 (null) festgelegt ist. Die **Variablen m \_ pszVerb** und **m \_ pwszVerb** sind private Variablen, die zum Speichern der zugeordneten sprachunabhängigen Verbzeichenfolge sowohl im ANSI- als auch im Unicode-Format verwendet werden.


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



## <a name="remarks"></a>Hinweise

Weitere Aufgaben zur Verbimplementierung finden Sie unter [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)

 

 
