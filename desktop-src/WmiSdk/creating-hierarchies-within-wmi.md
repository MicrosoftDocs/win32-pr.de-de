---
description: Der WMI-Namespace ist ein Programmier Objekt, das den Bereich für eine Gruppe von Klassen und Instanzen definiert. WMI-Anbieter Klassen müssen innerhalb eines Namespace definiert werden.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Erstellen von Hierarchien in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215460"
---
# <a name="creating-hierarchies-within-wmi"></a>Erstellen von Hierarchien in WMI

Der [*WMI-Namespace*](gloss-n.md) ist ein Programmier Objekt, das den Bereich für eine Gruppe von Klassen und Instanzen definiert. WMI-Anbieter Klassen müssen innerhalb eines Namespace definiert werden.

Namespaces beschreiben verschiedene verwaltete Umgebungen, z. b. die SMS-Umgebung. Da die Klassen und Instanzen eines Schemas die Komponenten einer verwalteten Umgebung definieren, erfordert jedes neue Schema einen neuen Namespace. Der root \\ CIMV2-Namespace enthält z. b. die Klassen und Instanzen, die im Win32-Schema definiert sind, sowie die CIM-Klassen (Parent Common Information Model), aus denen das Win32-Schema erbt. CIM-Klassen werden von der verteilten Verwaltungs Task Force ([DMTF](https://www.dmtf.org/home)) definiert.

> [!Note]  
> Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung in der [*MOF-Datei (Managed Object Format)*](gloss-m.md) .

 

WMI definiert einen Namespace als Instanz der [**\_ \_ Namespace**](--namespace.md) -System Klasse oder einer beliebigen Klasse, die vom **\_ \_ Namespace** abgeleitet ist. Die **\_ \_ Namespace** -System Klasse verfügt über eine einzelne Eigenschaft namens **Name**, die innerhalb des Gültigkeits Bereichs des übergeordneten Namespaces eindeutig sein muss. Die **Name** -Eigenschaft muss auch eine Zeichenfolge enthalten, die mit einem Buchstaben beginnt. Alle anderen Zeichen in der Zeichenfolge können Buchstaben, Ziffern oder Unterstriche sein. Bei allen Zeichen wird Groß-/Kleinschreibung nicht beachtet.

Der übergeordnete WMI-Namespace kann nicht nur den eindeutigen Namen für einen untergeordneten Namespace festlegen, sondern auch die statischen Instanzen der Klassen vor versehentlichen Änderungen durch andere Anbieter. Beispielsweise kann es sinnvoll sein, einen neuen Namespace unter einem vorhandenen Namespace für einen anderen Anbieter zu schachteln. Der ursprüngliche Anbieter kann jedoch versuchen, alle Klassen Instanzen so zu aktualisieren, dass Sie mit einem neuen Schema zu vergleichen sind. Dabei kann der ursprüngliche Anbieter alle untergeordneten untergeordneten Elemente in einem Namespace löschen. Obwohl dies eine geeignete Aktion für den Ziel Namespace sein kann, wirkt sich dies möglicherweise auf nicht verknüpfte Klassen Instanzen in einem untergeordneten Namespace aus (d. h. ihre eigenen Anbieter Klassen).

Daher empfiehlt es sich im Allgemeinen, Ihren Namespace als separat von Namespaces zu erstellen und zu registrieren, die Sie nicht direkt steuern. Dies trifft vor allem dann zu, wenn Ihre Klassen nur von allgemeinen CIM-Klassen oder anderen Klassen von Ihrem Unternehmen abgeleitet werden. Der Namespace kann sich unter dem **Stamm Namespace** befinden, z. b. wie folgt:

**Root/MyCompany/MyProduct**

Wenn die neue Klasse dagegen von der Klasse eines anderen Anbieters abgeleitet ist, müssen Sie möglicherweise die Klasse in einem untergeordneten Namespace dieses Anbieters speichern. Beachten Sie, dass dadurch die neue Klasse für das versehentliche Löschen durch den ursprünglichen Anbieter verfügbar gemacht wird.

WMI bietet verschiedene Möglichkeiten zum Erstellen eines Namespace:

-   [Erstellen eines untergeordneten Namespace mit MOF-Code](creating-a-child-namespace-with-mof-code.md)
-   [Erstellen eines gleich geordneten Namespace mit MOF-Code](creating-a-sibling-namespace-with-mof-code.md)
-   [Erstellen eines Namespace mit der WMI-API](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



