---
title: Propsheetheiader-Struktur (prsht. h)
description: Definiert den Frame und die Seiten eines Eigenschaften Blatts.
keywords:
- Propsheetheiader-Struktur Windows-Steuerelemente
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
ms.openlocfilehash: 90a11ff727b491a1801f8071e28c39a3a6594408
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106361258"
---
# <a name="propsheetheader--structure"></a>Propsheetheiader-Struktur

Definiert den Frame und die Seiten eines Eigenschaften Blatts.

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

Größe der-Struktur in Bytes. Der Eigenschaften Blatt-Manager verwendet diesen Member, um zu bestimmen, welche Version der **propsheederader** -Struktur Sie verwenden. Weitere Informationen finden Sie in den Hinweisen.

*dwFlags* 

Typ: [DWORD](../winprog/windows-data-types.md)

Flags, die angeben, welche Optionen beim Erstellen der Eigenschaftenblattseite verwendet werden. Dieser Member kann eine Kombination der folgenden Werte sein.

| Wert | Bedeutung |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Verwendet die Standardbedeutung für alle Strukturmember und erstellt ein normales Eigenschaften Blatt. Dieses Flag hat den Wert 0 (null) und wird nicht mit anderen Flags kombiniert. |
| PSH_AEROWIZARD (0x00004000) | [Version 6,00](common-control-versions.md) und höher. Erstellt ein Assistenten-Eigenschaften Blatt, das den Aero-Stil verwendet. Das PSH_WIZARD-Flag muss ebenfalls festgelegt werden. Das STA-Modell (Single Thread-Apartment) muss verwendet werden. |
| PSH_HASHELP (0x00000200) | Ermöglicht es Eigenschaften Blattseiten, eine **Hilfe** Schaltfläche anzuzeigen. Sie müssen auch das PSP_HASHELP-Flag in der [PROPSHEETPAGE](pss-propsheetpage.md) -Struktur der Seite festlegen, wenn die Seite erstellt wird. Wenn eine der ersten Seiten des Eigenschaften Blatts eine **Hilfe** Schaltfläche aktiviert, wird PSH_HASHELP automatisch festgelegt. Wenn keine der ersten Seiten eine **Hilfe** Schaltfläche aktiviert, müssen Sie PSH_HASHELP explizit festlegen, wenn Sie über Hilfe Schaltflächen auf Seiten verfügen möchten, die später hinzugefügt werden können. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt.|
| PSH_HEADER (0x00080000) | [Version 5,80](common-control-versions.md) und höher. Gibt an, dass eine Header Bitmap mit einem Wizard97-Assistenten verwendet wird. Sie müssen auch das PSH_WIZARD97-Flag festlegen. Wenn das PSH_USEHBMHEADER-Flag festgelegt ist, wird die Header Bitmap aus dem *hbmheader* -Element abgerufen. Andernfalls wird die Header Bitmap aus dem *pszbmheader* -Member abgerufen. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |
| PSH_HEADERBITMAP (0x08000000) | [Version 6,00](common-control-versions.md) und höher. Der *pszbmheader* -Member gibt eine Bitmap an, die im Header Bereich angezeigt wird. Muss in Kombination mit PSH_AEROWIZARD verwendet werden. |
| PSH_MODELESS (0x00000400) | Bewirkt, dass die [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) -Funktion das Eigenschaften Blatt als nicht modales Dialogfeld, sondern als nicht modales Dialogfeld erstellt. Wenn dieses Flag festgelegt ist, wird [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) unmittelbar nach dem Erstellen des Dialog Felds zurückgegeben, und der Rückgabewert von [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) ist das Fenster Handle für das Eigenschaften Blatt-Dialogfeld. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |
| PSH_NOAPPLYNOW (0x00000080) | Entfernt die Schaltfläche **anwenden** . Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |
| PSH_NOCONTEXTHELP (0x02000000) | [Version 5,80](common-control-versions.md) und höher. Entfernt die kontextbezogene Hilfe Schaltfläche ("?"), die in der Regel auf der Titelleiste der Eigenschaften Blätter vorhanden ist. Dieses Flag ist für Assistenten ungültig. Eine Erläuterung zum Entfernen der **Hilfe** Schaltfläche der Beschriftungs Leiste für frühere Versionen der allgemeinen Steuerelemente finden Sie unter [Informationen zu Eigenschaften Blättern](property-sheets.md) . Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |
| PSH_NOMARGIN (0x10000000) | [Version 6,00](common-control-versions.md) oder höher. Gibt an, dass kein Rand zwischen der Seite und dem Frame eingefügt wird. Muss in Kombination mit PSH_AEROWIZARD verwendet werden. |
| PSH_PROPSHEETPAGE (0x00000008) | Verwendet das *PPSP* -Element und ignoriert den *phpage* -Member, wenn die Seiten für das Eigenschaften Blatt erstellt werden. |
| PSH_PROPTITLE (0x00000001) | Gibt an, dass *pszcaption* der Name des Objekts ist, für das Eigenschaften angezeigt werden. Windows stellt eine Versions-und sprachabhängige Anpassung der Beschriftung dar. Beispielsweise wird in englischer Sprache der Ausdruck "Properties for" einem nicht leeren *pszcaption* vorangestellt (und wenn *pszcaption* eine leere Beschriftung erzeugt, ist der Titel einfach "Properties"). Wenn dieses Flag weggelassen wird, wird die pszcaption unverändert verwendet.  |
| PSH_RESIZABLE (0x04000000) | Ermöglicht, dass die Größe des Assistenten vom Benutzer geändert wird. Die Schaltflächen "maximieren" und "minimieren" werden im Rahmen des Assistenten angezeigt, und der Frame ist gleich Um dieses Flag verwenden zu können, müssen Sie auch PSH_AEROWIZARD festlegen. |
| PSH_RTLREADING (0x00000800) | Legt das Eigenschaften Blatt oder das Assistenten Fenster auf die Lesereihenfolge von rechts nach links (RTL) fest, die für Sprachen wie Hebräisch und Arabisch geeignet ist. Wenn dieses Flag nicht angegeben wird, werden die Eigenschaften Blatt Fenster standardmäßig von links nach rechts (LTR) gelesen, und die Fenster des Assistenten stimmen mit der Lesereihenfolge der aktuellen Seite ab. |
| PSH_STRETCHWATERMARK (0x00040000) | Streckt das Wasserzeichen in Wizard97-Assistenten. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. Dieses stilflag ist nur enthalten, um Abwärtskompatibilität für bestimmte Anwendungen bereitzustellen. Die Verwendung wird nicht empfohlen und wird nur von den Common Controls-Versionen 4,0 und 4,01 unterstützt. Bei Common Controls, Version 5,80 und höher, wird dieses Flag ignoriert. |
| PSH_USECALLBACK (0x00000100) | Ruft die Funktion auf, die vom *pfncallback* -Parameter angegeben wird, wenn bestimmte Ereignisse auftreten. Weitere Informationen finden Sie in der Beschreibung der [pfnpropsheetcallback](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) -Rückruffunktion. |
| PSH_USEHBMHEADER (0x00100000) | [Version 5,80](common-control-versions.md). Ruft die Header Bitmap aus dem *hbmheader* -Member anstelle des *pszbmheader* -Members ab. Sie müssen auch das PSH_AEROWIZARD-Flag oder das PSH_WIZARD97-Flag mit dem PSH_HEADER-Flag festlegen. |
| PSH_USEHBMWATERMARK (0x00010000 bis) | [Version 5,80](common-control-versions.md). Ruft das Wasserzeichen Bitmap vom Member " *hbmwatermark* " anstelle des *pszbmwatermark* -Members ab. Außerdem müssen Sie PSH_WIZARD97 und PSH_WATERMARK festlegen. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |
| PSH_USEHICON (0x00000002) | Verwendet *HICON* als kleines Symbol in der Titelleiste des Dialog Felds Eigenschaften Seite. |
| PSH_USEHPLWATERMARK (0x00020000) | [Version 5,80](common-control-versions.md). Verwendet die **hpalette** -Struktur, auf die durch den *hplwatermark* -Member verwiesen wird, anstelle der Standardpalette, um das Wasserzeichen Bitmap und/oder die Header Bitmap für einen Wizard97-Assistenten zu zeichnen. Außerdem müssen Sie PSH_WIZARD97 und PSH_WATERMARK oder PSH_HEADER festlegen. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt.  |
| PSH_USEICONID (0x00000004) | Verwendet *pszicon* als Namen der zu ladenden Symbol Ressource und als kleines Symbol in der Titelleiste des Eigenschaften Blatts-Dialog Felds. |
| PSH_USEPAGELANG (0x00200000) | [Version 5,80](common-control-versions.md). Gibt an, dass die Sprache für das Eigenschaften Blatt aus der Ressource der ersten Seite entnommen wird. Diese Seite muss durch den Ressourcen Bezeichner angegeben werden. |
| PSH_USEPSTARTPAGE (0x00000040) | Verwendet den *pstartpage* -Member anstelle des *nstartpage* -Members, wenn die Anfangs Seite des Eigenschaften Blatts angezeigt wird. |
| PSH_WATERMARK (0x00008000) | [Version 5,80](common-control-versions.md). Gibt an, dass eine Wasserzeichen-Bitmap mit einem Wizard97-Assistenten auf Seiten mit dem PSP_HIDEHEADER Stil verwendet wird. Sie müssen auch das PSH_WIZARD97-Flag festlegen. Die Wasserzeichen-Bitmap wird vom *pszbmwatermark* -Element abgerufen, es sei denn, PSH_USEHBMWATERMARK festgelegt ist. In diesem Fall wird die Header Bitmap aus dem *hbmwatermark* -Element abgerufen. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt.  |
| PSH_WIZARD (0x00000020) | Erstellt ein Eigenschaften Blatt für den Assistenten. Wenn Sie PSH_AEROWIZARD verwenden, müssen Sie auch dieses Flag festlegen. |
| PSH_WIZARD97 (0x01000000) | [Version 5,80](common-control-versions.md). Erstellt ein Wizard97-Eigenschaften Blatt, das Bitmaps in der Kopfzeile von inneren Seiten und auf der linken Seite von äußeren Seiten unterstützt. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Fügt eine kontextabhängige **Hilfe** Schaltfläche ("?") hinzu, die normalerweise nicht in der Titelleiste eines Assistenten vorhanden ist. Dieses Flag ist für reguläre Eigenschaften Blätter ungültig. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |
| PSH_WIZARDHASFINISH (0x00000010)  | Zeigt immer die Schaltfläche **Fertig** stellen im Assistenten an. Sie müssen auch entweder PSH_WIZARD, PSH_WIZARD97 oder PSH_AEROWIZARD festlegen. |
| PSH_WIZARD_LITE (0x00400000) | [Version 5,80](common-control-versions.md). Verwendet den Wizard-Lite-Stil. Dieser Stil ähnelt dem Aussehen in PSH_WIZARD97, aber er ist ähnlich wie PSH_WIZARD implementiert. Es gibt einige Einschränkungen hinsichtlich der Formatierung der Seiten. Zum Beispiel gibt es keine erzwungenen Rahmen, und der PSH_WIZARD_LITE Stil zeichnet nicht das Wasserzeichen und die Header Bitmaps für Sie wie Wizard97. Dieses Flag wird nicht in Verbindung mit PSH_AEROWIZARD unterstützt. |

*hwndParent* 

Typ: [HWND](../winprog/windows-data-types.md)

Handle für das Besitzer Fenster des Eigenschaften Blatts.

*hInstance* 

Typ: [HINSTANCE](../winprog/windows-data-types.md)

Handle für die-Instanz, von der das Symbol, die Titel Zeichen folgen Ressource, der Name der Startseite, die Header Bitmap oder das Wasserzeichen geladen werden soll. Wenn das Element *pszicon*, *pszcaption*, *pstartpage*, *pszbmheader* oder *pszbmwatermark* eine zu ladende Ressource identifiziert, muss dieser Member angegeben werden.

*hIcon* 

Typ: [HICON](../winprog/windows-data-types.md)

Handle für das Symbol, das als kleines Symbol in der Titelleiste des Dialog Felds Eigenschaften Seite verwendet werden soll. Dieser Member wird verwendet, wenn der *dwFlags* -Member PSH_USEHICON enthält. Dieser Member wird als Union mit *pszicon* deklariert.

*pszicon* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

Symbol Ressource, die als kleines Symbol in der Titelleiste des Dialog Felds Eigenschaften Seite verwendet werden soll. Dieser Member wird verwendet, wenn der *dwFlags* -Member PSH_USEICONID enthält. Dieser Member kann entweder den Bezeichner der Symbol Ressource oder die Adresse der Zeichenfolge angeben, die den Namen der Symbol Ressource angibt. In beiden Fällen wird das Symbol aus der-Instanz geladen, die vom *HINSTANCE* -Member bereitgestellt wird. Dieser Member wird als Union mit *HICON* deklariert.

*pszcaption* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

Der Titel des Eigenschaften Blatts-Dialog Felds. Dieser Member kann entweder den Bezeichner einer Zeichen folgen Ressource (geladen von der-Instanz, die vom *HINSTANCE* -Member angegeben wird) oder die Adresse einer Zeichenfolge angeben, die den Titel angibt. Wenn der *dwFlags* -Member PSH_PROPTITLE einschließt, werden die Zeichen folgen **Eigenschaften für** am Anfang des Titels eingefügt. Dieses Feld wird für Wizard97-Assistenten ignoriert. Bei Aero-Assistenten wird die Zeichenfolge allein für die Beschriftung verwendet, unabhängig davon, ob das PSH_PROPTITLE-Flag festgelegt ist.

*npages* 

Typ: [uint](../winprog/windows-data-types.md)

Anzahl der Eigenschaften Blattseiten, die im *PPSP* -oder *phpage* -Array bereitgestellt werden.

*nstartpage* 

Typ: [uint](../winprog/windows-data-types.md)

NULL basierter Index der Anfangs Seite, die beim Erstellen des Eigenschaften Blatt Dialogfelds angezeigt wird. Dieser Member wird verwendet, wenn das *dwFlags* -Element das PSH_USEPSTARTPAGE-Flag nicht einschließt. Dieser Member wird als Union mit *pstartpage* deklariert.

*pstartpage* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

Der Name der Anfangs Seite, die angezeigt wird, wenn das Dialogfeld Eigenschaften Blatt erstellt wird. Dieser Member wird verwendet, wenn der *dwFlags* -Member das PSH_USESTARTPAGE-Flag enthält. Dieser Member kann entweder den Bezeichner einer Zeichen folgen Ressource (geladen von der-Instanz, die vom *HINSTANCE* -Member angegeben wird) oder die Adresse einer Zeichenfolge angeben, die den Namen angibt. Der Name der Startseite wird mit den Beschriftungen der Seiten abgeglichen. Dieser Member wird als Union mit *nstartpage* deklariert.

*PPSP* 

Typ: **lpcpropsheetpage**

Zeiger auf ein Array von [PROPSHEETPAGE](pss-propsheetpage.md) -Strukturen, die die Seiten im Eigenschaften Blatt definieren. Wenn der *dwFlags* -Member keine PSH_PROPSHEETPAGE enthält, wird dieser Member ignoriert. Beachten Sie, dass die **PROPSHEETPAGE** -Struktur variabel ist. Anwendungen, die das Array analysieren, auf das von *PPSP* verwiesen wird, müssen die Größe der einzelnen Seiten berücksichtigen. Dieser Member wird als Union mit *phpage* deklariert.

*phpage* 

Typ: **hpropsheetpage \***

Zeiger auf ein Array von Handles für die Eigenschaften Blattseiten. Dieser Member wird verwendet, wenn der *dwFlags* -Member keine PSH_PROPSHEETPAGE enthält. Jedes Handle muss von einem vorherigen aufrufsbefehl der Funktion " [foratepropertysheetpage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) " erstellt worden sein. Wenn die [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) -Funktion zurückgibt, werden alle hpropsheetpage-Handles im *phpage* -Array zerstört. Dieser Member wird als Union mit *PPSP* deklariert.

*pfncallback* 

Typ: **pfnpropsheetcallback**

Zeiger auf eine Anwendungs definierte Rückruffunktion, die aufgerufen wird, wenn bestimmte Ereignisse auftreten. Weitere Informationen zur Rückruffunktion finden Sie in der Beschreibung der [pfnpropsheetcallback](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) -Rückruffunktion. Wenn der *dwFlags* -Member keine PSH_USECALLBACK enthält, wird dieser Member ignoriert.

*hbmwatermark* 

Typ: [hBitmap](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) oder höher. Handle für das Wasserzeichen Bitmap. Wenn der *dwFlags* -Member keine PSH_USEHBMWATERMARK enthält, wird dieser Member ignoriert.

*pszbmwatermark* 

Typ: [LPCTSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) oder höher. Bitmap-Ressource, die als Wasserzeichen verwendet werden soll. Dieser Member kann entweder den Bezeichner der Bitmap-Ressource oder die Adresse der Zeichenfolge angeben, die den Namen der Bitmapressource angibt. Wenn der *dwFlags* -Member PSH_USEHBMWATERMARK enthält, wird dieser Member ignoriert.

*hplwatermark*

Typ: [hpalette](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) oder höher. **Hpalette** -Struktur zum Zeichnen der Bitmap-und/oder Header Bitmap für das Wasserzeichen. Wenn der *dwFlags* -Member keine PSH_USEHPLWATERMARK enthält, wird dieser Member ignoriert.

*hbmheader*

Typ: [hBitmap](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) oder höher. Handle für die Header Bitmap. Wenn der *dwFlags* -Member keine PSH_USEHBMHEADER enthält, wird dieser Member ignoriert.

*pszbmheader*

Typ: [LPCSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) oder höher. Die als Header zu verwendende Bitmap-Ressource. Dieser Member kann entweder den Bezeichner der Bitmap-Ressource oder die Adresse der Zeichenfolge angeben, die den Namen der Bitmapressource angibt. Wenn der *dwFlags* -Member PSH_USEHBMHEADER enthält, wird dieser Member ignoriert.

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer eine Einstellung (z. b. große Schriftarten) auswählt, die das Dialogfeld vergrößert, wird auch das Wasserzeichen, das auf den Start-und Abschluss Seiten gezeichnet wird, vergrößert. Die Größe und Position der ursprünglichen Bitmap bleiben unverändert. Der zusätzliche Bereich wird mit der Farbe des Pixels in der oberen linken Ecke der Bitmap gefüllt.

Die PSH_WIZARD-, PSH_WIZARD97-und PSH_WIZARD_LITE Stile sind gegenseitig inkompatibel. Nur eines dieser stilflags sollte festgelegt werden. PSH_AEROWIZARD sollten mit PSH_WIZARD kombiniert werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows Vista \[ -Desktop-Apps\]                                    |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\]                              |
| Header                   | Prsht. h |
| Unicode- und ANSI-Name                   | **Propsheetheiaderw** (Unicode) und **propshee-Adera** (ANSI) |
