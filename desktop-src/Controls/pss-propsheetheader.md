---
title: PROPSHEETHEADER-Struktur (Prsht.h)
description: Definiert den Rahmen und die Seiten eines Eigenschaftenblatts.
keywords:
- PROPSHEETHEADER-Struktur Windows Steuerelementen
topic_type:
- apiref
api_name:
- PROPSHEETHEADER
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 719982c1e17ab74dc5c624352625d226f8f4bef90ae84dce4f2b85d5dc2713f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085120"
---
# <a name="propsheetheader--structure"></a>PROPSHEETHEADER-Struktur

Definiert den Rahmen und die Seiten eines Eigenschaftenblatts.

## <a name="syntax"></a>Syntax

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HWND       hwndParent;
    HINSTANCE  hInstance;
    union {
        HICON   hIcon;
        LPCTSTR pszIcon;
    };
    LPCTSTR  pszCaption;
    UINT     nPages;
    union {
        UINT    nStartPage;
        LPCTSTR pStartPage;
    };
    union {
        LPCPROPSHEETPAGE ppsp;
        HPROPSHEETPAGE   *phpage;
    };
    PFNPROPSHEETCALLBACK pfnCallback;
    union {
        HBITMAP hbmWatermark;
        LPCTSTR pszbmWatermark;
    };
    HPALETTE  hplWatermark;
    union {
        HBITMAP hbmHeader;
        LPCSTR  pszbmHeader;
    };
} PROPSHEETHEADER, *LPPROPSHEETHEADER;
```

## <a name="members"></a>Member

*dwSize* 

Typ: [DWORD](../winprog/windows-data-types.md)

Größe dieser Struktur in Bytes. Der Eigenschaftenblatt-Manager verwendet diesen Member, um zu bestimmen, welche Version der **PROPSHEETHEADER-Struktur** Sie verwenden. Weitere Informationen finden Sie in den Hinweisen.

*dwFlags* 

Typ: [DWORD](../winprog/windows-data-types.md)

Flags, die angeben, welche Optionen beim Erstellen der Eigenschaftenblattseite verwendet werden. Dieser Member kann eine Kombination der folgenden Werte sein.

| Wert | Bedeutung |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Verwendet die Standardbe bedeutung für alle Strukturmitglieder und erstellt ein normales Eigenschaftenblatt. Dieses Flag hat den Wert 0 (null) und wird nicht mit anderen Flags kombiniert. |
| PSH_AEROWIZARD (0x00004000) | [Version 6.00](common-control-versions.md) und höher. Erstellt ein Eigenschaftenblatt des Assistenten, das den Stil Von Der Stil verwendet. Das PSH_WIZARD flag muss ebenfalls festgelegt werden. Das Singlethread-Apartmentmodell (STA) muss verwendet werden. |
| PSH_HASHELP (0x00000200) | Ermöglicht es Eigenschaftenblattseiten, eine **Hilfeschaltfläche** anzuzeigen. Sie müssen auch das PSP_HASHELP in der [PROPSHEETPAGE-Struktur](pss-propsheetpage.md) der Seite festlegen, wenn die Seite erstellt wird. Wenn eine der anfänglichen Eigenschaftenblattseiten eine Hilfeschaltfläche **aktiviert,** PSH_HASHELP automatisch festgelegt. Wenn keine der ersten  Seiten eine Hilfeschaltfläche aktiviert, müssen Sie PSH_HASHELP explizit festlegen, wenn Sie Hilfeschaltflächen auf allen Seiten verwenden möchten, die später hinzugefügt werden können. Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD.|
| PSH_HEADER (0x00080000) | [Version 5.80](common-control-versions.md) und höher. Gibt an, dass eine Headerbitmap mit einem Wizard97-Assistenten verwendet wird. Sie müssen auch das PSH_WIZARD97 festlegen. Wenn das PSH_USEHBMHEADER festgelegt ist, wird die Headerbitmap vom *hbmHeader-Member* erhalten. Andernfalls wird die Headerbitmap aus dem *ps bitmapmHeader-Member* erhalten. Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD. |
| PSH_HEADERBITMAP (0x08000000) | [Version 6.00](common-control-versions.md) und höher. Das *ps bitmapmHeader-Element* gibt eine Bitmap an, die im Headerbereich angezeigt wird. Muss in Kombination mit der PSH_AEROWIZARD. |
| PSH_MODELESS (0x00000400) | Bewirkt, [dass die PropertySheet-Funktion](/windows/win32/api/prsht/nf-prsht-propertysheeta) das Eigenschaftenblatt nicht als modales Dialogfeld, sondern als modusloses Dialogfeld erstellt. Wenn dieses Flag festgelegt ist, gibt [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) unmittelbar nach dem Erstellen des Dialogfelds zurück, und der Rückgabewert von [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) ist das Fensterhand handle für das Eigenschaftenblattdialogfeld. Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD. |
| PSH_NOAPPLYNOW (0x00000080) | Entfernt die **Schaltfläche Anwenden.** Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD. |
| PSH_NOCONTEXTHELP (0x02000000) | [Version 5.80](common-control-versions.md) und höher. Entfernt die kontextsensitive Hilfeschaltfläche ("?"), die in der Regel auf der Beschriftungsleiste von Eigenschaftenblättern vorhanden ist. Dieses Flag ist für Assistenten ungültig. Unter [About Property Sheets (Informationen zu Eigenschaftenblättern)](property-sheets.md) erfahren Sie, wie Sie die Hilfeschaltfläche der Beschriftungsleiste für frühere Versionen der allgemeinen Steuerelemente entfernen.  Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD. |
| PSH_NOMARGIN (0x10000000) | [Version 6.00](common-control-versions.md) oder höher. Gibt an, dass kein Rand zwischen der Seite und dem Frame eingefügt wird. Muss in Kombination mit der PSH_AEROWIZARD. |
| PSH_PROPSHEETPAGE (0x00000008) | Verwendet den *ppsp-Member* und ignoriert den *phpage-Member* beim Erstellen der Seiten für das Eigenschaftenblatt. |
| PSH_PROPTITLE (0x00000001) | Gibt an, *dass pszCaption* der Name des Dings ist, für das Eigenschaften angezeigt werden. Windows eine versions- und sprachabhängige Anpassung an die Beschriftung vor. Im Englischen wird beispielsweise der Ausdruck "Properties for" einer nicht leeren *pszCaption* voranstehenden (und wenn *pszCaption* eine leere Beschriftung erzeugt, ist der Titel einfach "Properties"). Wenn dieses Flag weggelassen wird, wird pszCaption unverändert verwendet.  |
| PSH_RESIZABLE (0x04000000) | Ermöglicht das Ändern der Größe des Assistenten durch den Benutzer. Schaltflächen zum Maximieren und Minimieren werden im Rahmen des Assistenten angezeigt, und der Frame kann siziert werden. Um dieses Flag verwenden zu können, müssen Sie auch PSH_AEROWIZARD. |
| PSH_RTLREADING (0x00000800) | Legt das Eigenschaftenblatt oder Assistentenfenster auf die Lese reihenfolge von rechts nach links (RTL) fest, die für Sprachen wie Hebräisch und Arabisch geeignet ist. Wenn dieses Flag nicht angegeben ist, wird für Eigenschaftenblattfenster standardmäßig die Lese reihenfolge von links nach rechts (LTR) verwendet, und Assistentenfenster stimmen mit der Lese reihenfolge der aktuellen Seite überein. |
| PSH_STRETCHWATERMARK (0x00040000) | Streckt das Wasserzeichen in Assistenten im Assistenten97-Stil. Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD. Dieses Formatflag ist nur enthalten, um Abwärtskompatibilität für bestimmte Anwendungen zu gewährleisten. Die Verwendung wird nicht empfohlen, und sie wird nur von den gängigen Steuerelementversionen 4.0 und 4.01 unterstützt. Bei allgemeinen Steuerelementen ab Version 5.80 wird dieses Flag ignoriert. |
| PSH_USECALLBACK (0x00000100) | Ruft die funktion auf, die durch den *pfnCallback-Parameter angegeben* wird, wenn bestimmte Ereignisse auftreten. Weitere Informationen finden Sie in der Beschreibung der [PFNPROPSHEETCALLBACK-Rückruffunktion.](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) |
| PSH_USEHBMHEADER (0x00100000) | [Version 5.80](common-control-versions.md). Erhält die Headerbitmap aus dem *hbmHeader-Member* anstelle des *ps bitmapmHeader-Members.* Sie müssen auch entweder das PSH_AEROWIZARD-Flag oder das PSH_WIZARD97-Flag zusammen mit dem PSH_HEADER festlegen. |
| PSH_USEHBMWATERMARK (0x00010000) | [Version 5.80](common-control-versions.md). Erhält die Wasserzeichenbitmap aus dem *hbmWatermark-Member* anstelle des *ps bitmapmWatermark-Members.* Sie müssen auch die PSH_WIZARD97 und PSH_WATERMARK. Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD. |
| PSH_USEHICON (0x00000002) | Verwendet *hIcon* als kleines Symbol in der Titelleiste des Eigenschaftenblattdialogfelds. |
| PSH_USEHPLWATERMARK (0x00020000) | [Version 5.80](common-control-versions.md). Verwendet die **HPALETTE-Struktur,** auf die das *hplWatermark-Member* verweist, anstelle der Standardpalette, um die Wasserzeichenbitmap und/oder Headerbitmap für einen Wizard97-Assistenten zu zeichnen. Sie müssen auch die PSH_WIZARD97 festlegen und PSH_WATERMARK oder PSH_HEADER. Dieses Flag wird in Verbindung mit der -PSH_AEROWIZARD.  |
| PSH_USEICONID (0x00000004) | Verwendet *pszIcon* als Namen der zu ladende Symbolressource und verwendet als kleines Symbol in der Titelleiste des Eigenschaftenblattdialogfelds. |
| PSH_USEPAGELANG (0x00200000) | [Version 5.80.](common-control-versions.md) Gibt an, dass die Sprache für das Eigenschaftenblatt aus der Ressource der ersten Seite übernommen wird. Diese Seite muss durch den Ressourcenbezeichner angegeben werden. |
| PSH_USEPSTARTPAGE (0x00000040) | Verwendet das *pStartPage-Element* anstelle des *nStartPage-Members,* wenn die Anfangsseite des Eigenschaftenblatts angezeigt wird. |
| PSH_WATERMARK (0x00008000) | [Version 5.80.](common-control-versions.md) Gibt an, dass eine Wasserzeichenbitmap mit einem Wizard97-Assistenten auf Seiten mit dem PSP_HIDEHEADER Stil verwendet wird. Sie müssen auch das flag PSH_WIZARD97 festlegen. Die Wasserzeichenbitmap wird aus dem *pschildmWatermark-Element* abgerufen, es sei denn, PSH_USEHBMWATERMARK ist festgelegt. In diesem Fall wird die Headerbitmap vom *hbmWatermark-Member* abgerufen. Dieses Flag wird in Verbindung mit PSH_AEROWIZARD nicht unterstützt.  |
| PSH_WIZARD (0x00000020) | Erstellt ein Eigenschaftenblatt des Assistenten. Wenn Sie PSH_AEROWIZARD verwenden, müssen Sie dieses Flag auch festlegen. |
| PSH_WIZARD97 (0x01000000) | [Version 5.80.](common-control-versions.md) Erstellt ein Eigenschaftenblatt im Stil wizard97, das Bitmaps im Header der inneren Seiten und auf der linken Seite von äußeren Seiten unterstützt. Dieses Flag wird in Verbindung mit PSH_AEROWIZARD nicht unterstützt. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Fügt eine kontextbezogene **Hilfeschaltfläche** ("?") hinzu, die in der Regel in der Beschriftungsleiste eines Assistenten nicht vorhanden ist. Dieses Flag ist für reguläre Eigenschaftenblätter ungültig. Dieses Flag wird in Verbindung mit PSH_AEROWIZARD nicht unterstützt. |
| PSH_WIZARDHASFINISH (0x00000010)  | Zeigt immer die Schaltfläche **Fertig stellen** im Assistenten an. Sie müssen auch entweder PSH_WIZARD, PSH_WIZARD97 oder PSH_AEROWIZARD festlegen. |
| PSH_WIZARD_LITE (0x00400000) | [Version 5.80.](common-control-versions.md) Verwendet den Stil Wizard-lite. Dieser Stil ähnelt der Darstellung PSH_WIZARD97, wird aber ähnlich wie PSH_WIZARD implementiert. Es gibt einige Einschränkungen hinsichtlich der Formatierung der Seiten. Es gibt z. B. keine erzwungenen Rahmen, und der PSH_WIZARD_LITE Format zeichnet die Wasserzeichen- und Headerbitmaps nicht für Sie so wie Wizard97. Dieses Flag wird in Verbindung mit PSH_AEROWIZARD nicht unterstützt. |

*hwndParent* 

Typ: [HWND](../winprog/windows-data-types.md)

Handle für das Besitzerfenster des Eigenschaftenblatts.

*hInstance* 

Typ: [HINSTANCE](../winprog/windows-data-types.md)

Handle für die Instanz, aus der das Symbol, die Titelzeichenfolgenressource, der Startseitenname, die Headerbitmap oder das Wasserzeichen geladen werden sollen. Wenn das *PszIcon-,* *pszCaption-,* *pStartPage-,* *pschildmHeader-* oder *pschildmWatermark-Element* eine zu ladende Ressource identifiziert, muss dieser Member angegeben werden.

*hIcon* 

Typ: [HICON](../winprog/windows-data-types.md)

Greifen Sie auf das Symbol zu, das als kleines Symbol in der Titelleiste des Eigenschaftenblattdialogfelds verwendet werden soll. Dieser Member wird verwendet, wenn das *dwFlags-Element* PSH_USEHICON enthält. Dieser Member wird mit *pszIcon* als Union deklariert.

*pszIcon* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

Symbolressource, die als kleines Symbol in der Titelleiste des Eigenschaftenblattdialogfelds verwendet werden soll. Dieser Member wird verwendet, wenn das *dwFlags-Element* PSH_USEICONID enthält. Dieser Member kann entweder den Bezeichner der Symbolressource oder die Adresse der Zeichenfolge angeben, die den Namen der Symbolressource angibt. In beiden Fällen wird das Symbol aus der -Instanz geladen, die vom *hInstance-Member* bereitgestellt wird. Dieser Member wird mit *hIcon* als Union deklariert.

*pszCaption* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

Titel des Dialogfelds "Eigenschaftenblatt". Dieser Member kann entweder den Bezeichner einer Zeichenfolgenressource (geladen aus der vom *hInstance-Member* angegebenen Instanz) oder die Adresse einer Zeichenfolge angeben, die den Titel angibt. Wenn der *dwFlags-Member* PSH_PROPTITLE enthält, wird die Zeichenfolge **Eigenschaften für** am Anfang des Titels eingefügt. Dieses Feld wird für Assistenten97 ignoriert. Bei Einem Assistenten wird die Zeichenfolge allein für die Beschriftung verwendet, unabhängig davon, ob das PSH_PROPTITLE-Flag festgelegt ist.

*nPages* 

Typ: [UINT](../winprog/windows-data-types.md)

Anzahl der Eigenschaftenblattseiten, die entweder im *ppsp-* oder *phpage-Array* bereitgestellt werden.

*nStartPage* 

Typ: [UINT](../winprog/windows-data-types.md)

Nullbasierter Index der anfangs angezeigten Seite, wenn das Eigenschaftenblattdialogfeld erstellt wird. Dieser Member wird verwendet, wenn der *dwFlags-Member* das flag PSH_USEPSTARTPAGE nicht enthält. Dieser Member wird mit *pStartPage* als Union deklariert.

*pStartPage* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

Name der Anfangsseite, die beim Erstellen des Eigenschaftenblattdialogfelds angezeigt wird. Dieser Member wird verwendet, wenn der *dwFlags-Member* das flag PSH_USESTARTPAGE enthält. Dieser Member kann entweder den Bezeichner einer Zeichenfolgenressource (geladen aus der vom *hInstance-Member* angegebenen Instanz) oder die Adresse einer Zeichenfolge angeben, die den Namen angibt. Der Name der Startseite wird mit den Beschriftungen der Seiten abgegleichen. Dieser Member wird mit *nStartPage* als Union deklariert.

*ppsp* 

Typ: **LPCPROPSHEETPAGE**

Zeiger auf ein Array von [PROPSHEETPAGE-Strukturen,](pss-propsheetpage.md) die die Seiten im Eigenschaftenblatt definieren. Wenn der *dwFlags-Member* PSH_PROPSHEETPAGE nicht enthält, wird dieser Member ignoriert. Beachten Sie, dass die **PROPSHEETPAGE-Struktur** eine variable Größe aufweist. Anwendungen, die das Array analysieren, auf das *ppsp* zeigt, müssen die Größe jeder Seite berücksichtigen. Dieser Member wird als Union mit *phpage* deklariert.

*phpage* 

Typ: **HPROPSHEETPAGE \***

Zeiger auf ein Array von Handles auf die Eigenschaftenblattseiten. Dieser Member wird verwendet, wenn der *dwFlags-Member* keine PSH_PROPSHEETPAGE enthält. Jedes Handle muss durch einen vorherigen Aufruf der [CreatePropertySheetPage-Funktion](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) erstellt worden sein. Wenn die [PropertySheet-Funktion](/windows/win32/api/prsht/nf-prsht-propertysheeta) zurückgegeben wird, wurden alle HPROPSHEETPAGE-Handles im *phpage-Array* zerstört. Dieser Member wird als Union mit *ppsp* deklariert.

*pfnCallback* 

Typ: **PFNPROPSHEETCALLBACK**

Zeiger auf eine anwendungsdefinierte Rückruffunktion, die aufgerufen wird, wenn bestimmte Ereignisse auftreten. Weitere Informationen zur Rückruffunktion finden Sie in der Beschreibung der [RÜCKRUFFUNKTION PFNPROPSHEETCALLBACK.](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) Wenn der *dwFlags-Member* keine PSH_USECALLBACK enthält, wird dieser Member ignoriert.

*hbmWatermark* 

Typ: [HBITMAP](../winprog/windows-data-types.md)

[Version 5.80](common-control-versions.md) oder höher. Handle für die Wasserzeichenbitmap. Wenn der *dwFlags-Member* keine PSH_USEHBMWATERMARK enthält, wird dieser Member ignoriert.

*psautomatmWatermark* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

[Version 5.80](common-control-versions.md) oder höher. Bitmapressource, die als Wasserzeichen verwendet werden soll. Dieser Member kann entweder den Bezeichner der Bitmapressource oder die Adresse der Zeichenfolge angeben, die den Namen der Bitmapressource angibt. Wenn das *dwFlags-Element* PSH_USEHBMWATERMARK enthält, wird dieser Member ignoriert.

*hplWatermark*

Typ: [HPALETTE](../winprog/windows-data-types.md)

[Version 5.80](common-control-versions.md) oder höher. **HPALETTE-Struktur,** die zum Zeichnen der Wasserzeichenbitmap und/oder Headerbitmap verwendet wird. Wenn der *dwFlags-Member* keine PSH_USEHPLWATERMARK enthält, wird dieser Member ignoriert.

*hbmHeader*

Typ: [HBITMAP](../winprog/windows-data-types.md)

[Version 5.80](common-control-versions.md) oder höher. Handle für die Headerbitmap. Wenn der *dwFlags-Member* PSH_USEHBMHEADER nicht enthält, wird dieser Member ignoriert.

*psautomatmHeader*

Typ: [LPCSTR](../winprog/windows-data-types.md)

[Version 5.80](common-control-versions.md) oder höher. Bitmapressource, die als Header verwendet werden soll. Dieser Member kann entweder den Bezeichner der Bitmapressource oder die Adresse der Zeichenfolge angeben, die den Namen der Bitmapressource angibt. Wenn das *dwFlags-Element* PSH_USEHBMHEADER enthält, wird dieses Element ignoriert.

## <a name="remarks"></a>Hinweise

Wenn der Benutzer eine Einstellung wie große Schriftarten ausgibt, die das Dialogfeld vergrößert, wird auch das Wasserzeichen vergrößert, das auf den Start- und Endseiten gezeichnet wird. Größe und Position der ursprünglichen Bitmap bleiben unverändert. Der zusätzliche Bereich wird mit der Farbe des Pixels in der linken oberen Ecke der Bitmap gefüllt.

Die Stile PSH_WIZARD, PSH_WIZARD97 und PSH_WIZARD_LITE sind gegenseitig inkompatibel. Es sollte nur eines dieser Stilflags festgelegt werden. PSH_AEROWIZARD sollten mit PSH_WIZARD kombiniert werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows \[Nur Vista-Desktop-Apps\]                                    |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\]                              |
| Header                   | Prsht.h |
| Unicode- und ANSI-Name                   | **PROPSHEETHEADERW** (Unicode) und **PROPSHEETHEADERA** (ANSI) |
