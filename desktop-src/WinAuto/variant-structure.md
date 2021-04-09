---
title: VARIANT-Struktur
description: Die meisten Funktionen von Microsoft Active Accessibility und die IAccessible-Eigenschaften und-Methoden übernehmen eine VARIANT-Struktur als Parameter. Im Wesentlichen handelt es sich bei der VARIANT-Struktur um einen Container für eine große Union, die viele Datentypen enthält.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101870"
---
# <a name="variant-structure"></a>VARIANT-Struktur

Die meisten Funktionen von Microsoft Active Accessibility und die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften und-Methoden übernehmen eine [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur als Parameter. Im Wesentlichen handelt es sich bei der **Variant** -Struktur um einen Container für eine große Union, die viele Datentypen enthält.

Der Wert im ersten Element der Struktur, **VT**, beschreibt, welche der Union-Member gültig ist. Obwohl die [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur viele verschiedene Datentypen unterstützt, werden von Microsoft Active Accessibility nur die folgenden Typen verwendet.



| VT-Wert     | Entsprechender Wertelement Name |
|--------------|---------------------------------|
| VT \_ I4       | **LVAL**                        |
| VT \_ -Verteilung | **pdispVal**                    |
| VT \_ BSTR     | **bstrauval**                     |
| VT \_ leer    | none                            |



 

Wenn Sie Informationen in einer [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur erhalten, überprüfen Sie das **VT** -Element, um herauszufinden, welches Mitglied gültige Daten enthält. Wenn Sie Informationen mithilfe einer **Variant** -Struktur senden, legen Sie auf ähnliche Weise fest, dass **VT** das Unionmember enthält, das die Informationen enthält.

Bevor Sie die-Struktur verwenden, initialisieren Sie Sie, indem Sie die [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) -Component Object Model (com)-Funktion aufrufen. Wenn die Struktur fertig ist, löschen Sie Sie, bevor der Speicher, der die [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) enthält, durch Aufrufen von [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)freigegeben wird.

 

 