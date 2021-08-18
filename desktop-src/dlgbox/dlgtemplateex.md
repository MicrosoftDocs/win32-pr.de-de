---
title: DLGTEMPLATEEX-Struktur
description: Eine vorlage für erweiterte Dialogfelder beginnt mit einem DLGTEMPLATEEX-Header, der das Dialogfeld beschreibt und die Anzahl der Steuerelemente im Dialogfeld angibt.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- DLGTEMPLATEEX-Strukturdialogfelder
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab23b93a72edb2da6784797dd47bdfb4a839e2e9ce662adfc6ffbe09e468ac17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503451"
---
# <a name="dlgtemplateex-structure"></a>DLGTEMPLATEEX-Struktur

Eine vorlage für erweiterte Dialogfelder beginnt mit einem **DLGTEMPLATEEX-Header,** der das Dialogfeld beschreibt und die Anzahl der Steuerelemente im Dialogfeld angibt. Für jedes Steuerelement in einem Dialogfeld verfügt eine vorlage für erweiterte Dialogfelder über einen Datenblock, der das [**DLGITEMTEMPLATEEX-Format**](dlgitemtemplateex.md) verwendet, um das Steuerelement zu beschreiben.

Die **DLGTEMPLATEEX-Struktur** ist in keiner Standardheaderdatei definiert. Die Strukturdefinition wird hier bereitgestellt, um das Format einer erweiterten Vorlage für ein Dialogfeld zu erläutern.

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

**dlgVer**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Versionsnummer der Vorlage für erweiterte Dialogfelder. Dieser Member muss auf 1 festgelegt werden.

</dd> <dt>

**Signatur**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Gibt an, ob eine Vorlage eine vorlage für erweiterte Dialogfelder ist. Wenn **die Signatur** 0xFFFF ist, handelt es sich um eine erweiterte Dialogfeldvorlage. In diesem Fall gibt der **dlgVer-Member** die Versionsnummer der Vorlage an. Wenn **signatur** ein anderer Wert als 0xFFFF ist, handelt es sich hierbei um eine Standarddialogfeldvorlage, die die [**DLGTEMPLATE-**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) und [**DLGITEMTEMPLATE-Strukturen**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) verwendet.

</dd> <dt>

**helpID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Hilfekontextbezeichner für das Dialogfeldfenster. Wenn das System eine [**WM \_ HELP-Nachricht**](../shell/wm-help.md) sendet, übergibt es diesen Wert im **wContextId-Member** der [**HELPINFO-Struktur.**](/windows/win32/api/winuser/ns-winuser-helpinfo)

</dd> <dt>

**exStyle**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die erweiterten Fensterstile. Dieser Member wird beim Erstellen von Dialogfeldern nicht verwendet, aber Anwendungen, die Dialogfeldvorlagen verwenden, können ihn verwenden, um andere Arten von Fenstern zu erstellen. Eine Liste der Werte finden Sie unter [**Erweiterte Fensterstile.**](/windows/desktop/winmsg/extended-window-styles)

</dd> <dt>

**style**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Stil des Dialogfelds. Dieser Member kann eine Kombination aus [Fensterformatwerten](/windows/desktop/winmsg/window-styles) und [Dialogfeldformatwerten sein.](dialog-box-styles.md)

Wenn **style** den **DS \_ SETFONT-** oder **DS \_ SHELLFONT-Dialogfeldstil** enthält, enthält der **DLGTEMPLATEEX-Header** der erweiterten Dialogfeldvorlage vier zusätzliche Member ( **pointsize**, **weight**, **italic** und **typeface**), die die Schriftart beschreiben, die für den Text im Clientbereich und Steuerelemente des Dialogfelds verwendet werden soll. Wenn möglich, erstellt das System eine Schriftart gemäß den in diesen Membern angegebenen Werten. Anschließend sendet das System eine [**WM \_ SETFONT-Nachricht**](/windows/desktop/winmsg/wm-setfont) an das Dialogfeld und an jedes Steuerelement, um ein Handle für die Schriftart bereitzustellen.

Weitere Informationen finden Sie unter [Dialogfeldschriftarten](about-dialog-boxes.md).

</dd> <dt>

**cDlgItems**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl der Steuerelemente im Dialogfeld.

</dd> <dt>

**x**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die x-Koordinate in Dialogfeldeinheiten der linken oberen Ecke des Dialogfelds.

</dd> <dt>

**y**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die y-Koordinate in Dialogfeldeinheiten der oberen linken Ecke des Dialogfelds.

</dd> <dt>

**Cx**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die Breite des Dialogfelds in Dialogfeldeinheiten.

</dd> <dt>

**Cy**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die Höhe des Dialogfelds in Dialogfeldeinheiten.

</dd> <dt>

**Menü**
</dt> <dd>

Typ: **sz \_ Oder \_ Ord**

</dd> <dd>

Ein Array variabler Länge mit 16-Bit-Elementen, das eine Menüressource für das Dialogfeld identifiziert. Wenn das erste Element dieses Arrays 0x0000 ist, enthält das Dialogfeld kein Menü und das Array keine anderen Elemente. Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordnungswert einer Menüressource in einer ausführbaren Datei angibt. Wenn das erste Element einen anderen Wert hat, behandelt das System das Array als auf NULL endende Unicode-Zeichenfolge, die den Namen einer Menüressource in einer ausführbaren Datei angibt.

</dd> <dt>

**windowClass**
</dt> <dd>

Typ: **sz \_ Oder \_ Ord**

</dd> <dd>

Ein Array variabler Länge mit 16-Bit-Elementen, das die Fensterklasse des Dialogfelds identifiziert. Wenn das erste Element des Arrays 0x0000 ist, verwendet das System die vordefinierte Dialogfeldklasse für das Dialogfeld, und das Array verfügt über keine anderen Elemente. Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordnungswert einer vordefinierten Systemfensterklasse angibt. Wenn das erste Element einen anderen Wert hat, behandelt das System das Array als auf NULL endende Unicode-Zeichenfolge, die den Namen einer registrierten Fensterklasse angibt.

</dd> <dt>

**title**
</dt> <dd>

Typ: **WCHAR \[ titleLen \]**

</dd> <dd>

Der Titel des Dialogfelds. Wenn das erste Element dieses Arrays 0x0000 ist, hat das Dialogfeld keinen Titel und das Array keine anderen Elemente.

</dd> <dt>

**pointsize**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Punktgröße der Schriftart, die für den Text im Dialogfeld und die zugehörigen Steuerelemente verwendet werden soll.

Dieser Member ist nur vorhanden, wenn der **Stilmember** **DS \_ SETFONT** oder **DS \_ SHELLFONT** angibt.

</dd> <dt>

**weight**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Gewichtung der Schriftart. Beachten Sie, dass zwar jeder der werte, die für den **lfWeight-Member** der [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) aufgelistet sind, aber jeder verwendete Wert automatisch in **FW \_ NORMAL** geändert wird.

Dieser Member ist nur vorhanden, wenn der **Stilmember** **DS \_ SETFONT** oder **DS \_ SHELLFONT** angibt.

</dd> <dt>

**Kursiv**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Gibt an, ob die Schriftart italisch ist. Wenn dieser Wert **TRUE** ist, ist die Schriftart italisch.

Dieser Member ist nur vorhanden, wenn der **Stilmember** **DS \_ SETFONT** oder **DS \_ SHELLFONT** angibt.

</dd> <dt>

**Charset**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Der zu verwendende Zeichensatz. Weitere Informationen finden Sie unter dem **lfcharset-Member** von [**LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

Dieser Member ist nur vorhanden, wenn der **Stilmember** **DS \_ SETFONT** oder **DS \_ SHELLFONT** angibt.

</dd> <dt>

**Schrift**
</dt> <dd>

Typ: **WCHAR \[ stringLen \]**

</dd> <dd>

Der Name der Schriftart für die Schriftart.

Dieser Member ist nur vorhanden, wenn der **Stilmember** **DS \_ SETFONT** oder **DS \_ SHELLFONT** angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In den Funktionen [**CreateDialogIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) [**DialogBoxIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)und [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) können Sie anstelle einer Standarddialogfeldvorlage eine Vorlage für erweiterte Dialogfelder verwenden.

Dem **DLGTEMPLATEEX-Header** in einer vorlage für erweiterte Dialogfelder folgt mindestens eine [**DLGITEMTEMPLATEEX-Struktur,**](dlgitemtemplateex.md) die die Steuerelemente des Dialogfelds beschreibt. Der **cDlgItems-Member** der **DLGITEMTEMPLATEEX-Struktur** gibt die Anzahl der **DLGITEMTEMPLATEEX-Strukturen** an, die in der Vorlage folgen.

Jede [**DLGITEMTEMPLATEEX-Struktur**](dlgitemtemplateex.md) in der Vorlage muss an einer **DWORD-Grenze** ausgerichtet sein. Wenn der **Stilmember** den **DS \_ SETFONT-** oder **DS \_ SHELLFONT-Stil** angibt, beginnt die erste **DLGITEMTEMPLATEEX-Struktur** an der ersten **DWORD-Grenze** nach der **Schriftartzeichenfolge.** Wenn diese Stile nicht angegeben werden, beginnt die erste Struktur an der ersten **DWORD-Grenze** nach der **Titelzeichenfolge.**

Die **Arrays "menu",** **"windowClass",** **"title"** und **"typeface"** müssen an **WORD-Grenzen** ausgerichtet sein.

Wenn Sie Zeichenfolgen im **Menü**, **fensterKlasse,** **Titel** und **Schriftartarrays** angeben, müssen Sie Unicode-Zeichenfolgen verwenden. Verwenden Sie die [**MultiByteToWideChar-Funktion,**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) um diese Unicode-Zeichenfolgen aus ANSI-Zeichenfolgen zu generieren.

Die Elemente **x,** **y,** **cx** und **cy** geben Werte in Dialogfeldeinheiten an. Sie können diese Werte mithilfe der [**MapDialogRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) in Bildschirmeinheiten (Pixel) konvertieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

