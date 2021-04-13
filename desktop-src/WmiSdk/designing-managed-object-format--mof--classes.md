---
description: Ein WMI-Anbieter besteht aus einer Managed Object Format Datei (MOF) und einer DLL-Datei. Die MOF-Datei definiert die Klassen, für die die Anbieter Implementierung Daten bereitstellt.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Entwerfen von Managed Object Format-Klassen (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216901"
---
# <a name="designing-managed-object-format-mof-classes"></a>Entwerfen von Managed Object Format-Klassen (MOF)

Ein [*WMI-Anbieter*](gloss-p.md) besteht aus einer Managed Object Format Datei (MOF) und einer DLL-Datei. Die MOF-Datei definiert die Klassen, für die die Anbieter Implementierung Daten bereitstellt.

Die MOF-Klassendefinitionen werden vom Hilfsprogramm [**Mofcomp**](mofcomp.md) kompiliert und im [*WMI-Repository*](gloss-w.md)gespeichert, das auch als Common Information Model (CIM)-Repository bezeichnet wird. Eine weniger gängige Methode zum Erstellen von Klassen ist die Methode der [com-API für WMI](com-api-for-wmi.md).

> [!Note]  
> Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung in der MOF-Datei.

 

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Definieren der zu verwaltenden Objekte](#defining-the-objects-to-manage)
-   [Definieren von Eigenschaften oder Methoden](#defining-properties-or-methods)
-   [Beziehung zwischen Objekten](#relating-objects-to-each-other)
-   [Zugehörige Themen](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Definieren der zu verwaltenden Objekte

Nachdem Sie den Teil Ihres Unternehmens für die Verwaltung identifiziert haben, definieren Sie die zu verwaltenden Objekte. Die Definition muss die erforderlichen Daten enthalten und die genaue Implementierung der relevanten Geschäftsregeln ermöglichen. Sie können Objekte auf granularer Ebene definieren, aber es empfiehlt sich, zwischen der Detailebene zu entscheiden, die in der Definition enthalten ist, und die Notwendigkeit, genügend Details bereitzustellen, um nützlich zu sein. Verknüpfungen können frühzeitig im Prozesszeit sparen, können jedoch in Zukunft zu weiteren Aufgaben führen.

Das CIM-Tutorial auf der DMTF-Website (verteilte Verwaltungs Task Force) enthält hervorragende Informationen zum Entwurfsprozess. Weitere Informationen finden Sie unter [www.DMTF.org](https://www.dmtf.org/).

Berücksichtigen Sie die folgenden Faktoren, wenn Sie einen Schema Entwurf entwickeln und implementieren:

-   Qualifizierer

    Qualifizierer stellen Informationen zum Beschreiben von Klassen, Objekten, Eigenschaften, Methoden und Parametern bereit. und werden auf Klassen-und Eigenschafts Definitionen angewendet. In MOF-Code werden Qualifizierer in eckige Klammern eingeschlossen und können einen Schlüssel oder eine Zuordnung enthalten \[ \] \[ \] . Weitere Informationen finden Sie unter [Hinzufügen von Qualifizierern](adding-a-qualifier.md) und [WMI-Qualifizierern](wmi-qualifiers.md).

-   Namespace

    Ein Namespace ist eine logische Einheit zum Gruppieren von Klassen und Objekten sowie zum Steuern des Gültigkeits Bereichs und der Sichtbarkeit. In der Regel enthält ein Namespace einen Satz von Klassen und Objekten, die verwaltete Objekte in einer bestimmten Umgebung darstellen. Weitere Informationen finden Sie unter [Erstellen von Hierarchien in WMI](creating-hierarchies-within-wmi.md).

-   Object

    Ein modelliertes Objekt kann ein physisches oder logisches Element des Schemas sein. Beispielsweise können Sie ein physisches Laufwerk (z. b. ein Festplattenlaufwerk) oder einen logischen Datenträger modellieren, der eine Partition auf einem physischen Datenträger sein kann. Ein Entwurf, der eine Klasse zum Modellieren eines physischen Laufwerks verwendet und dann diese Klasse erweitert, um einen logischen Datenträger zu modellieren, ist erweiterbar als eine Klasse, die versucht, eine separate Klasse für jeden Typ von Datenträger zu erstellen.

-   Daten

    Die Daten können dynamisch oder statisch sein. Wenn die Daten dynamisch sind, müssen Sie einen Klassen Anbieter dafür erstellen.

    Um dem Benutzer das Ändern von Daten zu ermöglichen, müssen Sie bestimmen, ob eine Eigenschaft nur mit einer vom Benutzer aufgerufenen Methode direkt geschrieben oder geändert werden soll.

## <a name="defining-properties-or-methods"></a>Definieren von Eigenschaften oder Methoden

Im Allgemeinen ähnelt eine WMI-Klassen Eigenschaft einer Eigenschaft in einer C++-Klasse. Wenn die einzige Aktion, die der Code für das Datenelement implementiert, den Wert erhält oder den Wert festgelegt wird, sollten die Daten als Eigenschaft der WMI-Klasse definiert werden.

Eine WMI-Methode führt im Allgemeinen eine Aktion aus, die den Status eines verwalteten Objekts ändert. Wenn beispielsweise die Aktion zum Aktivieren oder Deaktivieren des Vorgangs eines Hardware Objekts dient, ist es wahrscheinlich besser, eine Eigenschaft mit Lese-/Schreibzugriff zu erstellen. Sie können auch eine Eigenschaft erstellen, die den Status der Hardware anzeigt.

Wenn Sie eine Klasse oder eine Instanz erstellen, können Sie Kommentare einschließen. Verwenden Sie dieses Verfahren, um Ihre Klasse zu dokumentieren oder Ihre Programmiertechniken zu erläutern. Weitere Informationen finden Sie unter [Erstellen eines Kommentars](creating-a-comment.md). Außerdem können Sie Daten hinzufügen, um den Zweck eines Datenobjekts zu qualifizieren. Weitere Informationen finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).

## <a name="relating-objects-to-each-other"></a>Beziehung zwischen Objekten

Es gibt zwei Möglichkeiten, Objekte miteinander zu verknüpfen: durch Erstellen separater Objekte und eines Zuordnungs Objekts, das Sie miteinander verknüpft, oder durch Einbetten eines Objekts in das andere. CIM bietet keine Unterstützung für eingebettete Objekte. Daher müssen Sie die erste Methode verwenden, um CIM-kompatibel zu sein. WMI unterstützt jedoch eingebettete Objekte. verwenden Sie daher beide Methoden, um eine Beziehung zwischen Objekten darzustellen. Beispiele für eingebettete Objekte finden Sie in den [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider). Beispielsweise verfügt [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) über den eingebetteten Objekt- [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), der über ein anderes eingebettetes Objekt, [**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)verfügt.

Berücksichtigen Sie bei der Entscheidung, wie Beziehungen zwischen Objekten dargestellt werden sollen, Folgendes:

-   Wenn eine-Instanz selbst nützlich ist, funktioniert eine Zuordnung am besten. Beispielsweise [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) und [**Win32- \_ Benutzerkonto**](/windows/desktop/CIMWin32Prov/win32-useraccount). Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).
-   Wenn eine Instanz nicht außerhalb des übergeordneten Objekts vorhanden ist, funktioniert ein eingebettetes Objekt am besten. Beispielsweise [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) und [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Weitere Informationen finden Sie unter [Einbetten von Objekten in einer Klasse](embedded-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Bereitstellen von Daten für WMI](providing-data-to-wmi.md)
</dt> <dt>

[MOF-Datentypen](mof-data-types.md)
</dt> </dl>

 

 
