---
description: Ein WMI-Anbieter besteht aus einer MOF-Datei (Managed Object Format) und einer DLL-Datei. Die MOF-Datei definiert die Klassen, für die die Anbieterimplementierungen Daten liefern.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Entwerfen von MOF-Klassen (Managed Object Format)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 78e761b5fe0b7eeee80dc3188ba952812fb1d7f0bad963452a23e9073bb34282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374670"
---
# <a name="designing-managed-object-format-mof-classes"></a>Entwerfen von MOF-Klassen (Managed Object Format)

Ein [*WMI-Anbieter*](gloss-p.md) besteht aus einer MOF-Datei (Managed Object Format) und einer DLL-Datei. Die MOF-Datei definiert die Klassen, für die die Anbieterimplementierungen Daten liefern.

Die MOF-Klassendefinitionen werden vom [**mofcomp-Hilfsprogramm**](mofcomp.md) kompiliert und im [*WMI-Repository*](gloss-w.md)gespeichert, das auch als CIM-Repository (Common Information Model) bezeichnet wird. Eine weniger gängige Methode zum Erstellen von Klassen sind die Methoden der [COM-API für WMI.](com-api-for-wmi.md)

> [!Note]  
> Um sicherzustellen, dass alle WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wiederhergestellt werden, wenn WMI ausfällt und neu gestartet wird, verwenden Sie die Präprozessoranweisung [**\# pragma autorecover**](pragma-autorecover.md) in Ihrer MOF-Datei.

 

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Definieren der zu verwaltenden Objekte](#defining-the-objects-to-manage)
-   [Definieren von Eigenschaften oder Methoden](#defining-properties-or-methods)
-   [Miteinander in Beziehung stehende Objekte](#relating-objects-to-each-other)
-   [Zugehörige Themen](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Definieren der zu verwaltenden Objekte

Nachdem Sie den zu verwaltende Teil Ihres Unternehmens identifiziert haben, definieren Sie die zu verwaltende Objekte. Die Definition muss die erforderlichen Daten enthalten und ihnen ermöglichen, die relevanten Geschäftsregeln genau zu implementieren. Sie können Objekte auf einer präzisen Ebene definieren, aber es ist am besten, zwischen der Detailebene in der Definition und der Notwendigkeit zu entscheiden, genügend Details bereitzustellen, um nützlich zu sein. Verknüpfungen zu einem frühen Zeitpunkt des Prozesses können Zwar Zeit sparen, aber in Zukunft zu mehr Arbeit führen.

Das CIM-Tutorial auf der DMTF-Website (Distributed Management Task Force) enthält hervorragende Informationen zum Entwurfsprozess. Weitere Informationen finden Sie unter [www.dmtf.org](https://www.dmtf.org/).

Berücksichtigen Sie beim Entwickeln und Implementieren eines Schemaentwurfs die folgenden Faktoren:

-   Qualifizierer

    Qualifizierer bieten Informationen zum Beschreiben von Klassen, Objekten, Eigenschaften, Methoden und Parametern. und werden auf Klassen- und Eigenschaftendefinitionen angewendet. In MOF-Code werden Qualifizierer in eckige Klammern eingeschlossen und können \[ Schlüssel \] oder Zuordnung \[ \] enthalten. Weitere Informationen finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md) und [WMI-Qualifizierer.](wmi-qualifiers.md)

-   Namespace

    Ein Namespace ist eine logische Einheit zum Gruppieren von Klassen und Objekten sowie zum Steuern des Gültigkeitsbereichs und der Sichtbarkeit. In der Regel enthält ein Namespace eine Reihe von Klassen und Objekten, die verwaltete Objekte in einer bestimmten Umgebung darstellen. Weitere Informationen finden Sie unter [Creating Hierarchies Within WMI (Erstellen von Hierarchien innerhalb von WMI).](creating-hierarchies-within-wmi.md)

-   Object

    Ein modelliertes Objekt kann ein physisches oder logisches Element des Schemas sein. Beispielsweise können Sie ein physisches Laufwerk modellieren, z. B. ein Festplattenlaufwerk oder einen logischen Datenträger, der eine Partition auf einem physischen Datenträger sein kann. Ein Entwurf, der eine Klasse zum Modellieren eines physischen Laufwerks verwendet und diese Klasse dann erweitert, um einen logischen Datenträger zu modellieren, ist erweiterbarer als eine, die versucht, für jeden Datenträgertyp eine separate Klasse zu erstellen.

-   Daten

    Daten können dynamisch oder statisch sein. Wenn die Daten dynamisch sind, müssen Sie dafür einen Klassenanbieter erstellen.

    Damit der Benutzer Daten ändern kann, müssen Sie bestimmen, ob eine Eigenschaft nur mithilfe einer methode, die der Benutzer aufruft, direkt beschreibbar oder änderbar sein soll.

## <a name="defining-properties-or-methods"></a>Definieren von Eigenschaften oder Methoden

Im Allgemeinen ähnelt eine WMI-Klasseneigenschaft einer Eigenschaft in einer C++-Klasse. Wenn der Code nur aktionen implementiert, um den Wert abzurufen oder festzulegen, sollten die Daten als Eigenschaft der WMI-Klasse definiert werden.

Eine WMI-Methode führt im Allgemeinen eine Aktion aus, die den Zustand eines verwalteten Objekts ändert. Wenn die Aktion z. B. darin besteht, den Betrieb eines Hardwareobjekts zu aktivieren oder zu deaktivieren, ist eine Methode wahrscheinlich dem Erstellen einer Lese-/Schreibeigenschaft vorzuziehen. Sie können auch eine Eigenschaft erstellen, die den Status der Hardware anzeigt.

Wenn Sie eine Klasse oder eine Instanz erstellen, können Sie Kommentare einfügen. Verwenden Sie diese Technik, um Ihre Klasse zu dokumentieren oder Ihre Programmiertechniken zu erläutern. Weitere Informationen finden Sie unter [Erstellen eines Kommentars.](creating-a-comment.md) Darüber hinaus können Sie Daten hinzufügen, um den Zweck eines Datenobjekts zu qualifizieren. Weitere Informationen finden Sie unter [Hinzufügen eines Qualifizierers.](adding-a-qualifier.md)

## <a name="relating-objects-to-each-other"></a>Miteinander in Beziehung stehende Objekte

Es gibt zwei Möglichkeiten, Objekte miteinander in Beziehung zu setzen: durch Erstellen separater Objekte und eines Zuordnungsobjekts, das sie verknüpft, oder durch Einbetten eines Objekts in das andere Objekt. CIM unterstützt keine eingebetteten Objekte, daher müssen Sie die erste Methode verwenden, um CIM-kompatibel zu sein. WMI unterstützt jedoch eingebettete Objekte. Verwenden Sie daher beide Methoden, um eine Beziehung zwischen Objekten darzustellen. Beispiele für eingebettete Objekte finden Sie in den [Win32-Klassen.](/windows/desktop/CIMWin32Prov/win32-provider) [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) verfügt beispielsweise über das eingebettete [**Objekt Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), das ein weiteres eingebettetes Objekt, [**Win32-Vertrauensnehmer, \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)enthält.

Berücksichtigen Sie Bei der Entscheidung, wie Beziehungen zwischen Objekten dargestellt werden sollen, Folgendes:

-   Wenn eine Instanz allein nützlich ist, funktioniert eine Zuordnung am besten. Beispiel: [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) und [**Win32 \_ UserAccount.**](/windows/desktop/CIMWin32Prov/win32-useraccount) Weitere Informationen finden Sie unter [Deklarieren einer Zuordnungsklasse.](declaring-an-association-class.md)
-   Wenn eine Instanz außerhalb des übergeordneten Objekts nicht vorhanden ist, funktioniert ein eingebettetes Objekt am besten. Beispielsweise [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) und [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Weitere Informationen finden Sie unter [Einbetten von Objekten in eine Klasse.](embedded-objects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Bereitstellen von Daten für WMI](providing-data-to-wmi.md)
</dt> <dt>

[MOF-Datentypen](mof-data-types.md)
</dt> </dl>

 

 
