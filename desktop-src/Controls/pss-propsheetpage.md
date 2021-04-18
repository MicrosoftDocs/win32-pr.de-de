---
title: PROPSHEETPAGE-Struktur (prsht. h)
description: Definiert eine Seite in einem Eigenschaften Blatt.
keywords:
- PROPSHEETPAGE-Struktur von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- PROPSHEETPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: cdde3f27900c7599b33af706d8fac9f9e8127b6f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106365879"
---
# <a name="propsheetpage-structure"></a>PROPSHEETPAGE-Struktur

Definiert eine Seite in einem Eigenschaften Blatt.

## <a name="syntax"></a>Syntax

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HINSTANCE  hInstance;
    union {
        LPCSTR                 pszTemplate;
        PROPSHEETPAGE_RESOURCE pResource;
    };
    union {
        HICON  hIcon;
        LPCSTR pszIcon;
    };
    LPCSTR          pszTitle;
    DLGPROC         pfnDlgProc;
    LPARAM          lParam;
    LPFNPSPCALLBACK pfnCallback;
    UINT            *pcRefParent;
    LPCTSTR         pszHeaderTitle;
    LPCTSTR         pszHeaderSubTitle;
    HANDLE          hActCtx;
    union 
    {
        HBITMAP     hbmHeader;
        LPCSTR      pszbmHeader;
    }
} PROPSHEETPAGE, *LPPROPSHEETPAGE;
```

## <a name="members"></a>Member

*dwSize* 

Typ: [DWORD](../winprog/windows-data-types.md)

Größe der-Struktur in Bytes.

*dwFlags* 

Typ: [DWORD](../winprog/windows-data-types.md)

Flags, die angeben, welche Optionen beim Erstellen der Eigenschaftenblattseite verwendet werden. Dieser Member kann eine Kombination der folgenden Werte sein.

| Wert | Bedeutung |
|-------|---------|
| PSP_DEFAULT | Verwendet die Standardbedeutung für alle Strukturmember. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird. |
| PSP_DLGINDIRECT | Erstellt die Seite aus der Dialogfeld Vorlage im Speicher, auf die der *presource* -Member verweist. Die [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) -Funktion geht davon aus, dass die Vorlage, die sich im Arbeitsspeicher befindet, nicht schreibgeschützt ist. Eine schreibgeschützte Vorlage führt in einigen Versionen von Windows zu einer Ausnahme. |
| PSP_HASHELP | Aktiviert die Schaltfläche " **Hilfe** " des Eigenschaften Blatts, wenn die Seite aktiv ist. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird. |
| PSP_HIDEHEADER | [Version 5,80](common-control-versions.md) und höher. Bewirkt, dass die Eigenschaften Seite des Assistenten den Header Bereich beim Auswählen der Seite ausblenden. Wenn ein Wasserzeichen angegeben wurde, wird es auf der linken Seite der Seite gezeichnet. Dieses Flag sollte für Willkommens-und Abschluss Seiten festgelegt und für innere Seiten ausgelassen werden. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird. |
| PSP_PREMATURE | [Version 4,71](common-control-versions.md) oder höher. Bewirkt, dass die Seite beim Erstellen des Eigenschaften Blatts erstellt wird. Wenn dieses Flag nicht angegeben wird, wird die Seite erst erstellt, wenn Sie zum ersten Mal ausgewählt wird. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird. |
| PSP_RTLREADING | Kehrt die Richtung um, in der " *psztitle* " angezeigt wird. Normal Fenster zeigt den gesamten Text, einschließlich *psztitle*, von links nach rechts (LTR) an. Für Sprachen, wie z. b. Hebräisch oder Arabisch, die von rechts nach links (RTL) gelesen wurden, kann ein Fenster gespiegelt werden, und der gesamte Text wird RTL angezeigt. Wenn PSP_RTLREADING festgelegt ist, liest *psztitle* stattdessen RTL in einem normalen übergeordneten Fenster und LTR in einem gespiegelten übergeordneten Fenster. |
| PSP_USECALLBACK | Ruft die Funktion auf, die vom *pfncallback* -Member angegeben wird, wenn die von dieser Struktur definierte Eigenschaften Blattseite erstellt oder zerstört wird. |
| PSP_USEFUSIONCONTEXT | [Version 6,0](common-control-versions.md) und höher. Verwenden Sie einen Aktivierungs Kontext. Wenn Sie einen Aktivierungs Kontext verwenden möchten, müssen Sie dieses Flag festlegen und " *hactctx*" das Aktivierungs Kontext Handle zuweisen. Siehe Hinweise. |
| PSP_USEHEADERSUBTITLE | [Version 5,80](common-control-versions.md) oder höher. Zeigt die Zeichenfolge an, auf die vom *pszheaderunter Titel* -Member als Untertitel des Header Bereichs einer Wizard97 Seite verwiesen wird. Um dieses Flag zu verwenden, müssen Sie auch das PSH_WIZARD97-Flag im *dwFlags* -Member der zugeordneten [propsheeder](pss-propsheetheader.md) -Struktur festlegen. Das PSP_USEHEADERSUBTITLE-Flag wird ignoriert, wenn PSP_HIDEHEADER festgelegt ist. Im Aero-Assistenten wird der Titel am oberen Rand des Client Bereichs angezeigt. |
| PSP_USEHEADERTITLE | [Version 5,80](common-control-versions.md) oder höher. Zeigt die Zeichenfolge an, auf die der *pszheadertitle* -Member als Titel in der Kopfzeile einer Wizard97-inneren Seite zeigt. Sie müssen auch das PSH_WIZARD97-Flag im *dwFlags* -Member der zugeordneten [propsheedie Ader](pss-propsheetheader.md) -Struktur festlegen. Das PSP_USEHEADERTITLE-Flag wird ignoriert, wenn PSP_HIDEHEADER festgelegt ist. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird. |
| PSP_USEHICON | Verwendet *HICON* als kleines Symbol auf der Registerkarte für die Seite. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird.  |
| PSP_USEICONID | Verwendet *pszicon* als Namen der zu ladenden Symbol Ressource und wird als kleines Symbol auf der Registerkarte der Seite verwendet. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird. |
| PSP_USEREFPARENT | Verwaltet den Verweis Zähler, der vom *pkrefparent* -Element für die Lebensdauer der von dieser Struktur erstellten Eigenschaften Blattseite angegeben wird. |
| PSP_USETITLE | Verwendet das *psztitle* -Element als Titel des Eigenschaften Blatts-Dialog Felds anstelle des Titels, der in der Dialogfeld Vorlage gespeichert ist. Dieses Flag wird nicht unterstützt, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird. |

*hInstance* 

Typ: [HINSTANCE](../winprog/windows-data-types.md)

Handle für die-Instanz, aus der eine Symbol-oder Zeichen folgen Ressource geladen werden soll. Wenn das Element *pszicon*, *psztitle*, *pszheadertitle* oder *pszheaderunter Titel* eine zu ladende Ressource identifiziert, muss *HINSTANCE* angegeben werden.

*psztemplate* 

Typ: [LPCSTR](../winprog/windows-data-types.md)

Dialog Feld Vorlage, die zum Erstellen der Seite verwendet werden soll. Dieser Member kann entweder den Ressourcen Bezeichner der Vorlage oder die Adresse einer Zeichenfolge angeben, die den Namen der Vorlage angibt. Wenn das PSP_DLGINDIRECT-Flag im *dwFlags* -Member festgelegt ist, wird *psztemplate* ignoriert. Dieser Member wird als Union with *presource* deklariert.

*vorab Quelle* 

Geben Sie Folgendes ein: **lpcdlgtemplate**

Zeiger auf eine Dialogfeld Vorlage im Speicher. Die [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) -Funktion geht davon aus, dass die Vorlage nicht schreibgeschützt ist. Eine schreibgeschützte Vorlage führt in einigen Versionen von Windows zu einer Ausnahme. Wenn Sie diesen Member verwenden möchten, müssen Sie das PSP_DLGINDIRECT-Flag im *dwFlags* -Member festlegen. Dieser Member wird als Union mit *psztemplate* deklariert.

*hIcon* 

Typ: [HICON](../winprog/windows-data-types.md)

Handle für das Symbol, das als Symbol auf der Registerkarte der Seite verwendet werden soll. Wenn der *dwFlags* -Member keine PSP_USEHICON enthält, wird dieser Member ignoriert. Dieser Member wird als Union mit *pszicon* deklariert.

*pszicon* 

Typ: [LPCSTR](../winprog/windows-data-types.md)

Symbol Ressource, die als Symbol auf der Registerkarte der Seite verwendet werden soll. Dieser Member kann entweder den Bezeichner der Symbol Ressource oder die Adresse der Zeichenfolge angeben, die den Namen der Symbol Ressource angibt. Wenn Sie diesen Member verwenden möchten, müssen Sie das PSP_USEICONID-Flag im *dwFlags* -Member festlegen. Dieser Member wird als Union mit *HICON* deklariert.

*psztitle* 

Typ: [LPCSTR](../winprog/windows-data-types.md)

Der Titel des Eigenschaften Blatts-Dialog Felds. Dieser Titel überschreibt den in der Dialogfeld Vorlage angegebenen Titel. Dieser Member kann entweder den Bezeichner einer Zeichen folgen Ressource oder die Adresse einer Zeichenfolge angeben, die den Titel angibt. Wenn Sie diesen Member verwenden möchten, müssen Sie das PSP_USETITLE-Flag im *dwFlags* -Member festlegen.

*pfndlgproc* 

Typ: **DlgProc**

Zeiger auf die Dialogfeld Prozedur für die Seite. Da die Seiten als nicht modante Dialogfelder erstellt werden, darf die Dialogfeld Prozedur die [EndDialog](/windows/win32/api/winuser/nf-winuser-enddialog) -Funktion nicht aufzurufen.

*lParam* 

Typ: [LPARAM](../winprog/windows-data-types.md)

Wenn die Seite erstellt wird, wird eine Kopie der **PROPSHEETPAGE** -Struktur der Seite mit einer [WM_INITDIALOG](/windows/win32/dlgbox/wm-initdialog) Meldung an die Dialogfeld Prozedur übermittelt. Das *LPARAM* -Element wird bereitgestellt, damit Sie anwendungsspezifische Informationen an die Dialogfeld Prozedur übergeben können. Dies hat keine Auswirkungen auf die eigentliche Seite.

*pfncallback* 

Typ: **lpfnpspcallback**

Zeiger auf eine Anwendungs definierte Rückruffunktion, die aufgerufen wird, wenn die Seite erstellt wird, und wenn Sie gelöscht werden soll. Weitere Informationen zur Rückruffunktion finden Sie unter [lpfnpspcallbacka callback function](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka). Wenn Sie diesen Member verwenden möchten, müssen Sie das PSP_USECALLBACK-Flag im *dwFlags* -Member festlegen.

*pkref Parent* 

Typ: [uint *](../winprog/windows-data-types.md)

Zeiger auf den Verweis zählungs Wert. Wenn Sie diesen Member verwenden möchten, müssen Sie das PSP_USEREFPARENT-Flag im *dwFlags* -Member festlegen.

> [!NOTE]
> Wenn eine Eigenschaften Blattseite erstellt wird, wird der Wert, auf den von *pkrefparent* verwiesen wird, inkrementiert. Sie erstellen eine Eigenschaften Blattseite implizit, indem Sie das PSH_PROPSHEETPAGE-Flag im *dwFlags* -Member von [propsheeder Ader](pss-propsheetheader.md) festlegen und die [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) -Funktion aufrufen. Sie können dies explizit mithilfe der Funktion "Funktion" von " [kreatepropertysheetpage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) " erreichen. Wenn eine Eigenschaften Blattseite zerstört wird, wird der Wert, auf den der *pkrefparent* -Member verweist, verringert. Dies erfolgt automatisch, wenn das Eigenschaften Blatt zerstört wird. Sie können eine Eigenschaften Blattseite mithilfe der [destroypropertysheetpage](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage) -Funktion explizit zerstören.

*pszheadertitle* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) oder höher. Titel des Header Bereichs. Um dieses Element im Wizard97-Assistenten zu verwenden, müssen Sie auch die folgenden Schritte ausführen:

* Legen Sie das PSP_USEHEADERTITLE-Flag im *dwFlags* -Member fest.
* Legen Sie das PSH_WIZARD97-Flag im *dwFlags* -Member der [propsheeder](pss-propsheetheader.md) -Struktur der Seite fest.
* Stellen Sie sicher, dass das PSP_HIDEHEADER-Flag im *dwFlags* -Member nicht festgelegt ist.

*pszheaderuntertitel* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) oder höher. Untertitel des Header Bereichs. Um dieses Element zu verwenden, müssen Sie die folgenden Schritte ausführen:

* Legen Sie das PSP_USEHEADERSUBTITLE-Flag im *dwFlags* -Member fest.
* Legen Sie das PSH_WIZARD97-Flag im *dwFlags* -Member der [propsheeder](pss-propsheetheader.md) -Struktur der Seite fest.
* Stellen Sie sicher, dass das PSP_HIDEHEADER-Flag im *dwFlags* -Member nicht festgelegt ist.

> [!NOTE]
> Dieser Member wird ignoriert, wenn der Aero-Style-Assistent ([PSH_AEROWIZARD](pss-propsheetheader.md)) verwendet wird.

*hactctx* 

Typ: [handle](../winprog/windows-data-types.md)

[Version 6,0](common-control-versions.md) oder höher. Ein Aktivierungs Kontext handle. Legen Sie diesen Member auf das Handle fest, das zurückgegeben wird, wenn Sie den Aktivierungs Kontext mit " [kreateactctx](/windows/win32/api/winbase/nf-winbase-createactctxa)" erstellen. Das System aktiviert diesen Kontext, bevor das Dialogfeld erstellt wird. Sie müssen diesen Member nicht verwenden, wenn Sie ein globales Manifest verwenden.

*hbmheader* 

Typ: [hBitmap](../winprog/windows-data-types.md)

Dieser Member wird als Union mit *pszbmheader* deklariert.

*pszbmheader*

Typ: [LPCSTR](../winprog/windows-data-types.md)

Dieser Member wird als Union mit *hbmheader* deklariert.

## <a name="remarks"></a>Bemerkungen

Comctl32.dll Version 6 und höher ist nicht Verteil Bar. Wenn Sie Comctl32.dll Version 6 oder höher verwenden möchten, geben Sie die DLL-Datei in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows Vista \[ -Desktop-Apps\]                                    |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\]                              |
| Header                   | Prsht. h |
| Unicode- und ANSI-Name                   | **Propsheetheiaderw** (Unicode) und **propshee-Adera** (ANSI) |
