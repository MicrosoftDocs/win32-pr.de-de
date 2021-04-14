---
title: Dlgitemtemplateex-Struktur
description: Ein TextBlock, der von einer erweiterten Dialogfeld Vorlage verwendet wird, um das erweiterte Dialogfeld zu beschreiben. Eine Beschreibung des Formats einer erweiterten Dialogfeld Vorlage finden Sie unter dlgtemplateex.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Dialog Felder der dlgitemtemplateex-Struktur
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392190"
---
# <a name="dlgitemtemplateex-structure"></a>Dlgitemtemplateex-Struktur

Ein TextBlock, der von einer erweiterten Dialogfeld Vorlage verwendet wird, um das erweiterte Dialogfeld zu beschreiben. Eine Beschreibung des Formats einer erweiterten Dialogfeld Vorlage finden Sie unter [**dlgtemplateex**](dlgtemplateex.md).

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a>Member

<dl> <dt>

**HelpID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Hilfe Kontext Bezeichner für das Steuerelement. Wenn das System eine [**WM- \_ Hilfe**](../shell/wm-help.md) Nachricht sendet, übergibt es **den HelpID** -Wert im **dwcontextid** -Member der [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur.

</dd> <dt>

**exStyle**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die erweiterten Stile für ein Fenster. Dieser Member wird nicht zum Erstellen von Steuerelementen in Dialogfeldern verwendet, aber Anwendungen, die Dialogfeld Vorlagen verwenden, können ihn verwenden, um andere Fenstertypen zu erstellen. Eine Liste der Werte finden Sie unter [**Erweiterte Fenster Stile**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Das Format des Steuerelements. Dieser Member kann eine Kombination aus [Fenster Stil Werten](/windows/desktop/winmsg/window-styles) (z. b. WS-Rahmen) und einem oder mehreren der Steuerelement-Format [Werten](/windows/desktop/Controls/common-control-styles) (z. b. "bin **\_ Push Button** " und " **es \_ left**") sein. **\_**

</dd> <dt>

**x**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die x-Koordinate der oberen linken Ecke des Steuer Elements in Dialogfeld Einheiten. Diese Koordinate ist immer relativ zur oberen linken Ecke des Client Bereichs des Dialog Felds.

</dd> <dt>

**y**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die y-Koordinate der oberen linken Ecke des Steuer Elements in Dialogfeld Einheiten. Diese Koordinate ist immer relativ zur oberen linken Ecke des Client Bereichs des Dialog Felds.

</dd> <dt>

**verschoben**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die Breite des Steuer Elements in Dialogfeld Einheiten.

</dd> <dt>

**CY**
</dt> <dd>

Typ: **Short**

</dd> <dd>

Die Höhe des Steuer Elements in Dialogfeld Einheiten.

</dd> <dt>

**id**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Steuerelement Bezeichner.

</dd> <dt>

**windowClass**
</dt> <dd>

Typ: **SZ \_ oder \_ Ord**

</dd> <dd>

Ein Array variabler Länge mit 16-Bit-Elementen, das die Fenster Klasse des Steuer Elements angibt. Wenn das erste Element dieses Arrays ein anderer Wert als 0xFFFF ist, behandelt das System das Array als eine mit NULL endenden Unicode-Zeichenfolge, die den Namen einer registrierten Fenster Klasse angibt.

Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer vordefinierten System Klasse angibt. Die Ordinalzahl kann einen der folgenden Atom-Werte aufweisen.



| Wert                                                                             | Bedeutung               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>0x0080</dt> </dl> | Schaltfläche<br/>     |
| <dl> <dt>0x0081</dt> </dl> | Bearbeiten<br/>       |
| <dl> <dt>0x0082</dt> </dl> | statischen<br/>     |
| <dl> <dt>0x0083</dt> </dl> | Listenfeld<br/>   |
| <dl> <dt>0x0084</dt> </dl> | Bildlaufleiste<br/> |
| <dl> <dt>0x0085</dt> </dl> | Kombinationsfeld<br/>  |



 

</dd> <dt>

**title**
</dt> <dd>

Typ: **SZ \_ oder \_ Ord**

</dd> <dd>

Ein Array variabler Länge mit 16-Bit-Elementen, das den Anfangstext oder Ressourcen Bezeichner des Steuer Elements enthält. Wenn das erste Element dieses Arrays 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer Ressource (z. b. ein Symbol) in einer ausführbaren Datei angibt. Sie können einen Ressourcen Bezeichner für Steuerelemente verwenden, z. b. statische Symbol Steuerelemente, die ein Symbol oder eine andere Ressource anstelle von Text laden und anzeigen. Wenn das erste Element ein anderer Wert als 0xFFFF ist, behandelt das System das Array als eine mit NULL endenden Unicode-Zeichenfolge, die den Anfangstext angibt.

</dd> <dt>

**extracount**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der Bytes der Erstellungs Daten, die diesem Element folgen. Wenn dieser Wert größer als 0 (null) ist, beginnt die Erstellungs Daten an der nächsten **Wort** Grenze. Diese Erstellungs Daten können eine beliebige Größe und ein beliebiges Format aufweisen. Die Fenster Prozedur des Steuer Elements muss in der Lage sein, die Daten zu interpretieren. Wenn das System das Steuerelement erstellt, übergibt es einen Zeiger auf diese Daten im *LPARAM* -Parameter der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, die an das Steuerelement gesendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine erweiterte Vorlage für ein Dialogfeld besteht aus einem [**dlgtemplateex**](dlgtemplateex.md) -Header, gefolgt von einer **dlgitemtemplateex** -Struktur für jedes Steuerelement im Dialogfeld.

Jede **dlgitemtemplateex** -Struktur muss an einer **DWORD** -Grenze ausgerichtet sein. Die **WindowClass** -und **Title** -Arrays variabler Länge müssen an **Wort** Grenzen ausgerichtet werden. Das Erstellungs Daten Array muss, falls vorhanden, an einer **Wort** Grenze ausgerichtet werden.

Wenn Sie Zeichen folgen in den **WindowClass** -und **Title** -Arrays angeben, müssen Sie Unicode-Zeichen folgen verwenden. Verwenden Sie die [**multibytetewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion zum Generieren von Unicode-Zeichen folgen aus ANSI-Zeichen folgen.

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

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**Dialogboxindirekte**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**Dialogboxderedereparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**Dlgtemplateex**](dlgtemplateex.md)
</dt> <dt>

[**Mapdialogrect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MultiByteToWideChar muss**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**WM- \_ Hilfe**](../shell/wm-help.md)
</dt> </dl>

 

