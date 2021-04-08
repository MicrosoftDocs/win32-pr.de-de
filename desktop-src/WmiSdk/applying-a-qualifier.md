---
description: Wie viele andere Techniken in Managed Object Format (MOF) ist das Anwenden eines Qualifizierers auf Ihren Code ein relativ einfacher Vorgang.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Anwenden eines Qualifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760777"
---
# <a name="applying-a-qualifier"></a>Anwenden eines Qualifizierers

Wie viele andere Techniken in Managed Object Format (MOF) ist das Anwenden eines Qualifizierers auf Ihren Code ein relativ einfacher Vorgang.

Die einzigen wirklichen Herausforderungen sind die folgenden Einschränkungen bei den Benennungs Konventionen, die von WMI erzwungen werden:

-   Ein Qualifizierer kann eine Klasse, eine Instanz, eine Eigenschaft, eine Methode oder einen Methoden Parameter beschreiben.
-   Qualifizierernamen dürfen weder führende noch nachfolgende Unterstriche enthalten.
-   Ein qualifizierername darf nicht mit einer Ziffer beginnen.
-   Ein qualifizierername darf keine Sonderzeichen enthalten, z \* . b. & @! ~ \\ /.
-   Bei allen Qualifizierernamen wird Groß-/Kleinschreibung
-   Sie können die standardmäßigen WMI-Qualifizierer oder-Qualifizierer, die in der DMTF CIM-Spezifikation beschrieben werden
-   Qualifizierertypen werden nicht explizit deklariert.

    Wenn Sie keinen Qualifizierertyp deklarieren, geht WMI davon aus, dass der Typ boolescher Wert mit dem Wert **true** ist. Andernfalls sind WMI-Typen Qualifizierer basierend auf den deklarierten Qualifiziererwerten.

-   Wenn Sie Ihre eigenen Qualifizierer erstellen, sollten Sie Ihren Schema Namen dem Qualifizierernamen voranstellen.

    Der Zweck dieser Regel ist die Vermeidung von Verwechslungen mit neuen Qualifizierern.

-   Sie können homogene Arrays von Qualifizierern erstellen.

    Im folgenden Codebeispiel wird gezeigt, wie qualifiziererarrays mit geschweiften Klammern angegeben werden, die die Werte umschließen.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI unterstützt keine Automatisierungs Typen, die nicht in der Referenz aufgeführt sind, wie z \_ . b. VT NULL. Weitere Informationen finden Sie unter [MOF-Datentypen](mof-data-types.md).

Das folgende Verfahren hilft Ihnen bei der Verwendung von C++, um einer Eigenschaft einen Qualifizierer hinzuzufügen.

**So wenden Sie einen Qualifizierer mit C++ an**

-   Wenden Sie den Qualifizierer mit einem-Befehl an die [**iwbemqualifierset::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) -Methode an.

    Sie können andere Methoden von [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) verwenden, um vorhandene Qualifizierer abzurufen oder zu löschen.

Mithilfe des folgenden Verfahrens können Sie einen Qualifizierer in MOF-Dateien anwenden.

**So beschreiben Sie ein Schlüsselwort oder einen Bezeichner mit einem Qualifizierer mit MOF**

-   Platzieren Sie einen Qualifizierer in Klammern, bevor Sie das Schlüsselwort oder den Bezeichner beschreiben

    Das folgende Codebeispiel zeigt, wie Qualifizierer verwendet werden.

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    Im folgenden Beispiel wird die richtige Platzierung von Qualifizierern beschrieben.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



