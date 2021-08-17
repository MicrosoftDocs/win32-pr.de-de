---
description: Wenn der Benutzer mit der rechten Maustaste auf einen Member eines Dateityps klickt, um das Eigenschafteneigenschaftenblatt anzuzeigen, ruft die Shell die Eigenschaftenblatthandler auf, die für den Dateityp registriert sind. Jeder Handler kann dem Standardeigenschaftenblatt eine benutzerdefinierte Seite hinzufügen.
title: Registrieren und Implementieren eines Eigenschaftenblatthandlers für einen Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce0451071ba1f454ffae9ca1444f30428909946442f5aead853e74095d0c0c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049806"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Registrieren und Implementieren eines Eigenschaftenblatthandlers für einen Dateityp

Wenn der Benutzer mit der rechten Maustaste auf einen Member eines Dateityps klickt, um das Eigenschafteneigenschaftenblatt anzuzeigen, ruft die Shell die Eigenschaftenblatthandler auf, die für den Dateityp registriert sind. Jeder Handler kann dem Standardeigenschaftenblatt eine benutzerdefinierte Seite hinzufügen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   Shell

### <a name="prerequisites"></a>Voraussetzungen

-   Verstehen von Kontextmenüs

## <a name="instructions"></a>Anweisungen

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Schritt 1: Registrieren eines Eigenschaftenblatthandlers für einen Dateityp

Fügen Sie neben der normalen com-Registrierung (Component Object Model) dem **Shellex-Unterschlüssel** des ProgID-Schlüssels der Anwendung, die dem Dateityp zugeordnet ist, einen **PropertySheetHandlers-Unterschlüssel** hinzu. Erstellen Sie einen Unterschlüssel von **PropertySheetHandlers** mit dem Namen des Handlers, und legen Sie den Standardwert auf die Zeichenfolgenform der CLSID-GUID (Class Identifier) des Eigenschaftenblatthandlers fest.

Um dem Eigenschaftenblatt mehrere Seiten hinzuzufügen, registrieren Sie einen Handler für jede Seite. Die maximale Anzahl von Seiten, die ein Eigenschaftenblatt unterstützen kann, beträgt 32. Um mehrere Handler zu registrieren, erstellen Sie einen Schlüssel unter dem **Shellex-Schlüssel** für jeden Handler, wobei der Standardwert auf die CLSID-GUID des Handlers festgelegt ist. Es ist nicht erforderlich, für jeden Handler ein eigenes Objekt zu erstellen. Das bedeutet, dass mehrere Handler denselben GUID-Wert aufweisen können. Die Seiten werden in der Reihenfolge angezeigt, in der ihre Schlüssel unter **shellex** aufgeführt sind.

Das folgende Beispiel veranschaulicht einen Registrierungseintrag, der zwei Handler für Eigenschaftenblatterweiterungen für einen MyP-Beispieldateityp aktiviert. In diesem Beispiel wird für jede Seite ein separates -Objekt verwendet, aber es kann auch ein einzelnes -Objekt für beide verwendet werden.

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

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Schritt 2: Implementieren eines Eigenschaftenblatthandlers für einen Dateityp

Zusätzlich zur allgemeinen Implementierung, die unter Funktionsweise von [Eigenschaftenblatthandlern](propsheet-handlers.md)erläutert wird, muss ein Eigenschaftenblatthandler für einen Dateityp auch über eine entsprechende Implementierung der [**IShellPropSheetExt-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) verfügen. Nur die [**IShellPropSheetExt::AddPages-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) benötigt eine Nichttokenimplementierungen. Die Shell ruft [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage)nicht auf.

Die [**IShellPropSheetExt::AddPages-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) ermöglicht einem Eigenschaftenblatthandler das Hinzufügen einer Seite zu einem Eigenschaftenblatt. Die -Methode verfügt über zwei Eingabeparameter. Die erste , *lpfnAddPage,* ist ein Zeiger auf eine [*AddPropSheetPageProc-Rückruffunktion,*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) die verwendet wird, um der Shell die Informationen bereitzustellen, die zum Hinzufügen der Seite zum Eigenschaftenblatt erforderlich sind. Der zweite Wert, *lParam,* ist ein von der Shell definierter Wert, der nicht vom Handler verarbeitet wird. Sie wird einfach an die Shell übergeben, wenn die Rückruffunktion aufgerufen wird.

Das allgemeine Verfahren zum Implementieren von [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) lautet wie folgt.

**Implementieren der AddPages-Methode**

1.  Weisen Sie den Membern einer [**PROPSHEETPAGE-Struktur**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) entsprechende Werte zu. Dies gilt insbesondere für:
    -   Weisen Sie dem **pcRefParent-Member** die Variable zu, die den Verweiszähler des Handlers enthält. Diese Vorgehensweise verhindert, dass das Handlerobjekt entladen wird, während das Eigenschaftenblatt weiterhin angezeigt wird.
    -   Sie können auch eine [*PropSheetPageProc-Rückruffunktion*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) implementieren und ihren Zeiger einem **pfnCallback-Member** zuweisen. Diese Funktion wird aufgerufen, wenn die Seite erstellt wird und sie zerstört werden soll.
2.  Erstellen Sie das HPAGE-Handle der Seite, indem Sie die [**PROPSHEETPAGE-Struktur**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) an die [**CreatePropertySheetPage-Funktion**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) übergeben.
3.  Rufen Sie die Funktion auf, auf die *lpfnAddPage* zeigt. Legen Sie seinen ersten Parameter auf das HPAGE-Handle fest, das im vorherigen Schritt erstellt wurde. Legen Sie den zweiten Parameter auf den *lParam-Wert* fest, der von der Shell an [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) übergeben wurde.
4.  Alle Nachrichten, die der Seite zugeordnet sind, werden an die Dialogfeldprozedur übergeben, die dem **pfnDlgProc-Member** der [**PROPSHEETPAGE-Struktur**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) zugewiesen wurde.
5.  Wenn Sie **pfnCallback** eine [*PropSheetPageProc-Rückruffunktion*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) zugewiesen haben, wird sie aufgerufen, wenn die Seite zerstört werden soll. Der Handler kann dann alle erforderlichen Bereinigungsvorgänge ausführen, z. B. das Freigeben aller darin enthaltenen Verweise.

Das folgende Codebeispiel veranschaulicht eine einfache [**AddPages-Implementierung.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)


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



Die **g \_ hInst-Variable** ist das Instanzhandle für die DLL, und IDD \_ PAGEDLG ist die Ressourcen-ID der Dialogfeldvorlage der Seite. Die **PageDlgProc-Funktion** ist die Dialogfeldprozedur, die die Nachrichten der Seite verarbeitet. Die **g \_ DllRefCount-Variable** enthält den Verweiszähler des Objekts. Die [**AddPages-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) ruft [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) auf, um die Anzahl zu erhöhen. Der Verweiszähler wird jedoch von der Rückruffunktion **PageCallbackProc** freigegeben, wenn die Seite zerstört werden soll.

## <a name="remarks"></a>Hinweise

Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungshandlern finden Sie unter [Erstellen von Shellerweiterungshandlern.](handlers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
