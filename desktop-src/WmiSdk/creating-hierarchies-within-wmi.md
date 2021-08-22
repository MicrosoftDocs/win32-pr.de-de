---
description: Der WMI-Namespace ist ein Programmierobjekt, das den Bereich für einen Satz von Klassen und Instanzen definiert. WMI-Anbieterklassen müssen innerhalb eines Namespace definiert werden.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Erstellen von Hierarchien in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2649fb764c1710613b27e1c9bbe518dd4cb8d02215df935ddccb59c9d7e922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568780"
---
# <a name="creating-hierarchies-within-wmi"></a>Erstellen von Hierarchien in WMI

[*Der WMI-Namespace*](gloss-n.md) ist ein Programmierobjekt, das den Bereich für einen Satz von Klassen und Instanzen definiert. WMI-Anbieterklassen müssen innerhalb eines Namespace definiert werden.

Namespaces beschreiben verschiedene verwaltete Umgebungen, z. B. die SMS-Umgebung. Da die Klassen und Instanzen eines Schemas die Komponenten einer verwalteten Umgebung definieren, erfordert jedes neue Schema einen neuen Namespace. Der Cimv2-Stammnamespace enthält z. B. die im Win32-Schema definierten Klassen und Instanzen sowie die übergeordneten Common Information Model-Klassen (CIM), von denen das \\ Win32-Schema erbt. CIM-Klassen werden von der Distributed Management Task Force ([DMTF ) definiert.](https://www.dmtf.org/home)

> [!Note]  
> Um sicherzustellen, dass alle WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wiederhergestellt werden, wenn WMI einen Fehler auftrat und neu gestartet wird, verwenden Sie die [**\# Präprozessoranweisung pragma autorecover**](pragma-autorecover.md) in Der [*Managed Object Format-Datei (MOF).*](gloss-m.md)

 

WMI definiert einen Namespace als Eine Instanz der [**\_ \_ Namespace-Systemklasse**](--namespace.md) oder eine beliebige Klasse, die von **\_ \_ Namespace ableitung.** Die **\_ \_ Namespace-Systemklasse** verfügt über eine einzelne Eigenschaft namens **Name,** die innerhalb des Bereichs des übergeordneten Namespace eindeutig sein muss. Die **Name-Eigenschaft** muss auch eine Zeichenfolge enthalten, die mit einem Buchstaben beginnt. Alle anderen Zeichen in der Zeichenfolge können Buchstaben, Ziffern oder Unterstriche sein. Bei allen Zeichen wird die Groß-/Kleinschreibung nicht beachtet.

Zusätzlich zur Bestimmung des eindeutigen Namens für einen untergeordneten Namespace kann der übergeordnete WMI-Namespace die statischen Instanzen Ihrer Klassen vor versehentlichen Änderungen durch andere Anbieter schützen. Beispielsweise kann es praktisch sein, einen neuen Namespace unter einem vorhandenen Namespace für einen anderen Anbieter zu schachteln. Der ursprüngliche Anbieter kann jedoch versuchen, alle Klasseninstanzen so zu aktualisieren, dass sie mit einem neuen Schema übereinstimmen. Dabei kann der ursprüngliche Anbieter alle untergeordneten Elemente in einem Namespace löschen. Dies kann zwar eine geeignete Aktion für den Zielnamespace sein, kann sich jedoch auf nicht verknüpfte Klasseninstanzen in einem untergeordneten Namespace (d.h. Ihre eigenen Anbieterklassen) auswirken.

Daher wird im Allgemeinen empfohlen, ihren Namespace getrennt von Namespaces zu erstellen und zu registrieren, die Sie nicht direkt steuern. Dies gilt insbesondere, wenn Ihre Klassen nur von allgemeinen CIM-Klassen oder anderen Klassen aus Ihrem Unternehmen ableiten. Ihr Namespace kann sich unter dem **Stammnamespace** befinden, z. B.:

**Root/myCompany/myProduct**

Wenn ihre neue Klasse dagegen von der Klasse eines anderen Anbieters ableitungt, müssen Sie ihre Klasse möglicherweise in einem Unternamespace dieses Anbieters speichern. Beachten Sie, dass die neue Klasse dadurch versehentlich vom ursprünglichen Anbieter gelöscht wird.

WMI bietet verschiedene Möglichkeiten zum Erstellen eines Namespace:

-   [Erstellen eines untergeordneten Namespace mit MOF-Code](creating-a-child-namespace-with-mof-code.md)
-   [Erstellen eines gleichgeordneten Namespace mit MOF-Code](creating-a-sibling-namespace-with-mof-code.md)
-   [Erstellen eines Namespace mit der WMI-API](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen Managed Object Format -Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



