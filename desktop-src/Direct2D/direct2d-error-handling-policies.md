---
title: Richtlinien für die Direct2D-Fehlerbehandlung
description: In diesem Thema werden die Direct2D-Fehlerbehandlungsrichtlinien beschrieben. Der Abschnitt ist wie folgt gegliedert.
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3be48c5d80cbbd971f63392efaf6b902ff6187e0a2687df25ccc728efafbfab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318030"
---
# <a name="direct2d-error-handling-policies"></a>Richtlinien für die Direct2D-Fehlerbehandlung

In diesem Thema werden die Direct2D-Fehlerbehandlungsrichtlinien beschrieben. Der Abschnitt ist wie folgt gegliedert.

-   [Verwendung von HRESULT](#use-of-hresult)
-   [Rückgabewert von Batchfunktionen](#return-value-of-batched-functions)
-   [Ungültige Eingabe](#invalid-input)
    -   [Ausgabezeiger](#output-pointer)
    -   [Erforderlicher Parameter](#required-parameter)
-   [NaN- und Schlecht geordnete Eingabe-RECTs](#nan-and-poorly-ordered-input-rects)
    -   [NaN als Eingabe](#nan-as-input)
    -   [Schlecht geordnete Eingabe-RECTs](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Verwendung von HRESULT

Wenn eine Funktion nicht batchweise ausgeführt wird und einen Laufzeitfehler haben kann, sollte **sie HRESULT** zurückgeben, um einen Fehler anzugeben. Ein Laufzeitfehler ist jeder Fehler, der zur Entwurfszeit nicht vermieden werden kann, z. B. nicht genügend Arbeitsspeicher.

## <a name="return-value-of-batched-functions"></a>Rückgabewert von Batchfunktionen

Batchfunktionen in Direct2D sind die Funktionen, die als einzelne Einheit verarbeitet werden, wenn [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) aufgerufen wird. Dies sind die Zeichnungsbefehle zwischen [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und **EndDraw oder** Befehle in [**GeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) Für diese Funktionen werden Fehler beim Abschluss des Batches gemeldet. Der Fehler wird nach **EndDraw für** Zeichnungsbefehle und nach **Close** für **GeometrySink zurückgegeben.**

RenderTargets beenden das Zeichnen, wenn ein Fehlerzustand festgelegt ist, aber eine Anwendung kann [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) aufrufen, um den Fehlerzustand zurückzusetzen und das Zeichnen wieder aufzunehmen.

**Die Funktionen Get** **und Set** haben keinen Rückgabewert. Wenn eine **Set-Funktion** jedoch über eine ungültige Eingabe verfügt, generiert die Debugebene eine Meldung. In diesem Fall wird kein Fehlerzustand festgelegt, und die **Set-Funktion** führt nichts aus.

## <a name="invalid-input"></a>Ungültige Eingabe

Direct2D dereferenziert Ausgabezeder und erforderliche Parameter, die zu Zugriffsverletzungen führen, wenn die Zeiger ungültig oder **NULL sind.**

### <a name="output-pointer"></a>Ausgabezeiger

Direct2D dereferenziert einen Ausgabezeiger und  weist ihn sofort nach dem Eingeben der Funktion NULL zu. Dies verursacht eine Zugriffsverletzung, wenn ein Aufrufer **NULL** als Zeiger auf den Rückgabewert übergibt. Diese Richtlinie gilt auch für Arrays von Zeigern. Bei anderen Ausgabeparametern, z. B. einer Struktur, erfolgt die Dereferenzierung später und führt auch zu einer Zugriffsverletzung. Es gibt jedoch einige Methoden mit optionalen Ausgabezedern (d. h. [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush),**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)die keine Zugriffsverletzung verursachen.

### <a name="required-parameter"></a>Erforderlicher Parameter

Wenn **NULL** an eine Funktion übergeben wird, die einen gültigen Wert erfordert, dereferenziert die Funktion den ungültigen Zeiger frühzeitig, was zu einer Zugriffsverletzung führt. Bei optionalen **Eingabeparametern ist NULL** ein gültiger Wert, der zu einem angemessenen Standardwert führt.

## <a name="nan-and-poorly-ordered-input-rects"></a>NaN- und Schlecht geordnete Eingabe-RECTs

In Direct2D gilt NaN als gültige Eingabe, und schlecht sortierte Eingabe-RECTs werden sortiert.

### <a name="nan-as-input"></a>NaN als Eingabe

NaN wird als gültige Eingabe betrachtet, führt jedoch in der Regel dazu, dass das Primitive, das das NaN enthält, nicht gezeichnen wird. Die Direct2D-API bietet keine explizite Filterung von NaN zum Überprüfen der Eingabe.

### <a name="poorly-ordered-input-rects"></a>Schlecht geordnete Eingabe-RECTs

Schlecht sortierte Eingabe-RECTs werden so sortiert, dass die oberen, linken und unteren, rechten Ecken richtig angegeben werden. Für die Ausgabe sehen leere Rechtecke wie dies aus: {Infinity, Infinity, FloatMax, FloatMax}.

 

 