---
description: Wenn der Benutzer mit der rechten Maustaste auf einen Member eines Dateityps klickt, um das Eigenschaften Blatt Eigenschaften anzuzeigen, ruft die Shell die Eigenschaften Blatt Handler auf, die für den Dateityp registriert sind. Jeder Handler kann dem Standardeigenschaften Blatt eine benutzerdefinierte Seite hinzufügen.
title: Registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994663"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp

Wenn der Benutzer mit der rechten Maustaste auf einen Member eines Dateityps klickt, um das Eigenschaften Blatt Eigenschaften anzuzeigen, ruft die Shell die Eigenschaften Blatt Handler auf, die für den Dateityp registriert sind. Jeder Handler kann dem Standardeigenschaften Blatt eine benutzerdefinierte Seite hinzufügen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   Shell

### <a name="prerequisites"></a>Voraussetzungen

-   Ein Verständnis der Kontextmenüs

## <a name="instructions"></a>Instructions

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Schritt 1: Registrieren eines Eigenschaften Blatt Handlers für einen Dateityp

Fügen Sie dem **shellex** -Unterschlüssel des ProgID-Schlüssels der Anwendung, die dem Dateityp zugeordnet ist, neben der normalen Component Object Model Registrierung (com) einen **propertysheethandlers** -Unterschlüssel hinzu. Erstellen Sie einen Unterschlüssel von **propertysheethandlers** mit dem Namen des Handlers, und legen Sie den Standardwert auf das Zeichen folgen Format der Klassen Bezeichner-GUID (CLSID) des Eigenschaften Blatts fest.

Wenn Sie dem Eigenschaften Blatt mehr als eine Seite hinzufügen möchten, registrieren Sie einen Handler für jede Seite. Die maximale Anzahl von Seiten, die von einem Eigenschaften Blatt unterstützt werden können, ist 32. Um mehrere Handler zu registrieren, erstellen Sie einen Schlüssel unter dem **shellex** -Schlüssel für jeden Handler, wobei der Standardwert auf die CLSID-GUID des Handlers festgelegt ist. Es ist nicht erforderlich, für jeden Handler ein unterschiedliches Objekt zu erstellen, was bedeutet, dass mehrere Handler denselben GUID-Wert aufweisen können. Die Seiten werden in der Reihenfolge angezeigt, in der Ihre Schlüssel unter **shellex** aufgeführt sind.

Das folgende Beispiel veranschaulicht einen Registrierungs Eintrag, der zwei Eigenschaften Blatt-Erweiterungs Handler für den Dateityp example. MYP aktiviert. In diesem Beispiel wird ein separates Objekt für jede Seite verwendet, aber es kann auch ein einzelnes Objekt für beide verwendet werden.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Schritt 2: Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp

Zusätzlich zu der allgemeinen Implementierung, die unter [Funktionsweise von Eigenschaften Blatt Handlern](propsheet-handlers.md)erläutert wird, muss ein Eigenschaften Blatt Handler für einen Dateityp auch über eine entsprechende Implementierung der [**ishellpropsheetext**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) -Schnittstelle verfügen. Nur die [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode benötigt eine nicht Token-Implementierung. Die Shell ruft nicht [**ishellpropsheetext:: replacepage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage)auf.

Mit der [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode kann ein Eigenschaften Blatt Handler eine Seite zu einem Eigenschaften Blatt hinzufügen. Die-Methode verfügt über zwei Eingabeparameter. Der erste *lpfnaddpage*-Wert ist ein Zeiger auf eine [*addpropsheetpageproc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) -Rückruffunktion, die verwendet wird, um der Shell die Informationen zur Verfügung zu stellen, die erforderlich sind, um die Seite dem Eigenschaften Blatt hinzuzufügen. Der zweite *LPARAM*-Wert ist ein shelldefinierter Wert, der nicht vom Handler verarbeitet wird. Sie wird einfach an die Shell zurückgegeben, wenn die Rückruffunktion aufgerufen wird.

Das allgemeine Verfahren zum Implementieren von [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) lautet wie folgt.

**Implementieren der addPages-Methode**

1.  Weisen Sie den Membern einer [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) -Struktur geeignete Werte zu. Dies gilt insbesondere für:
    -   Weisen Sie die Variable, die den Verweis Zähler des Handlers enthält, dem **pkrefparent** -Member zu. Diese Vorgehensweise verhindert, dass das Handlerobjekt entladen wird, während das Eigenschaften Blatt noch angezeigt wird.
    -   Sie können auch eine [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Rückruffunktion implementieren und Ihren Zeiger einem **pfncallback** -Member zuweisen. Diese Funktion wird aufgerufen, wenn die Seite erstellt wird und wenn Sie gelöscht wird.
2.  Erstellen Sie den hPage-Handle der Seite, indem Sie die [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) -Struktur an [**die Funktion "**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) " in der Funktion "-Funktion" übergeben.
3.  Die Funktion, auf die von *lpfnaddpage* verwiesen wird, wird aufgerufen. Legen Sie den ersten Parameter auf das hPage-Handle fest, das im vorherigen Schritt erstellt wurde. Legen Sie den zweiten Parameter auf den *LPARAM* -Wert fest, der von der Shell an [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) übergeben wurde.
4.  Alle der Seite zugeordneten Nachrichten werden an die Dialogfeld Prozedur, die dem **pfndlgproc** -Member der [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) -Struktur zugewiesen wurde, übermittelt.
5.  Wenn Sie **pfncallback** eine [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Rückruffunktion zugewiesen haben, wird Sie aufgerufen, wenn die Seite zerstört werden soll. Der Handler kann dann alle erforderlichen Bereinigungs Vorgänge ausführen, z. b. die Freigabe aller darin enthaltenen Verweise.

Im folgenden Codebeispiel wird eine einfache [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Implementierung veranschaulicht.


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



Die Variable **g \_ hInst** ist der Instanzhandle für die dll, und IDD \_ pagedlg ist die Ressourcen-ID der Dialogfeld Vorlage der Seite. Die **pagedlgproc** -Funktion ist die Dialogfeld Prozedur, die die Meldungen der Seite behandelt. Die **g \_ dllref count** -Variable enthält den Verweis Zähler des Objekts. Die [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode ruft die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) auf, um die Anzahl zu erhöhen. Der Verweis Zähler wird jedoch von der Rückruffunktion **pagecallbackproc** freigegeben, wenn die Seite zerstört werden soll.

## <a name="remarks"></a>Bemerkungen

Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ishellpropsheetext**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
