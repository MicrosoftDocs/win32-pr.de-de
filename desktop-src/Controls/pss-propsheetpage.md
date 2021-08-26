---
title: PROPSHEETPAGE-Struktur (Prsht.h)
description: Definiert eine Seite in einem Eigenschaftenblatt.
keywords:
- PROPSHEETPAGE-Struktur Windows Steuerelementen
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
ms.openlocfilehash: 1c1be3b6240f024b5aeee4a4d7a9d308cdb6572ae5080db00b3d05da30e02306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914460"
---
# <a name="propsheetpage-structure"></a>PROPSHEETPAGE-Struktur

Definiert eine Seite in einem Eigenschaftenblatt.

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

Größe dieser Struktur in Bytes.

*dwFlags* 

Typ: [DWORD](../winprog/windows-data-types.md)

Flags, die angeben, welche Optionen beim Erstellen der Eigenschaftenblattseite verwendet werden. Dieser Member kann eine Kombination der folgenden Werte sein.

| Wert | Bedeutung |
|-------|---------|
| PSP_DEFAULT | Verwendet die Standardbe bedeutung für alle Strukturmitglieder. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md) |
| PSP_DLGINDIRECT | Erstellt die Seite aus der Dialogfeldvorlage im Arbeitsspeicher, auf die das *pResource-Mitglied zeigt.* Die [PropertySheet-Funktion](/windows/win32/api/prsht/nf-prsht-propertysheeta) geht davon aus, dass die Vorlage im Arbeitsspeicher nicht schreibgeschützt ist. Eine schreibgeschützte Vorlage verursacht eine Ausnahme in einigen Versionen Windows. |
| PSP_HASHELP | Aktiviert die **Hilfeschaltfläche** des Eigenschaftenblatts, wenn die Seite aktiv ist. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md) |
| PSP_HIDEHEADER | [Version 5.80](common-control-versions.md) und höher. Bewirkt, dass das Eigenschaftenblatt des Assistenten den Headerbereich ausblendet, wenn die Seite ausgewählt ist. Wenn ein Wasserzeichen angegeben wurde, wird es links auf der Seite gestrichen. Dieses Flag sollte für Begrüßungs- und Vervollständigungsseiten festgelegt und für innere Seiten weggelassen werden. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md) |
| PSP_PREMATURE | [Version 4.71](common-control-versions.md) oder höher. Bewirkt, dass die Seite erstellt wird, wenn das Eigenschaftenblatt erstellt wird. Wenn dieses Flag nicht angegeben wird, wird die Seite erst erstellt, wenn sie zum ersten Mal ausgewählt wird. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md) |
| PSP_RTLREADING | Kehrt die Richtung um, in der *pszTitle* angezeigt wird. Normale Fenster zeigen den ganzen Text an, einschließlich *pszTitle*, von links nach rechts (LTR). Für Sprachen wie Hebräisch oder Arabisch, die von rechts nach links (RTL) lesen, kann ein Fenster gespiegelt werden, und der ganze Text wird angezeigt. Wenn PSP_RTLREADING festgelegt ist, liest *pszTitle* stattdessen RTL in einem normalen übergeordneten Fenster und LTR in einem gespiegelten übergeordneten Fenster. |
| PSP_USECALLBACK | Ruft die Funktion auf, die vom *pfnCallback-Member beim* Erstellen oder Zerstören der durch diese Struktur definierten Eigenschaftenblattseite angegeben wird. |
| PSP_USEFUSIONCONTEXT | [Version 6.0](common-control-versions.md) und höher. Verwenden Sie einen Aktivierungskontext. Um einen Aktivierungskontext zu verwenden, müssen Sie dieses Flag festlegen und *hActCtx* das Aktivierungskontexthand handle zuweisen. Weitere Informationen finden Sie in den Anmerkungen. |
| PSP_USEHEADERSUBTITLE | [Version 5.80](common-control-versions.md) oder höher. Zeigt die Zeichenfolge an, auf die das *pszHeaderSubTitle-Member* als Untertitel des Headerbereichs einer Wizard97-Seite zeigt. Um dieses Flag zu verwenden, müssen Sie auch das PSH_WIZARD97 im *dwFlags-Member* der zugeordneten [PROPSHEETHEADER-Struktur](pss-propsheetheader.md) festlegen. Das PSP_USEHEADERSUBTITLE-Flag wird ignoriert, wenn PSP_HIDEHEADER festgelegt ist. In Assistenten im Stil von Stilen wird der Titel am oberen Ende des Clientbereichs angezeigt. |
| PSP_USEHEADERTITLE | [Version 5.80](common-control-versions.md) oder höher. Zeigt die Zeichenfolge an, auf die das *pszHeaderTitle-Member* als Titel im Header einer inneren Seite von Wizard97 zeigt. Sie müssen auch das PSH_WIZARD97 im *dwFlags-Member* der zugeordneten [PROPSHEETHEADER-Struktur](pss-propsheetheader.md) festlegen. Das PSP_USEHEADERTITLE-Flag wird ignoriert, wenn PSP_HIDEHEADER festgelegt ist. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md) |
| PSP_USEHICON | Verwendet *hIcon* als kleines Symbol auf der Registerkarte für die Seite. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md)  |
| PSP_USEICONID | Verwendet *pszIcon* als Namen der Symbolressource zum Laden und Verwenden als kleines Symbol auf der Registerkarte für die Seite. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md) |
| PSP_USEREFPARENT | Behält die vom *pcRefParent-Element* angegebene Verweisanzahl für die Lebensdauer der Eigenschaftenblattseite bei, die aus dieser Struktur erstellt wurde. |
| PSP_USETITLE | Verwendet das *pszTitle-Member* als Titel des Eigenschaftenblattdialogfelds anstelle des in der Dialogfeldvorlage gespeicherten Titels. Dieses Flag wird nicht unterstützt, wenn der Assistent im Stil von Stil[(PSH_AEROWIZARD) verwendet wird.](pss-propsheetheader.md) |

*hInstance* 

Typ: [HINSTANCE](../winprog/windows-data-types.md)

Handle für die Instanz, aus der ein Symbol oder eine Zeichenfolgenressource geladen werden soll. Wenn das *pszIcon-,* *pszTitle-,* *pszHeaderTitle-* oder *pszHeaderSubTitle-Member* eine zu ladende Ressource identifiziert, muss *hInstance* angegeben werden.

*pszTemplate* 

Typ: [LPCSTR](../winprog/windows-data-types.md)

Dialogfeldvorlage, die zum Erstellen der Seite verwendet werden soll. Dieser Member kann entweder den Ressourcenbezeichner der Vorlage oder die Adresse einer Zeichenfolge angeben, die den Namen der Vorlage angibt. Wenn das PSP_DLGINDIRECT im *dwFlags-Member* festgelegt ist, *wird pszTemplate* ignoriert. Dieser Member wird als Union mit *pResource deklariert.*

*pResource* 

Typ: **LPCDLGTEMPLATE**

Zeiger auf eine Dialogfeldvorlage im Arbeitsspeicher. Die [PropertySheet-Funktion](/windows/win32/api/prsht/nf-prsht-propertysheeta) geht davon aus, dass die Vorlage nicht schreibgeschützt ist. Eine schreibgeschützte Vorlage verursacht eine Ausnahme in einigen Versionen Windows. Um diesen Member zu verwenden, müssen Sie das PSP_DLGINDIRECT im *dwFlags-Member* festlegen. Dieser Member wird als Union mit *pszTemplate deklariert.*

*hIcon* 

Typ: [HICON](../winprog/windows-data-types.md)

Handle für das Symbol, das als Symbol auf der Registerkarte der Seite verwendet werden soll. Wenn das *dwFlags-Member* keine PSP_USEHICON, wird dieser Member ignoriert. Dieser Member wird als Union mit *pszIcon deklariert.*

*pszIcon* 

Typ: [LPCSTR](../winprog/windows-data-types.md)

Symbolressource, die als Symbol auf der Registerkarte der Seite verwendet werden soll. Dieses Element kann entweder den Bezeichner der Symbolressource oder die Adresse der Zeichenfolge angeben, die den Namen der Symbolressource angibt. Um diesen Member zu verwenden, müssen Sie das PSP_USEICONID im *dwFlags-Member* festlegen. Dieser Member wird als Union mit *hIcon deklariert.*

*pszTitle* 

Typ: [LPCSTR](../winprog/windows-data-types.md)

Titel des Eigenschaftenblattdialogfelds. Dieser Titel überschreibt den in der Dialogfeldvorlage angegebenen Titel. Dieser Member kann entweder den Bezeichner einer Zeichenfolgenressource oder die Adresse einer Zeichenfolge angeben, die den Titel angibt. Um diesen Member zu verwenden, müssen Sie das PSP_USETITLE im *dwFlags-Member* festlegen.

*pfnDlgProc* 

Typ: **DLGPROC**

Zeiger auf die Dialogfeldprozedur für die Seite. Da die Seiten als nicht moduslose Dialogfelder erstellt werden, darf die Dialogfeldprozedur die [EndDialog-Funktion nicht](/windows/win32/api/winuser/nf-winuser-enddialog) aufrufen.

*lParam* 

Typ: [LPARAM](../winprog/windows-data-types.md)

Wenn die Seite erstellt wird, wird eine Kopie der **PROPSHEETPAGE-Struktur** der Seite an die Dialogfeldprozedur mit einer WM_INITDIALOG [übergeben.](../dlgbox/wm-initdialog.md) Das *lParam-Member* wird bereitgestellt, damit Sie anwendungsspezifische Informationen an die Dialogfeldprozedur übergeben können. Dies hat keine Auswirkungen auf die eigentliche Seite.

*pfnCallback* 

Typ: **LPFNPSPCALLBACK**

Zeiger auf eine anwendungsdefinierte Rückruffunktion, die aufgerufen wird, wenn die Seite erstellt und zerstört wird. Weitere Informationen zur Rückruffunktion finden Sie unter [LPFNPSPCALLBACKA-Rückruffunktion.](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) Um diesen Member zu verwenden, müssen Sie das PSP_USECALLBACK im *dwFlags-Member* festlegen.

*pcRefParent* 

Typ: [UINT*](../winprog/windows-data-types.md)

Zeiger auf den Verweiszählerwert. Um diesen Member zu verwenden, müssen Sie das PSP_USEREFPARENT im *dwFlags-Member* festlegen.

> [!NOTE]
> Wenn eine Eigenschaftenblattseite erstellt wird, wird der Wert, auf den *pcRefParent* zeigt, inkrementiert. Sie erstellen implizit eine Eigenschaftenblattseite, indem Sie das PSH_PROPSHEETPAGE-Flag im *dwFlags-Member* von [PROPSHEETHEADER](pss-propsheetheader.md) festlegen und die [PropertySheet-Funktion](/windows/win32/api/prsht/nf-prsht-propertysheeta) aufrufen. Sie können dies explizit mithilfe der [CreatePropertySheetPage-Funktion](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) tun. Wenn eine Eigenschaftenblattseite zerstört wird, wird der Wert, auf den das *pcRefParent-Element* zeigt, dekrementiert. Dies erfolgt automatisch, wenn das Eigenschaftenblatt zerstört wird. Sie können eine Eigenschaftenblattseite explizit mithilfe der [DestroyPropertySheetPage-Funktion](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage) zerstören.

*pszHeaderTitle* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

[Version 5.80](common-control-versions.md) oder höher. Titel des Headerbereichs. Um dieses Mitglied im Assistenten im Assistenten97-Stil zu verwenden, müssen Sie auch folgende Schritte ausführen:

* Legen Sie das PSP_USEHEADERTITLE im *dwFlags-Member* fest.
* Legen Sie PSH_WIZARD97 im *dwFlags-Member* der [PROPSHEETHEADER-Struktur](pss-propsheetheader.md) der Seite fest.
* Stellen Sie sicher, PSP_HIDEHEADER flag im *dwFlags-Member* nicht festgelegt ist.

*pszHeaderSubTitle* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

[Version 5.80](common-control-versions.md) oder höher. Untertitel des Headerbereichs. Gehen Sie wie folgt vor, um diesen Member zu verwenden:

* Legen Sie das PSP_USEHEADERSUBTITLE im *dwFlags-Member* fest.
* Legen Sie PSH_WIZARD97 im *dwFlags-Member* der [PROPSHEETHEADER-Struktur](pss-propsheetheader.md) der Seite fest.
* Stellen Sie sicher, PSP_HIDEHEADER flag im *dwFlags-Member* nicht festgelegt ist.

> [!NOTE]
> Dieser Member wird ignoriert, wenn der Assistent im Stil von Stil ( PSH_AEROWIZARD ) verwendet[wird.](pss-propsheetheader.md)

*hActCtx* 

Typ: [HANDLE](../winprog/windows-data-types.md)

[Version 6.0](common-control-versions.md) oder höher. Ein Aktivierungskontexthand handle. Legen Sie diesen Member auf das Handle fest, das zurückgegeben wird, wenn Sie den Aktivierungskontext mit [CreateActCtx erstellen.](/windows/win32/api/winbase/nf-winbase-createactctxa) Das System aktiviert diesen Kontext, bevor das Dialogfeld erstellt wird. Sie müssen diesen Member nicht verwenden, wenn Sie ein globales Manifest verwenden.

*hbmHeader* 

Typ: [HBITMAP](../winprog/windows-data-types.md)

Dieser Member wird als Union mit *psmusheader deklariert.*

*pswittmHeader*

Typ: [LPCSTR](../winprog/windows-data-types.md)

Dieser Member wird als Union mit *hbmHeader deklariert.*

## <a name="remarks"></a>Hinweise

Comctl32.dll Version 6 und höher sind nicht verteilbar. Um Version Comctl32.dll 6 oder höher zu verwenden, geben Sie die .dll in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ Vista-Desktop-Apps\]                                    |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\]                              |
| Header                   | Prsht.h |
| Unicode- und ANSI-Name                   | **PROPSHEETHEADERW** (Unicode) und **PROPSHEETHEADERA** (ANSI) |