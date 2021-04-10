---
title: Verwalten von Eigenschaften
description: Jede Eigenschaft besteht aus einem Eigenschafts Bezeichner (innerhalb des Eigenschaften Satzes eindeutig), einem Variant-Typ (VT oder VarType), der den Typ eines Werts darstellt, und dem Wert selbst.
ms.assetid: d220ecb4-b014-4ac9-a636-9a493187cc87
keywords:
- Strukturierter Speicher, Verwendung, Verwalten von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10dd78a1f8a8484090728dba6fe149840e940461
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858318"
---
# <a name="managing-properties"></a>Verwalten von Eigenschaften

Jede Eigenschaft besteht aus einem *Eigenschafts Bezeichner* (innerhalb des Eigenschaften Satzes eindeutig), einem *Variant-Typ (VT oder VarType)* , der den Typ eines Werts darstellt, und dem *Wert* selbst. Das Variant Type-Tag beschreibt die Darstellung der Daten im-Wert. Außerdem kann einer Eigenschaft ein *Zeichen folgen Name* zugewiesen werden, der zum Identifizieren der Eigenschaft verwendet werden kann, anstatt den erforderlichen numerischen Eigenschaften Bezeichner (ID) zu verwenden. Zum Erstellen und Verwalten von Eigenschaften definiert com die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle.

Die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle enthält Methoden zum Lesen und Schreiben von Arrays von Eigenschaften-oder Eigenschaftsnamen. Die-Schnittstelle enthält [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) -und [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) -Methoden, die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Methoden gleichen Namens ähneln. Es gibt Hilfsmethoden, mit denen Sie den Klassen Bezeichner (CLSID) des Eigenschaften Satzes festlegen, die dem Satz zugeordneten Zeiten festlegen und Statistiken zum Eigenschaften Satz erhalten. Schließlich erstellt die [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) -Methode einen Enumerator und gibt einen Zeiger auf die zugehörige [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) -Schnittstelle zurück. Sie können die Methoden dieser Schnittstelle aufrufen, um die [**Status propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) -Strukturen für Ihr Objekt aufzulisten, das Informationen zu allen Eigenschaften im aktuellen Eigenschaften Satz bereitstellt.

Im folgenden finden Sie ein Beispiel für die Darstellung von Eigenschaften. Wenn eine bestimmte Eigenschaft in einem Eigenschaften Satz den wissenschaftlichen Namen eines Tieres enthält, könnte dieser Name als NULL-terminierte Zeichenfolge gespeichert werden. Zusammen mit dem Namen wird ein Typindikator gespeichert, um anzugeben, dass der Wert eine NULL-terminierte Zeichenfolge ist. Diese Eigenschaften können folgende Merkmale aufweisen:



| Eigenschafts-ID | Zeichen folgen Bezeichner | Typindikator | Dargestellter Wert              |
|-------------|-------------------|----------------|--------------------------------|
| 02          | PID \_ animalname   | VT \_ LPWSTR     | NULL terminierte Unicode-Zeichenfolge |
| 03          | PID- \_ legcount     | VT \_ I2         | WORD                           |



 

Jede Anwendung, die das Eigenschafts Satz Format erkennt – identifiziert Sie mithilfe ihrer Format-ID (fmtid) – kann die-Eigenschaft mit dem Bezeichner "PID \_ animalname" untersuchen, feststellen, dass es sich um eine NULL terminierte Zeichenfolge handelt, und den Wert lesen und schreiben. Obwohl die Anwendung [**IPropertyStorage:: Read Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) aufrufen kann, um einen oder alle Eigenschaften Sätze zu lesen (nachdem zunächst ein Zeiger abgerufen wurde), muss die Anwendung wissen, wie der Eigenschaften Satz interpretiert werden kann.

Ein Eigenschafts Wert wird durch Eigenschaften Schnittstellen als Instanz des [**typpropvariant**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)-Objekts übermittelt.

Es ist wichtig, zwischen diesen gespeicherten (permanenten) Eigenschaften und Lauf Zeiteigenschaften zu unterscheiden. Variant-Type-Wert Konstanten haben Namen, die mit VT beginnen \_ . Der Satz gültiger PROPVARIANT ist jedoch nicht vollständig gleichwertig mit dem Satz von Varianten, die in Automation-und ActiveX-Steuerelementen verwendet werden.

Der einzige Unterschied zwischen den beiden-Strukturen ist der zulässige Satz von VT \_ -Tags (Variant Type/VarType) in jedem. Wenn ein bestimmter Eigenschaftentyp sowohl in einem Variant-als auch in einem PROPVARIANT-Typ verwendet werden kann, weist das Type-Tag (der VT- \_ Wert) immer einen identischen Wert auf. Außerdem ist für einen bestimmten VT \_ -Wert die in-Memory-Darstellung, die in Varianten und propvarianten verwendet wird, identisch. Diese Vorgehensweise ermöglicht es dem Typsystem, unzulässige typtags abzufangen, während gleichzeitig einem erfahrenen Client ermöglicht wird, ggf. eine Zeiger Umwandlung zu implementieren.

Weitere Informationen finden Sie im folgenden Abschnitt [Überlegungen zum Eigenschaften Speicher](property-storage-considerations.md).

 

 