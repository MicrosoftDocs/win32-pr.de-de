---
description: Eigenschaften in WMI-Klassen beschreiben Daten über ein verwaltetes Objekt.
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: Hinzufügen einer WMI-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bba8944da155ca250edfed0c6e9160f555ba9551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352522"
---
# <a name="adding-a-wmi-property"></a>Hinzufügen einer WMI-Eigenschaft

Eigenschaften in WMI-Klassen beschreiben Daten über ein verwaltetes Objekt. **Handle**, **ProcessID** und **PageFaults** werden z. b. als Eigenschaften der Win32- [**\_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse definiert und beschreiben Aspekte eines Betriebssystem Prozesses. Weitere Informationen finden Sie unter [Schreiben eines Eigenschaften Anbieters](writing-a-property-provider.md).

## <a name="defining-a-property-in-mof"></a>Definieren einer Eigenschaft in MOF

Eine WMI-Eigenschaft stellt einen Aspekt oder einen Zustand im-Objekt dar. Anstatt Methoden zu erstellen, die einfach einen Wert erhalten und festgelegt haben, können Sie eine Eigenschaft erstellen. Beispielsweise wird mit der Eigenschaft " **nettenabled** " von [**Win32 \_ Network Adapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) angezeigt, ob der Status des Adapters aktiviert oder deaktiviert ist. Die Aktivierungs [**-und**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) [**Deaktivierungs**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) Methoden führen jedoch tatsächlich die Aktion aus, den Adapter Zustand zu ändern.

Eine Eigenschaft muss einen Datentyp aufweisen. Der Datentyp des [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Eigenschaften **Handles** ist **String** , und der Datentyp von **PageFaults** ist **UInt32**. Wenn eine Eigenschaft nur zwei Zustände aufweisen kann, wird der Datentyp der Eigenschaft normalerweise auf einen **booleschen** Wert festgelegt.

Die-Eigenschaft kann auch ein Array sein. Die Sicherheits-ID (**sid**)-Eigenschaft des Win32-Vertrauens nehmers ist beispielsweise ein Bytearray (**Uint8**), das die sid enthält. [**\_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) Eigenschaften können eingebettete Objekte enthalten, die Verweise auf eine oder mehrere Instanzen einer anderen WMI-Klasse sind. Die Eigenschaften von "freigegebene Zugriffs Steuerungs Liste **(DACL)** " und "System Access Control List" **(SACL)** von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)sind z. b. Arrays von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Objekten, die die Gruppen und Konten beschreiben, die Zugriff haben. Die **Group** -Eigenschaft in **Win32 \_ securityDescriptor** enthält einen Verweis auf eine einzelne Instanz des **Win32- \_ Treuhänders**. Weitere Informationen finden Sie unter [Einbetten von Objekten in einer Klasse](embedded-objects.md).

Eine Eigenschaft kann über mehrere [*Qualifizierer*](gloss-q.md)verfügen. Diese [Qualifizierer](wmi-qualifiers.md) können [*Common Information Model (CIM)*](gloss-c.md) oder WMI-Qualifizierern sein oder für bestimmte Typen von klassenspezifisch sein, z. b. die Qualifizierer der [Leistungs](qualifiers-specific-to-wmi-performance-classes.md) Bezeichner-Klasse. Qualifizierer geben einen Aspekt der Eigenschaft an, z. b. Wenn Sie schreibgeschützt ist oder ohne ein bestimmtes Privileg geändert werden kann. Eine Anwendung, die versucht, in die [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)**DACL** -Eigenschaft zu schreiben, benötigt z. b. die Berechtigungen " **SeSecurityPrivilege** " und " **SeRestorePrivilege**". Weitere Informationen finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).

Zum Schluss muss eine Eigenschaft einen Namen haben. Sie können eine Eigenschaft in den Grenzen der Standard Programmierungs Praxis benennen. Es gibt jedoch zwei Haupt Ausnahmen. Erstens können Sie kein MOF-Schlüsselwort, z. b. "Class", als Eigenschaftsnamen verwenden. Zweitens können Sie auch keine WQL-Schlüsselwörter, wie z. b. "Group", als Eigenschaftsnamen verwenden. Weitere Informationen zu MOF-und WQL-Schlüsselwörtern finden Sie unter [MOF-Datentypen](mof-data-types.md) und [WQL (SQL für WMI)](wql-sql-for-wmi.md).

Sowohl für C++-als auch für Managed Object Format (MOF)-Code deklarieren Sie die Eigenschaften einer Klasse zur gleichen Zeit, in der Sie die Klasse deklarieren.

**So definieren Sie eine Eigenschaft**

-   Schließen Sie den Eigenschafts Datentyp, den Namen und einen optionalen Standardwert und den Qualifizierer zwischen den geschweiften Klammern der Klassen Beschreibung ein.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    Die Klasse MyClass im vorangehenden Beispiel hat drei Eigenschaften: eine Zeichenfolge, eine 32-Bit-Ganzzahl mit Vorzeichen und eine 32-Bit-Ganzzahl ohne Vorzeichen. Jeder Eigenschaft wird der Name der Groß-/Kleinschreibung und der MOF-Datentyp zugewiesen.

    Der [**Schlüssel**](key-qualifier.md) Qualifizierer definiert die Zeichen folgen Eigenschaft als Schlüsseleigenschaft, die eine Instanz der Klasse eindeutig identifiziert. Weitere Informationen zu Qualifizierern finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Klasse](creating-a-class.md)
</dt> </dl>

 

 
