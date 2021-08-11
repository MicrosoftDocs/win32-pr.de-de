---
description: Anzeigen von Topologieinformationen
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Anzeigen von Topologieinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fd1d7d28de3d7fa5420241abf793295323532dca29d3d68d1271545aa460dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237372"
---
# <a name="viewing-topology-information"></a>Anzeigen von Topologieinformationen

In TopoEdit verfügt jedes Topologieelement, z. B. Knoten, Knoteneingaben und Knotenausgabe, über einen zugeordneten Attributspeicher, der das Verhalten des Knotens verwaltet. Um die Attribute anzuzeigen, wählen Sie das Element aus, und **im Bereich Attribute werden** die Informationen angezeigt. Bei Topologien, die aus einer XML-Datei geladen werden, zeigen einige Knoten möglicherweise nicht den gesamten Attributspeicher an. Um den gesamten Attributspeicher zu sehen, lösen Sie die Topologie auf. Weitere Informationen finden Sie unter [Auflösen einer Topologie mit TopoEdit](resolving-a-topology-with-topoedit.md).

Die folgende Tabelle zeigt das Topologieelement und die Attribute, die im Bereich angezeigt werden.



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
<li><a href="topology-node-attributes.md">Topologieknotenattribute für</a> alle Knoten.<br/></li>
<li><a href="presentation-descriptor-attributes.md">Präsentationsdeskriptorattribute nur</a> für Quellknoten.<br/></li>
<li>Informationen zur Eingabe- und Ausgabevertrauensstellungsstelle für Transformations- und Ausgabeknoten.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Knoteneingabe</td>
<td><ul>
<li><a href="media-type-attributes.md">Medientypattribute für</a> alle Knoten.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Knotenausgabe</td>
<td><ul>
<li><a href="stream-descriptor-attributes.md">Streamdeskriptorattribute nur</a> für Quellknoten.<br/></li>
<li><a href="media-type-attributes.md">Medientypattribute für</a> alle Knoten.<br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Attributwerte, mit Ausnahme von Zeigerverweisen und Arraywerten, können geändert werden. Um einen Attributwert zu ändern, geben Sie den  neuen Wert neben dem Attribut ein, und klicken Sie im **Bereich Attribute auf Speichern.** Der neue Wert wird im Attributspeicher aktualisiert und erst auf die Topologie angewendet, nachdem er aufgelöst wurde.

## <a name="to-add-a-new-attribute-for-a-node"></a>So fügen Sie ein neues Attribut für einen Knoten hinzu

1.  Wählen Sie den Knoten aus, indem Sie im **Topologiebereich darauf klicken.**

    Die Attribute, die auf dem Knoten festgelegt sind, werden im **Bereich Attribute angezeigt.**

2.  Klicken Sie **im Bereich Attribute** auf **Hinzufügen.**

    Dadurch wird das **Dialogfeld Attribut** hinzufügen geöffnet.

3.  Wählen Sie in der ersten Dropdownliste die Kategorie Attribut aus.

    Die Kategorien hängen vom Topologieknoten ab. Für den Quellknoten werden in der Dropdownliste beispielsweise **Presentation Descriptor Attributes (Präsentationsdeskriptorattribute)** und **Node Attributes** (Knotenattribute) als verfügbare Kategorien angezeigt.

4.  Wählen Sie in der zweiten Dropdownliste das Attribut aus, das Sie auf dem Knoten festlegen möchten.

5.  Fügen Sie im Bearbeitungsfeld den Wert für das Attribut hinzu.

6.  Klicken **Sie auf** Hinzufügen, um das Attribut hinzuzufügen und zum Hauptfenster zurückzukehren, oder klicken Sie **auf** Abbrechen, um den Vorgang abzubricht.

7.  Klicken Sie **im Menü** Topologie auf **Topologie auflösen,** um das neue Attribut auf die Topologie zu setzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




