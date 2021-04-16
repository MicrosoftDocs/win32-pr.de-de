---
title: Dlgtemplateex-Struktur
description: Eine erweiterte Dialogfeld Vorlage beginnt mit einem dlgtemplateex-Header, der das Dialogfeld beschreibt und die Anzahl der Steuerelemente im Dialogfeld angibt.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Dialog Felder der dlgtemplateex-Struktur
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518353"
---
# <a name="dlgtemplateex-structure"></a>Dlgtemplateex-Struktur

Eine erweiterte Dialogfeld Vorlage beginnt mit einem **dlgtemplateex** -Header, der das Dialogfeld beschreibt und die Anzahl der Steuerelemente im Dialogfeld angibt. Für jedes Steuerelement in einem Dialogfeld verfügt eine erweiterte Dialogfeld Vorlage über einen Datenblock, der das [**dlgitemtemplateex**](dlgitemtemplateex.md) -Format verwendet, um das Steuerelement zu beschreiben.

Die **dlgtemplateex** -Struktur ist in keiner Standard Header Datei definiert. Die Struktur Definition wird hier bereitgestellt, um das Format einer erweiterten Vorlage für ein Dialogfeld zu erläutern.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a>Member

<dl> <dt>

**dlgver**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Versionsnummer der erweiterten Dialogfeld Vorlage. Dieser Member muss auf 1 festgelegt werden.

</dd> <dt>

**Signatur**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Gibt an, ob eine Vorlage eine erweiterte Dialogfeld Vorlage ist. Wenn die **Signatur** "0xFFFF" ist, handelt es sich um eine erweiterte Dialogfeld Vorlage. In diesem Fall gibt das **dlgver** -Mitglied die Versionsnummer der Vorlage an. Wenn **Signature** ein anderer Wert als 0xFFFF ist, handelt es sich hierbei um eine Standard Dialogfeld Vorlage, die die [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) -Struktur und die [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -Struktur verwendet.

</dd> <dt>

**HelpID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Hilfe Kontext Bezeichner für das Dialogfeld Fenster. Wenn das System eine [**WM- \_ Hilfe**](../shell/wm-help.md) Nachricht sendet, übergibt es diesen Wert an den **wcontextid** -Member der [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur.

</dd> <dt>

**exStyle**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die erweiterten Windows-Stile. Dieser Member wird nicht zum Erstellen von Dialogfeldern verwendet, aber Anwendungen, die Dialogfeld Vorlagen verwenden, können ihn verwenden, um andere Fenstertypen zu erstellen. Eine Liste der Werte finden Sie unter [**Erweiterte Fenster Stile**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Stil des Dialog Felds. Dieser Member kann eine Kombination aus [Fenster Stil Werten](/windows/desktop/winmsg/window-styles) und [Dialogfeld-Stil Werten](dialog-box-styles.md)sein.

Wenn **Style** den Formatvorlagen Stil **DS \_ setFont** oder **DS \_ shellfont** enthält, enthält der **dlgtemplateex** -Header der erweiterten Dialogfeld Vorlage vier zusätzliche Member ( **pointsize**, **Weight**, **kursiv** und Font **),** die die Schriftart beschreiben, die für den Text im Client Bereich und die Steuerelemente des Dialog Felds verwendet werden soll. Wenn möglich, erstellt das System eine Schriftart entsprechend den Werten, die in diesen Membern angegeben sind. Anschließend sendet das System eine [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht an das Dialogfeld und an jedes Steuerelement, um ein Handle für die Schriftart bereitzustellen.

Weitere Informationen finden Sie unter [Dialog Feld Schriftarten](about-dialog-boxes.md).

</dd> <dt>

**cdlgitems**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der Steuerelemente im Dialogfeld.

</dd> <dt>

**x**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die x-Koordinate der oberen linken Ecke des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

**y**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die y-Koordinate der oberen linken Ecke des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

**verschoben**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die Breite des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

**CY**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die Höhe des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

**stehen**
</dt> <dd>

Typ: **SZ \_ oder \_ Ord**

</dd> <dd>

Ein Array variabler Länge mit 16-Bit-Elementen, das eine Menü Ressource für das Dialogfeld angibt. Wenn das erste Element dieses Arrays 0x0000 ist, enthält das Dialogfeld kein Menü, und das Array enthält keine anderen Elemente. Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer Menü Ressource in einer ausführbaren Datei angibt. Wenn das erste Element einen anderen Wert aufweist, behandelt das System das Array als eine NULL-terminierte Unicode-Zeichenfolge, die den Namen einer Menü Ressource in einer ausführbaren Datei angibt.

</dd> <dt>

**windowClass**
</dt> <dd>

Typ: **SZ \_ oder \_ Ord**

</dd> <dd>

Ein Array variabler Länge mit 16-Bit-Elementen, das die Fenster Klasse des Dialog Felds angibt. Wenn das erste Element des Arrays 0x0000 ist, verwendet das System die vordefinierte Dialogfeld Klasse für das Dialogfeld, und das Array enthält keine anderen Elemente. Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer vordefinierten System Fenster Klasse angibt. Wenn das erste Element einen anderen Wert aufweist, behandelt das System das Array als eine NULL-terminierte Unicode-Zeichenfolge, die den Namen einer registrierten Fenster Klasse angibt.

</dd> <dt>

**title**
</dt> <dd>

Typ: **WCHAR \[ titlelen \]**

</dd> <dd>

Der Titel des Dialogfelds. Wenn das erste Element dieses Arrays 0x0000 ist, enthält das Dialogfeld keinen Titel, und das Array enthält keine anderen Elemente.

</dd> <dt>

**pointsize**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Punktgröße der Schriftart, die für den Text im Dialogfeld und dessen Steuerelemente verwendet werden soll.

Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.

</dd> <dt>

**weight**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Gewichtung der Schriftart. Beachten Sie, dass die Werte, die für den **lfWeight** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur aufgeführt sind, zwar alle Werte sein können **\_**

Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.

</dd> <dt>

**Kursiv**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Gibt an, ob die Schriftart kursiv formatiert ist. Wenn dieser Wert **true** ist, wird die Schriftart kursiv formatiert.

Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.

</dd> <dt>

**charset**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Der zu verwendende Zeichensatz. Weitere Informationen finden Sie unter dem **lfCharSet** -Member von [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).

Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.

</dd> <dt>

**Gotik**
</dt> <dd>

Typ: **WCHAR \[ stringlen \]**

</dd> <dd>

Der Name der Schriftart für die Schriftart.

Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können eine erweiterte Dialogfeld Vorlage anstelle einer Standard Dialogfeld Vorlage [**in den Funktionen**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)"" von "", "", " [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)", "-param", "Funktionen [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)" und " [**dialogboxindirekte**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) " verwenden.

Im Anschluss an den **dlgtemplateex** -Header in einer erweiterten Dialogfeld Vorlage handelt es sich um eine oder mehrere [**dlgitemtemplateex**](dlgitemtemplateex.md) -Strukturen, die die Steuerelemente des Dialog Felds beschreiben. Der **cdlgitems** -Member der **dlgitemtemplateex** -Struktur gibt die Anzahl der **dlgitemtemplateex** -Strukturen an, die in der Vorlage befolgt werden.

Jede [**dlgitemtemplateex**](dlgitemtemplateex.md) -Struktur in der Vorlage muss an einer **DWORD** -Grenze ausgerichtet sein. Wenn der **stilmember** den **DS- \_ setFont** - **oder DS- \_ shellfont** -Stil angibt, beginnt die erste **dlgitemtemplateex** -Struktur an der ersten **DWORD** -Grenze hinter der **Schriftart** Zeichenfolge. Wenn diese Stile nicht angegeben werden, beginnt die erste Struktur an der ersten **DWORD** -Grenze hinter der **Titel** Zeichenfolge.

Die Arrays " **Menu**", " **WindowClass**", " **Title**" und " **Schriftart** " müssen an **Wort** Grenzen ausgerichtet werden.

Wenn Sie Zeichen folgen in den Feldern " **Menü**", " **WindowClass**", " **Title**" und " **Schriftart** " angeben, müssen Sie Unicode-Zeichen folgen verwenden. Verwenden Sie die [**Multibyte-**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) Funktion, um diese Unicode-Zeichen folgen aus ANSI-Zeichen folgen zu generieren.

Die Member **x**, **y**, **CX** und **CY** geben Werte in Dialogfeld Einheiten an. Sie können diese Werte mithilfe der [**mapdialogrect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) -Funktion in Bildschirm Einheiten (Pixel) konvertieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**"Kreatedialogindirect"**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**"Kreatedialogindirectparam"**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**Dialogboxindirekte**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**Dialogboxderedereparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**Dlgitemtemplateex**](dlgitemtemplateex.md)
</dt> <dt>

[**Mapdialogrect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**"LogFont"**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar muss**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

