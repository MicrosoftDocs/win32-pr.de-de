---
title: DLGITEMTEMPLATEEX-Struktur
description: Ein Textblock, der von einer erweiterten Dialogfeldvorlage verwendet wird, um das erweiterte Dialogfeld zu beschreiben. Eine Beschreibung des Formats einer erweiterten Dialogfeldvorlage finden Sie unter DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- DLGITEMTEMPLATEEX-Strukturdialogfelder
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad2bf1795f5059ec1fdda00ddb6a93cfe396dae5b4119d392eff42382fa978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785866"
---
# <a name="dlgitemtemplateex-structure"></a>DLGITEMTEMPLATEEX-Struktur

Ein Textblock, der von einer erweiterten Dialogfeldvorlage verwendet wird, um das erweiterte Dialogfeld zu beschreiben. Eine Beschreibung des Formats einer erweiterten Dialogfeldvorlage finden Sie unter [**DLGTEMPLATEEX**](dlgtemplateex.md).

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

**helpID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Hilfekontextbezeichner für das Steuerelement. Wenn das System eine [**WM \_ HELP-Nachricht**](../shell/wm-help.md) sendet, übergibt es den **helpID-Wert** im **dwContextId-Element** der [**HELPINFO-Struktur.**](/windows/win32/api/winuser/ns-winuser-helpinfo)

</dd> <dt>

**exStyle**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die erweiterten Stile für ein Fenster. Dieser Member wird nicht zum Erstellen von Steuerelementen in Dialogfeldern verwendet, aber Anwendungen, die Dialogfeldvorlagen verwenden, können damit andere Arten von Fenstern erstellen. Eine Liste der Werte finden Sie unter [**Erweiterte Fensterstile.**](/windows/desktop/winmsg/extended-window-styles)

</dd> <dt>

**style**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Das Format des Steuerelements. Bei diesem Member kann [](/windows/desktop/winmsg/window-styles) es sich um eine Kombination aus Fensterformatwerten (z. B. **WS \_ BORDER)** und mindestens einem der Steuerelementformatwerte [(z.](/windows/desktop/Controls/common-control-styles) **B. BS \_ PUSHBUTTON** und ES **\_ LEFT) sein.**

</dd> <dt>

**x**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die x-Koordinate der oberen linken Ecke des Steuerelements in Dialogfeldeinheiten. Diese Koordinate ist immer relativ zur oberen linken Ecke des Clientbereichs des Dialogfelds.

</dd> <dt>

**y**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die y-Koordinate der oberen linken Ecke des Steuerelements in Dialogfeldeinheiten. Diese Koordinate ist immer relativ zur oberen linken Ecke des Clientbereichs des Dialogfelds.

</dd> <dt>

**Cx**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die Breite des Steuerelements in Dialogfeldeinheiten.

</dd> <dt>

**Cy**
</dt> <dd>

Typ: **short**

</dd> <dd>

Die Höhe des Steuerelements in Dialogfeldeinheiten.

</dd> <dt>

**id**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Steuerelementbezeichner.

</dd> <dt>

**windowClass**
</dt> <dd>

Typ: **sz \_ Or \_ Ord**

</dd> <dd>

Ein Array variabler Länge aus 16-Bit-Elementen, das die Fensterklasse des Steuerelements angibt. Wenn das erste Element dieses Arrays ein anderer Wert als 0xFFFF ist, behandelt das System das Array als auf NULL beendete Unicode-Zeichenfolge, die den Namen einer registrierten Fensterklasse angibt.

Wenn das erste Element 0xFFFF, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer vordefinierten Systemklasse angibt. Die Ordnungszahl kann einer der folgenden Atomwerte sein.



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

Typ: **sz \_ Or \_ Ord**

</dd> <dd>

Ein Array variabler Länge aus 16-Bit-Elementen, das den anfänglichen Text oder Ressourcenbezeichner des Steuerelements enthält. Wenn das erste Element dieses Arrays 0xFFFF, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer Ressource, z. B. ein Symbol, in einer ausführbaren Datei angibt. Sie können einen Ressourcenbezeichner für Steuerelemente wie statische Symbolsteuerelemente verwenden, die anstelle von Text ein Symbol oder eine andere Ressource laden und anzeigen. Wenn das erste Element ein anderer Wert als 0xFFFF ist, behandelt das System das Array als mit NULL beendete Unicode-Zeichenfolge, die den ursprünglichen Text angibt.

</dd> <dt>

**extraCount**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl der Bytes der Erstellungsdaten, die diesem Member folgen. Wenn dieser Wert größer als 0 (null) ist, beginnen die Erstellungsdaten an der nächsten **WORD-Grenze.** Diese Erstellungsdaten können eine beliebige Größe und ein beliebiges Format haben. Die Fensterprozedur des Steuerelements muss in der Lage sein, die Daten zu interpretieren. Wenn das System das Steuerelement erstellt, übergibt es einen Zeiger auf diese Daten im *lParam-Parameter* der [**WM \_ CREATE-Nachricht,**](/windows/desktop/winmsg/wm-create) die es an das Steuerelement sendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine erweiterte Vorlage für ein Dialogfeld besteht aus einem [**DLGTEMPLATEEX-Header,**](dlgtemplateex.md) gefolgt von einer **DLGITEMTEMPLATEEX-Struktur** für jedes Steuerelement im Dialogfeld.

Jede **DLGITEMTEMPLATEEX-Struktur** muss an einer **DWORD-Grenze ausgerichtet** werden. Die **WindowClass-** und **Titelarrays** variabler Länge müssen an WORD-Grenzen **ausgerichtet** werden. Das Datenarray für die Erstellung muss an einer **WORD-Grenze ausgerichtet** werden, falls es ein Array gibt.

Wenn Sie Zeichenfolgen in den **Arrays windowClass** und **title** angeben, müssen Sie Unicode-Zeichenfolgen verwenden. Verwenden Sie die [**MultiByteToWideChar-Funktion,**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) um Unicode-Zeichenfolgen aus ANSI-Zeichenfolgen zu generieren.

Die **Elemente x,** **y,** **cx** und **cy** geben Werte in Dialogfeldeinheiten an. Sie können diese Werte mithilfe der [**MapDialogRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) in Bildschirmeinheiten (Pixel) konvertieren.

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

[**Createwindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATEEX**](dlgtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**\_WM-HILFE**](../shell/wm-help.md)
</dt> </dl>

 

