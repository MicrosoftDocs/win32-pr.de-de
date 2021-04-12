---
title: Direct2D-Fehler Behandlungsrichtlinien
description: In diesem Thema werden die Direct2D-Fehler Behandlungsrichtlinien beschrieben. Der Abschnitt ist wie folgt gegliedert.
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949025"
---
# <a name="direct2d-error-handling-policies"></a>Direct2D-Fehler Behandlungsrichtlinien

In diesem Thema werden die Direct2D-Fehler Behandlungsrichtlinien beschrieben. Der Abschnitt ist wie folgt gegliedert.

-   [Verwendung von HRESULT](#use-of-hresult)
-   [Rückgabewert von Batch Funktionen](#return-value-of-batched-functions)
-   [Ungültige Eingabe](#invalid-input)
    -   [Ausgabe Zeiger](#output-pointer)
    -   [Erforderlicher Parameter](#required-parameter)
-   ["NaN" und "schlecht geordnete Eingabe"](#nan-and-poorly-ordered-input-rects)
    -   [Nan als Eingabe](#nan-as-input)
    -   [Nicht ordnungs eine schlechte geordnete Eingabe](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Verwendung von HRESULT

Wenn eine Funktion nicht in einem Batch verarbeitet wird und einen Laufzeitfehler verursachen kann, sollte **HRESULT** zurückgegeben werden, um einen Fehler anzugeben. Bei einem Laufzeitfehler handelt es sich um einen Fehler, der zur Entwurfszeit nicht vermieden werden kann, z. b. nicht genügend Arbeitsspeicher.

## <a name="return-value-of-batched-functions"></a>Rückgabewert von Batch Funktionen

Batch Funktionen in Direct2D sind die Funktionen, die als einzelne Einheit verarbeitet werden, wenn [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) aufgerufen wird. Dabei handelt es sich um die Zeichnungs Befehle zwischen [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und **EndDraw** oder Befehlen in [**geometrysink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Für diese Funktionen werden Fehler zu dem Zeitpunkt gemeldet, zu dem der Batch abgeschlossen ist. Der Fehler wird nach " **EndDraw** " für Zeichnungs Befehle und nach " **Close** " für " **geometrysink**" zurückgegeben.

Rendertargets stoppt das Zeichnen, wenn ein Fehlerzustand festgelegt ist. eine Anwendung kann jedoch eine leeren [**aufzurufen,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) um den Fehlerzustand zurückzusetzen und das Zeichnen fortzusetzen.

**Get** -und **set** -Funktionen haben keinen Rückgabewert. Wenn eine **Set** -Funktion jedoch über eine ungültige Eingabe verfügt, generiert die debugschicht eine Meldung. In diesem Fall wird kein Fehlerzustand festgelegt, und die **Set** -Funktion führt keine Aktion aus.

## <a name="invalid-input"></a>Ungültige Eingabe

Direct2D dereferenziert Ausgabe Zeiger und erforderliche Parameter, die zu Zugriffs Verstößen führen, wenn die Zeiger ungültig sind oder **null** sind.

### <a name="output-pointer"></a>Ausgabe Zeiger

Direct2D dereferenziert einen Ausgabe Zeiger und weist ihn sofort nach der Eingabe der Funktion **null** zu. Dies führt zu einer Zugriffsverletzung, wenn ein Aufrufer **null** als Zeiger auf den Rückgabewert übergibt. Diese Richtlinie gilt auch für Arrays von Zeigern. Bei anderen Ausgabeparametern, z. b. einer Struktur, erfolgt die Dereferenzierung später und führt ebenfalls zu einer Zugriffsverletzung. Es gibt jedoch einige Methoden mit optionalen Ausgabe Zeigern (d. h. [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)), die keine Zugriffsverletzung verursachen.

### <a name="required-parameter"></a>Erforderlicher Parameter

Wenn **null** an eine Funktion übermittelt wird, die einen gültigen Wert erfordert, dereferenziert die Funktion den ungültigen Zeiger frühzeitig und führt zu einer Zugriffsverletzung. Bei optionalen Eingabe Parametern ist **null** ein gültiger Wert, der einen angemessenen Standardwert ergibt.

## <a name="nan-and-poorly-ordered-input-rects"></a>"NaN" und "schlecht geordnete Eingabe"

In Direct2D wird NaN als gültige Eingabe betrachtet, und eine nicht ordnungsgemäß geordnete Eingabe wird sortiert.

### <a name="nan-as-input"></a>Nan als Eingabe

NaN wird als gültige Eingabe betrachtet, obwohl es in der Regel zu der primitiven führt, die das Nan-Zeichen nicht zeichnet. Die Direct2D-API bietet keine explizite Filterung von Nan zum Validieren von Eingaben.

### <a name="poorly-ordered-input-rects"></a>Nicht ordnungs eine schlechte geordnete Eingabe

Nicht ordnungsgemäß sortierte Eingabe-rects werden so sortiert, dass die oberen, linken und unteren, rechten Ecken richtig angegeben werden. Bei der Ausgabe sehen leere Rechtecke wie folgt aus: {unendlich, unendlich, Floatmax, Floatmax}.

 

 