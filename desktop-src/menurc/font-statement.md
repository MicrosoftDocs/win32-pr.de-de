---
title: FONT-Anweisung
description: Definiert die Schriftart, mit der das System Text im Dialogfeld zeichnet. Die Schriftart muss zuvor geladen worden sein. beispielsweise durch Aufrufen der LoadResource-Funktion.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- FONT-Anweisung Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad289923503866ba2bcd9338bb59a556d0e37cd0a839d4eede0f95a0bec5fd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972069"
---
# <a name="font-statement"></a>FONT-Anweisung

Definiert die Schriftart, mit der das System Text im Dialogfeld zeichnet. Die Schriftart muss zuvor geladen worden sein. beispielsweise durch Aufrufen der [**LoadResource-Funktion.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*
</dt> <dd>

Die Schriftgröße in Punkten.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*Schrift*
</dt> <dd>

Der Name der Schriftart. Dieser Parameter muss in Anführungszeichen (") eingeschlossen werden.

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*Gewicht*
</dt> <dd>

Die Gewichtung der Schriftart im Bereich von 0 bis 1000. Beispielsweise ist 400 normal und 700 fett. Wenn dieser Wert 0 ist, wird die Standardgewichtung verwendet. Eine Liste der vordefinierten Werte finden Sie in den **FW-Werten, \_ \*** die in WinGDI.h definiert sind.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*Italic*
</dt> <dd>

Gibt eine italische Schriftart an, wenn diese auf TRUE festgelegt ist.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*Charset*
</dt> <dd>

Der Zeichensatz. Eine Liste der Werte finden Sie unter dem **lfCharSet-Element** der [**LOGFONT-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **FONT-Anweisung** veranschaulicht:

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 