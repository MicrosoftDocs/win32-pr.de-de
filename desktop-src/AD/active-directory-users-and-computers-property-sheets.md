---
title: Eigenschaften Blätter für das Active Directory von Benutzern und Computern
description: Das MMC-Snap-in "Active Directory-Benutzer und-Computer" ist darauf ausgelegt, ein Eigenschaften Blatt für verschiedene Objekte auf einem Active Directory Server anzuzeigen.
ms.assetid: 38032d89-9549-475c-90aa-dac5cfe11084
ms.tgt_platform: multiple
keywords:
- Eigenschaften Blätter für Active Directory Benutzer und Computer anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea24f34e86f21af178e975852accb667bb69e4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724665"
---
# <a name="active-directory-users-and-computers-property-sheets"></a>Eigenschaften Blätter für das Active Directory von Benutzern und Computern

Das MMC-Snap-in "Active Directory-Benutzer und-Computer" ist darauf ausgelegt, ein Eigenschaften Blatt für verschiedene Objekte auf einem Active Directory Server anzuzeigen. Das Eigenschaften Blatt enthält eine oder mehrere Seiten, die zum Anzeigen und Ändern von Objektdaten verwendet werden. Für unterschiedliche Objekttypen werden unterschiedliche Seiten Sätze angezeigt. Das MMC-Snap-in "Active Directory-Benutzer und-Computer" ermöglicht Drittanbietern auch das Hinzufügen benutzerdefinierter Seiten zum Eigenschaften Blatt für einen bestimmten Objekttyp. Weitere Informationen finden Sie unter [Eigenschaften Seiten für die Verwendung mit Anzeige spezifiken](property-pages-for-use-with-display-specifiers.md).

Einige Anwendungen, außer dem MMC-Snap-in "Active Directory-Benutzer und-Computer", müssen dem Benutzer die Möglichkeit bieten, Attribute für ein Objekt in einem Active Directory Server anzuzeigen und zu bearbeiten. Die Anwendung könnte eigene Eigenschaften Blätter implementieren, aber es ist besser, eine konsistente Benutzeroberfläche bereitzustellen, um Verwirrung und Lernzeit zu reduzieren. Glücklicherweise ermöglicht das MMC-Snap-in "Active Directory-Benutzer und-Computer" allen OLE-COM-Anwendungen, ein Eigenschaften Blatt für ein Objekt anzuzeigen, das mit dem Eigenschaften Blatt identisch ist, das vom MMC-Snap-in "Active Directory-Benutzer und-Computer" für dasselbe Objekt angezeigt wird.

Weitere Informationen und ein Codebeispiel, in dem ein Eigenschaften Blatt für Active Directory Benutzer und Computer gehostet wird, finden Sie im Beispiel propsheethost im Platform Software Development Kit (SDK).

## <a name="developer-audience"></a>Entwicklerzielgruppe

In dieser Dokumentation wird davon ausgegangen, dass der Reader mit der com-Operation und-Komponentenentwicklung mit C++ vertraut ist. Derzeit ist es nicht möglich, eine Active Directory Eigenschaften Blatt Erweiterung mit Visual Basic zu erstellen.

## <a name="hosting-an-active-directory-users-and-computers-property-sheet"></a>Eigenschaften Blatt "Active Directory-Benutzer und-Computer" wird gehostet

**So zeigen Sie ein Eigenschaften Blatt für ein Objekt in einem Active Directory Server an**

1.  Erstellen Sie ein Fenster, das zum Verarbeiten von Nachrichten verwendet werden kann. Dabei kann es sich um ein vorhandenes oder ein spezielles Fenster handeln. Dies wird als ausgeblendetes *Fenster* bezeichnet.
2.  Erstellen Sie ein OLE-COM-Objekt, das von [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)abgeleitet ist. Dieses Datenobjekt muss die folgenden Datenformate unterstützen:

    -   [**Cfstr \_ Dsobjectnames**](cfstr-dsobjectnames.md) dieses Datenformat enthält einen [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Wert, der das Objekt identifiziert, für das das Eigenschaften Blatt gilt. Beim Hosting eines Eigenschaften Blatts werden die signifikanteren Member der **dsobjectnames** -Struktur in der folgenden Liste angezeigt.

        **clsidnamespace** Bleiben. Legen Sie dies für die Anwendung hier auf eine GUID fest, wenn Sie in Zukunft verwendet wird.
        
        **aobjects** Enthält ein Array von [**dsboject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Strukturen. Jede **dsboject** -Struktur stellt ein einzelnes Verzeichnis Objekt dar. Der Member **cItems** enthält die Anzahl der Elemente im Array. Es wird nur das erste Objekt in diesem Array verwendet. Andere Objekte werden ignoriert.

    -   [**Cfstr \_ Dsdisplayspecoptions**](cfstr-ds-display-spec-options.md) dieses Datenformat enthält eine [**dsdisplayspecoptions**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) -Struktur, die Daten enthält, die von den Eigenschaften Seiten verwendet werden, z. b. den Speicherort der Eigenschaften Seiten, den Server und die Anmelde Informationen, die verwendet werden sollen, usw. In der folgenden Liste sind die signifikanteren Member der **dsdisplayspecoptions** -Elemente aufgeführt.

        **offmentattribprefix** Die Attribut Präfix Zeichenfolge bestimmt, wo die Liste der Eigenschaften Seiten abgerufen wird. Diese muss eine der folgenden Zeichen folgen enthalten.

        

        | Präfix-Zeichenfolge | BESCHREIBUNG                                              |
        |-------------------------|----------------------------------------------------------------------------------------------------------------------|
        | Administrator<br/>      | Die Eigenschaften Seiten werden aus dem Attribut [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) geladen.<br/> |
        | schel<br/>      | Die Eigenschaften Seiten werden aus dem [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages) -Attribut geladen.<br/> |

        


    -   [**Cfstr \_ DS \_ propsheetconfig**](cfstr-ds-propsheetconfig.md) dieses Datenformat enthält eine [**propsheetcfg**](propsheetcfg.md) -Struktur, die Eigenschaften Blatt-Hostdaten enthält. Beim Hosting eines Eigenschaften Blatts enthalten die signifikanteren Member der **propsheetcfg** -Struktur die in der folgenden Liste dargestellten Daten.

        **lnotifyhandle** Muss 0 (null) sein.
        **hwndparametrisheet**  Enthält das Handle des Fensters zum Empfangen von " [**WM \_ adsprop \_ Notify \_ Change**](wm-adsprop-notify-change.md) Messages", wenn etwas auf einer der Seiten geändert wird und angewendet wird. Kann **null** sein, wenn diese Nachricht nicht gewünscht ist.

        **hwndhidden** Enthält das Handle des Fensters zum Empfangen der [**WM- \_ DSA- \_ Blatt \_ Erstellung \_ Benachrichtigen**](wm-dsa-sheet-create-notify.md) und [**WM-DSA- \_ \_ Blatt \_ Close \_ Notify**](wm-dsa-sheet-close-notify.md) Messages. Legen Sie diese Einstellung auf das Handle des ausgeblendeten Fensters fest.

        **wparamsheetclose** Enthält einen von der Anwendung definierten Bezeichner, der in der *wParam* in der [**WM-DSA-Tabelle " \_ \_ \_ Close \_ Notify**](wm-dsa-sheet-close-notify.md) Message" zurückgegeben wird. Wenn dieser Member 0 (null) ist, wird das WM-DSA-Blatt "Nachricht **\_ \_ \_ Schließen \_** " nicht im verborgenen Fenster gepostet.


3.  Erstellen Sie eine Instanz des [**CLSID \_ dspropertypages**](guids-of-user-interface-elements.md) -Objekts, und rufen Sie die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle für das Objekt ab. Es ist auch möglich, das Verhalten des **CLSID-Objekts \_ dspropertypages** zu duplizieren. Weitere Informationen finden Sie unter Duplizieren des Verhaltens des CLSID \_ dspropertypages-Objekts.
4.  Initialisieren Sie das [**CLSID \_ dspropertypages**](guids-of-user-interface-elements.md) -Objekt, indem Sie die [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode aufrufen. Die Parameter *pidlfolder* und *hkeyprogid* werden in dieser Methode nicht verwendet. Der *pdtobj* -Parameter ist der Zeiger auf das Datenobjekt, das in Schritt 2 erstellt wurde. Wenn die **ishellextinit:: Initialize** -Methode aufgerufen wird, speichert das **CLSID \_ dspropertypages** -Objekt einen Verweis auf das Datenobjekt.
5.  Rufen Sie die [**ishellpropsheetext**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) -Schnittstelle für das [**CLSID \_ dspropertypages**](guids-of-user-interface-elements.md) -Objekt ab, und rufen Sie die [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode auf. Der *lpfnaddpage* -Parameter ist die Adresse einer Rückruffunktion, die Sie implementieren müssen. Das Format dieser Funktion ist unten dargestellt. Wenn die Rückruffunktion als Member einer C++-Klasse deklariert ist, muss die Rückruffunktion als **statisch** deklariert werden. Der *LPARAM* -Parameter ist ein von der Anwendung definierter Wert, der zum Identifizieren des Objekts verwendet werden kann, das die Rückruffunktion implementiert. Wenn die **ishellpropsheetext:: addPages** -Methode aufgerufen wird, ruft das **CLSID \_ dspropertypages** -Objekt die Daten aus dem Datenobjekt ab und listet die Eigenschaften Seiten auf, die für die Objekt Anzeige spezifiers registriert sind. Das **CLSID \_ dspropertypages** -Objekt zählt dann die Eigenschaften Seiten Objekte auf, wobei die **ishellpropsheetext:: addPages** -Methode jedes Objekts aufgerufen wird.

    ```C++
    BOOL CALLBACK AddPagesCallback(HPROPSHEETPAGE, LPARAM)
    ```

    

6.  Jede Seite, die von den Eigenschaften Seiten Objekten hinzugefügt wird, führt dazu, dass die Rückruffunktion mit dem Handle auf der Eigenschaften Seite und dem von der Anwendung definierten Wert aufgerufen wird. Die Rückruffunktion muss jeden bestandenen Eigenschaften Seiten Handle speichern. Wenn die [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode des [**CLSID \_ dspropertypages**](guids-of-user-interface-elements.md) -Objekts zurückgibt, wurden alle Seiten über Ihre Rückruffunktion hinzugefügt.
7.  Füllen Sie eine [**propsheetheiader**](/windows/win32/api/prsht/ns-prsht-propsheetheadera_v2) -Struktur aus, um das Eigenschaften Blatt anzuzeigen. Der **phpage** -Member erhält einen Zeiger auf ein Array von Seiten Handles, die von ihrer Rückruffunktion erfasst wurden. Der **npages** -Member empfängt die Anzahl der Seiten im Seiten Handle-Array.
8.  Zeigen Sie das Eigenschaften Blatt durch Aufrufen der [**PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) -Funktion an.

Wenn die Daten auf einer beliebigen Seite geändert werden und auf die Schaltflächen **OK** oder **anwenden** geklickt wird, erhält das Fenster, das durch das **hwndparametsheet** -Element der [**propsheetcfg**](propsheetcfg.md) -Struktur identifiziert wird, eine " [**WM \_ adsprop \_ Notify \_ Change**](wm-adsprop-notify-change.md) Message". Bei dieser Nachricht handelt es sich um eine reine Benachrichtigung, die keine bestimmte Aktion erfordert.

Wenn die Seite geschlossen wird, erhält das Fenster, das durch das **hwndhidden** -Element der [**propsheetcfg**](propsheetcfg.md) -Struktur identifiziert wird, eine Meldung zum [**\_ \_ \_ Schließen \_**](wm-dsa-sheet-close-notify.md) der "WM-DSA". Bei dieser Nachricht handelt es sich um eine reine Benachrichtigung, und es muss keine bestimmte Aktion ausgeführt werden.

In einigen Fällen muss für die vorhandenen Eigenschaften Blätter ein sekundäres Eigenschaften Blatt angezeigt werden. Wenn Sie z. b. das Eigenschaften Blatt für ein Benutzerobjekt anzeigen und das **Mitglied der** Seite auswählen, wird eine Liste der Gruppen angezeigt, in denen der Benutzer Mitglied ist. Wenn Sie auf eine dieser Gruppen in der Liste doppelklicken, wird das Eigenschaften Blatt für diese Gruppe angezeigt. Auf dem primären Eigenschaften Blatt wird das sekundäre Blatt nicht allein angezeigt. Sie fordert an, dass der Host das sekundäre Blatt anzeigt, indem er ein [**WM- \_ DSA- \_ Blatt \_ Create \_ Notify**](wm-dsa-sheet-create-notify.md) Message an das Fenster sendet, das vom **hwndhidden** -Member der [**propsheetcfg**](propsheetcfg.md) -Struktur identifiziert wird. Der *wParam* des **WM- \_ DSA- \_ Blatts \_ Create \_ Notify** Message ist ein Zeiger auf eine [**DSA sec- \_ \_ Seiten \_**](dsa-sec-page-info.md) Informationsstruktur, die Informationen über das sekundäre Eigenschaften Blatt und das Objekt enthält, das es darstellt. Als Antwort auf diese Nachricht muss der Eigenschaften Blatt Host das sekundäre Eigenschaften Blatt auf die gleiche Weise wie oben dargestellt anzeigen. Nach der Verarbeitung des **WM- \_ DSA- \_ Blatts \_ Create \_ Notify** Message muss der Nachrichtenempfänger die **DSA sec- \_ \_ Seiten \_ Informations** Struktur freigeben, indem er den *wParam* -Wert an die [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) -Funktion übergibt.

## <a name="duplicating-the-behavior-of-the-clsid_dspropertypages-object"></a>Duplizieren des Verhaltens des CLSID- \_ dspropertypages-Objekts

**So duplizieren Sie das Verhalten des CLSID- \_ dspropertypages-Objekts**

1.  Zählen Sie die Werte im Attribut [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) oder [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages) für den Anzeigespezifizierer für die Objektklasse auf. Jeder Wert ist eine Zeichenfolge, die eine Zahl gefolgt von einem Komma enthält, gefolgt von der Zeichen folgen Darstellung des Klassen Bezeichners der Erweiterung der Eigenschaften Seite. Weitere Informationen zum Format der Eigenschaften Seiten Anzeige spezifiziererwerte finden Sie unter [Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer](registering-the-property-page-com-object-in-a-display-specifier.md).
2.  Konvertieren Sie jede Klassen-Bezeichnerzeichenfolge mithilfe der [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion in eine **CLSID** .
3.  Sortieren Sie die Bezeichner der Erweiterungs Klasse nach der Zahl, die den einzelnen Klassen-ID-Zeichen folgen im Attribut Wert vorangestellt ist. Wenn zwei Zahlen identisch sind, Sortieren Sie die Klassen Bezeichner in der Reihenfolge, in der die Attributwerte vom Active Directory Server abgerufen werden.
4.  Listet die Erweiterungs Klassen Bezeichner auf und erstellt eine Instanz der einzelnen Erweiterungen.
5.  Nennen Sie für jede Erweiterung in der oben aufgeführten Reihenfolge die [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Erweiterung mit denselben Informationen, die Sie in Schritt 4 des Eigenschaften Blatts zum Hosting eines Active Directory Benutzer und Computers beschrieben haben.
6.  Nennen Sie für jede Erweiterung in der oben aufgeführten Reihenfolge die [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) der Erweiterung mit denselben Informationen, die Sie in Schritt 5 des Eigenschaften Blatts zum Hosting eines Active Directory Benutzer und Computers beschrieben haben.

Verwenden Sie nach Möglichkeit das [**CLSID- \_ dspropertypages**](guids-of-user-interface-elements.md) -Objekt, um die Seiten zu erstellen, anstatt dies manuell zu tun. Die **CLSID- \_ dspropertypages** wurde optimiert und behandelt Fehlerfälle ordnungsgemäß, z. b. Wenn für das aktuelle Gebiets Schema kein Anzeigespezifizierer verfügbar ist. Außerdem kann sich das **CLSID- \_ dspropertypages** -Objekt in Zukunft ändern. Dies bedeutet, dass ihre Eigenschaften Blätter möglicherweise nicht genau mit den Eigenschaften des MMC-Snap-Ins "Active Directory Benutzer und Computer" übereinstimmen.

## <a name="special-programming-elements"></a>Besondere Programmier Elemente

Derzeit sind die folgenden Programmier Elemente nicht in einer veröffentlichten Header Datei definiert. Wenn Sie diese Elemente verwenden möchten, müssen Sie Sie im exakten Format definieren, das auf der jeweiligen Verweisseite angezeigt wird.

-   [**cfstr \_ DS \_ propsheetconfig**](cfstr-ds-propsheetconfig.md)
-   [**Propsheetcfg**](propsheetcfg.md)
-   [**WM- \_ DSA- \_ Blatt " \_ Schließen \_ "**](wm-dsa-sheet-close-notify.md)
-   [**WM \_ - \_ Blatt "DSA \_ Erstellen \_ "**](wm-dsa-sheet-create-notify.md)
-   [**\_ \_ Seite \_ Informationen zu DSA sec**](dsa-sec-page-info.md)

## <a name="example-code"></a>Beispielcode

Im folgenden C++-Codebeispiel wird eine sichere Möglichkeit zum Definieren dieser Elemente veranschaulicht, die weiterhin funktionieren, auch wenn diese Elemente in Zukunft in einer veröffentlichten Header Datei definiert sind.


```C++
#ifndef CFSTR_DS_PROPSHEETCONFIG
    #define CFSTR_DS_PROPSHEETCONFIG_W L"DsPropSheetCfgClipFormat"
    #define CFSTR_DS_PROPSHEETCONFIG_A "DsPropSheetCfgClipFormat"

    #ifdef UNICODE
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_W
    #else
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_A
    #endif //UNICODE
#endif //CFSTR_DS_PROPSHEETCONFIG


#ifndef WM_ADSPROP_SHEET_CREATE
    #define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
#endif


#ifndef WM_DSA_SHEET_CREATE_NOTIFY
    #define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
#endif


#ifndef WM_DSA_SHEET_CLOSE_NOTIFY
    #define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5) 
#endif


#ifndef DSA_SEC_PAGE_INFO
    typedef struct _DSA_SEC_PAGE_INFO
    {
        HWND    hwndParentSheet;
        DWORD   offsetTitle;
        DSOBJECTNAMES dsObjectNames;
    } DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
#endif //DSA_SEC_PAGE_INFO

#ifndef PROPSHEETCFG
    typedef struct _PROPSHEETCFG
    {  
        LONG_PTR lNotifyHandle;  
        HWND hwndParentSheet;  
        HWND hwndHidden;  
        WPARAM wParamSheetClose;
    } PROPSHEETCFG, *PPROPSHEETCFG;
#endif //PROPSHEETCFG
```



 

