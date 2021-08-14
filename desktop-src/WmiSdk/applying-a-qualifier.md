---
description: Wie viele andere Techniken in Managed Object Format (MOF) ist das Anwenden eines Qualifizierers auf Ihren Code ein relativ einfacher Prozess.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Anwenden eines Qualifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a393c7d3764338a8365ad3959803a8a3f665dbf1b9bdb0bebaaa7121ee6cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320137"
---
# <a name="applying-a-qualifier"></a>Anwenden eines Qualifizierers

Wie viele andere Techniken in Managed Object Format (MOF) ist das Anwenden eines Qualifizierers auf Ihren Code ein relativ einfacher Prozess.

Die einzigen echten Herausforderungen sind die folgenden Einschränkungen in den Namenskonventionen, die WMI erzwingt:

-   Ein Qualifizierer kann eine Klasse, Instanz, Eigenschaft, Methode oder einen Methodenparameter beschreiben.
-   Qualifizierernamen dürfen keine führenden oder nachdenkenden Unterstriche enthalten.
-   Ein Qualifizierername darf nicht mit einer Ziffer beginnen.
-   Ein Qualifizierername darf keine Sonderzeichen wie & \* @ ! ~ \\ /.
-   Bei allen Qualifizierernamen wird die Groß-/Kleinschreibung nicht beachtet.
-   Sie können die WMI-Standardqualifizierer oder qualifizierer, die in der DMTF CIM-Spezifikation beschrieben sind, nicht neu definieren.
-   Qualifizierertypen werden nicht explizit deklariert.

    Wenn Sie keinen Qualifizierertyp deklarieren, geht WMI von einem booleschen Typ mit dem Wert **TRUE aus.** Andernfalls typen WMI Qualifizierer basierend auf den von Ihnen deklarierten Qualifiziererwerten.

-   Wenn Sie Ihre eigenen Qualifizierer erstellen, sollten Sie Ihrem Schemanamen den Qualifizierernamen vorangestellt haben.

    Der Zweck dieser Regel besteht in der Vermeidung von Verwechslungen mit neuen Qualifizierern.

-   Sie können homogene Arrays von Qualifizierern erstellen.

    Das folgende Codebeispiel zeigt, wie Qualifiziererarrays mit geschweiften Klammern angegeben werden, die die Werte umschließen.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI unterstützt keine Automatisierungstypen, die nicht in der Referenz aufgeführt sind, z. B. VT \_ NULL. Weitere Informationen finden Sie unter [MOF-Datentypen.](mof-data-types.md)

Mit dem folgenden Verfahren können Sie C++ verwenden, um einer Eigenschaft einen Qualifizierer hinzuzufügen.

**So wenden Sie einen Qualifizierer mit C++ an**

-   Wenden Sie den Qualifizierer mit einem Aufruf der [**IWbemQualifierSet::P ut-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) an.

    Sie können andere Methoden von [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) verwenden, um vorhandene Qualifizierer abzurufen oder zu löschen.

Mit dem folgenden Verfahren können Sie einen Qualifizierer in MOF-Dateien anwenden.

**So beschreiben Sie ein Schlüsselwort oder einen Bezeichner mit einem Qualifizierer mit mof**

-   Platzieren Sie einen Qualifizierer in Klammern vor dem Schlüsselwort oder Bezeichner, das bzw. der vom Qualifizierer beschrieben wird.

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

 

 



