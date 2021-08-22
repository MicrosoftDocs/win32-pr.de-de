---
title: VARIANT-Struktur
description: Die meisten Microsoft Active Accessibility Funktionen und die IAccessible-Eigenschaften und -Methoden nehmen eine VARIANT-Struktur als Parameter an. Im Wesentlichen ist die VARIANT-Struktur ein Container für eine große Union, die viele Arten von Daten enthält.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063d1e17d998f3cb7d70a0a271e55f02628e7864164e00becb5a708af371e12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563548"
---
# <a name="variant-structure"></a>VARIANT-Struktur

Die meisten Microsoft Active Accessibility-Funktionen und die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden verwenden eine [**VARIANT-Struktur**](/windows/win32/api/oaidl/ns-oaidl-variant) als Parameter. Im Wesentlichen ist die **VARIANT-Struktur** ein Container für eine große Union, die viele Arten von Daten enthält.

Der Wert im ersten Member der -Struktur, **vt,** beschreibt, welche der Union-Member gültig sind. Obwohl die [**VARIANT-Struktur**](/windows/win32/api/oaidl/ns-oaidl-variant) viele verschiedene Datentypen unterstützt, verwendet Microsoft Active Accessibility nur die folgenden Typen.



| vt-Wert     | Name des entsprechenden Wertmembers |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| VT \_ DISPATCH | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ EMPTY    | Keine                            |



 

Wenn Sie Informationen in einer [**VARIANT-Struktur**](/windows/win32/api/oaidl/ns-oaidl-variant) erhalten, überprüfen Sie den **vt-Member,** um herauszufinden, welcher Member gültige Daten enthält. Wenn Sie Informationen mithilfe einer **VARIANT-Struktur** senden, legen Sie **vt** entsprechend dem Union-Member fest, der die Informationen enthält.

Bevor Sie die -Struktur verwenden, initialisieren Sie sie, indem Sie die [**COM-Funktion (VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model) aufrufen. Wenn Sie mit der -Struktur fertig sind, löschen Sie sie, bevor der Arbeitsspeicher, der die [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) enthält, durch Aufrufen von [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)freigegeben wird.

 

 