---
description: Anzeigen von Topologieinformationen
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Anzeigen von Topologieinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347087"
---
# <a name="viewing-topology-information"></a>Anzeigen von Topologieinformationen

In topoedit verfügt jedes topologieelement, z. b. Knoten, Knoten Eingaben und Knoten Ausgaben, über einen zugeordneten Attribut Speicher, der das Verhalten des Knotens verwaltet. Um die Attribute anzuzeigen, wählen Sie das Element aus, und im Bereich **Attribute** werden die Informationen angezeigt. Für Topologien, die aus einer XML-Datei geladen werden, zeigen einige der Knoten möglicherweise nicht den gesamten Attribut Speicher an. Um den gesamten Attribut Speicher anzuzeigen, müssen Sie die Topologie auflösen. Weitere Informationen finden Sie unter [Auflösen einer Topologie mit topoedit](resolving-a-topology-with-topoedit.md).

In der folgenden Tabelle werden die Topologieelemente und die Attribute angezeigt, die im Bereich angezeigt werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Topologieelement</th>
<th>Attribute</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Topologieknoten</td>
<td><ul>
<li><a href="topology-node-attributes.md">Topologieknotenattribute</a> für alle Knoten.<br/></li>
<li><a href="presentation-descriptor-attributes.md">Präsentations deskriptorattribute</a> nur für Quellknoten.<br/></li>
<li>Eingabe-und Ausgabe Vertrauensstellungs Informationen für Transformations-und Ausgabe Knoten.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Knoten Eingabe</td>
<td><ul>
<li><a href="media-type-attributes.md">Medientyp Attribute</a> für alle Knoten.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Knoten Ausgabe</td>
<td><ul>
<li><a href="stream-descriptor-attributes.md">Streamdeskriptorattribute</a> nur für Quellknoten.<br/></li>
<li><a href="media-type-attributes.md">Medientyp Attribute</a> für alle Knoten.<br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Attributwerte, außer Zeiger Verweise und Array Werte, können geändert werden. Um einen Attribut Wert zu ändern, geben Sie den neuen Wert neben dem Attribut ein, und klicken Sie im Bereich **Attribute** auf **Speichern** . Der neue Wert wird im Attribut Speicher aktualisiert und erst dann auf die Topologie angewendet, nachdem er aufgelöst wurde.

## <a name="to-add-a-new-attribute-for-a-node"></a>So fügen Sie ein neues Attribut für einen Knoten hinzu

1.  Wählen Sie den Knoten aus, indem Sie im Bereich **Topologie** darauf klicken.

    Die Attribute, die für den Knoten festgelegt werden, werden im Bereich **Attribute** angezeigt.

2.  Klicken Sie im Bereich **Attribute** auf **Hinzufügen**.

    Dadurch wird das Dialogfeld **Attribut hinzufügen** geöffnet.

3.  Wählen Sie in der ersten Dropdown Liste die Attribut Kategorie aus.

    Die Kategorien sind vom topologieknoten abhängig. Beispielsweise zeigt die Dropdown Liste für den Quellknoten die **Präsentations deskriptorattribute** und **Knoten Attribute** als verfügbare Kategorien an.

4.  Wählen Sie in der zweiten Dropdown Liste das Attribut aus, das Sie für den Knoten festlegen möchten.

5.  Fügen Sie im Bearbeitungsfeld den Wert für das-Attribut hinzu.

6.  Klicken Sie auf **Hinzufügen** , um das Attribut hinzuzufügen und zum Hauptfenster zurückzukehren, oder auf **Abbrechen** , um den Vorgang abzubrechen.

7.  Klicken Sie im Menü **Topologie** auf **Topologie auflösen** , um das neue Attribut auf die Topologie festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 




