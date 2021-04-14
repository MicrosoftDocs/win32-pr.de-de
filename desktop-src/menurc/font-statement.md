---
title: Font-Anweisung
description: Definiert die Schriftart, mit der das System Text im Dialogfeld zeichnet. Die Schriftart muss bereits geladen worden sein. beispielsweise durch Aufrufen der LoadResource-Funktion.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Font-Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473052"
---
# <a name="font-statement"></a>Font-Anweisung

Definiert die Schriftart, mit der das System Text im Dialogfeld zeichnet. Die Schriftart muss bereits geladen worden sein. beispielsweise durch Aufrufen der [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) -Funktion.

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*
</dt> <dd>

Die Größe der Schriftart in Punkten.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*Gotik*
</dt> <dd>

Der Name der Schriftart. Dieser Parameter muss in Anführungszeichen (") eingeschlossen werden.

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*Gewicht*
</dt> <dd>

Die Gewichtung der Schriftart im Bereich von 0 bis 1000. 400 ist z. b. Normal, und 700 ist fett formatiert. Wenn dieser Wert 0 ist, wird die Standard Gewichtung verwendet. Eine Liste der vordefinierten Werte finden Sie in den in WinGDI. h definierten **FW \_ \*** -Werten.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*Kursiv*
</dt> <dd>

Gibt eine kursiv Schrift an, wenn auf true festgelegt.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*charset*
</dt> <dd>

Der Zeichensatz. Eine Liste der Werte finden Sie unter dem **lfCharSet** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Font** -Anweisung veranschaulicht:

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 