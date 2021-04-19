---
title: Dialog Ressource
description: Definiert ein Dialogfeld. | Dialog Ressource
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Dialog Feld Ressourcen Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366397"
---
# <a name="dialog-resource"></a>Dialog Ressource

Definiert ein Dialogfeld. Die-Anweisung definiert die Position und die Dimensionen des Dialog Felds auf dem Bildschirm sowie den Dialogfeld Stil.

> [!Note]  
> **Dialog** ist eine veraltete Ressourcen-ID. Neue Anwendungen sollten [**DIALOGEX**](dialogex-resource.md)verwenden.

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder ein eindeutiger ganzzahliger 16-Bit-Wert ohne Vorzeichen, der das Dialogfeld identifiziert.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*
</dt> <dd>

Optionen für das Dialogfeld. Dies kann NULL oder mehr der folgenden-Anweisungen sein.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beschriftung**](caption-statement.md) "*Text*"                    | Beschriftung des Dialog Felds, wenn es über eine Titelleiste verfügt. Weitere Informationen finden Sie unter [**Caption**](caption-statement.md).                                                                             |
| [**Merkmale**](characteristics-statement.md) *DWORD*     | Benutzerdefinierter **DWORD** -Wert, der von Ressourcen Tools verwendet werden soll. Dieser Wert wird vom System nicht verwendet. Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md).                |
| [**Class**](class-statement.md) - *Klasse*                         | Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die die Klasse des Dialog Felds angibt. Weitere Informationen finden Sie unter- [**Klasse**](class-statement.md).      |
| **ExStyle =** *Erweiterte Stile*                                   | Erweiterte Fenster Stil des Dialog Felds. Weitere Informationen finden Sie unter [**ExStyle**](exstyle-statement.md).                                                                                     |
| **Schriftart** *pointsize*, *Schriftart*                                 | Die Punktgröße und Schriftart für die Schriftart. Weitere Informationen finden Sie unter [**Schriftart**](font-statement.md).                                                                                              |
| [**Sprach**](language-statement.md) *Sprache*, *unter Sprache* | Sprache des Dialog Felds. Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).                                                                                                |
|  *MENUNAME darf* -Menü                                              | Das zu verwendende Menü. Dieser Wert ist entweder der Name des Menüs oder der ganzzahlige Bezeichner.                                                                                                        |
| [**Stil**](style-statement.md) *Stile*                        | Stile des Dialog Felds. Weitere Informationen finden Sie unter [**Style**](style-statement.md).                                                                                                        |
| [**Version**](version-statement.md) *DWORD*                     | Benutzerdefinierter **DWORD** -Wert. Diese Anweisung ist für die Verwendung durch zusätzliche Ressourcen Tools vorgesehen und wird nicht vom System verwendet. Weitere Informationen finden Sie unter [**Version**](version-statement.md). |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="remarks"></a>Bemerkungen

Die [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) -Funktion gibt die Dialog Basiseinheiten in Pixel zurück. Die genaue Bedeutung der Koordinaten hängt von dem Stil ab, der von der [**Style**](style-statement.md) Option-Anweisung definiert wird. Bei Dialogfeldern im untergeordneten Stil sind die Koordinaten relativ zum Ursprung des übergeordneten Fensters, es sei denn, im Dialogfeld ist der Stil **DS \_ absalign** enthalten. in diesem Fall sind die Koordinaten relativ zum Ursprung des Anzeige Bildschirms.

Verwenden Sie das unter **geordnete \_ WS** -Format nicht mit einem modalen Dialogfeld. Die [**Dialogbox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) -Funktion deaktiviert immer das übergeordnete Element bzw. den Besitzer des neu erstellten Dialog Felds. Wenn ein übergeordnetes Fenster deaktiviert wird, werden die untergeordneten Fenster implizit deaktiviert. Da das übergeordnete Fenster des Dialog Felds untergeordneter Stil deaktiviert ist, ist das Dialogfeld untergeordnete Formate ebenfalls.

Wenn ein Dialogfeld den Stil " **DS \_ absalign** " aufweist, sind die Dialog Koordinaten für die linke obere Ecke relativ zum Bildschirm Ursprung und nicht zur oberen linken Ecke des übergeordneten Fensters. Normalerweise verwenden Sie diesen Stil, wenn das Dialogfeld in einem bestimmten Teil der Anzeige gestartet werden soll, unabhängig davon, wo sich das übergeordnete Fenster möglicherweise auf dem Bildschirm befindet.

Das **Dialog** Feld Name kann auch als Class-Name-Parameter für die Funktion "up [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) " verwendet werden, um ein Fenster mit Dialog Feld Attributen zu erstellen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Dialog** -Anweisung veranschaulicht:

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Dialog Feldern](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[**"Kreatedialog"**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Dialogbox**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 
