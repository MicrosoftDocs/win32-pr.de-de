---
title: Selflag-Konstanten (Oleacc. h)
description: In diesem Thema werden die Konstanten Werte beschrieben, die verwendet werden, um anzugeben, wie ein Barrierefreies Objekt ausgewählt wird oder den Fokus erhält.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364691"
---
# <a name="selflag-constants"></a>Selflag-Konstanten

In diesem Thema werden die Konstanten Werte beschrieben, die verwendet werden, um anzugeben, wie ein Barrierefreies Objekt ausgewählt wird oder den Fokus erhält. Die Konstanten werden in Oleacc. h definiert und mit der [**ibarrierefreie:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) -Methode verwendet.

Die folgenden Kombinationen sind nicht zulässig:

-   selflag \_ AddSelection \| selflag \_ RemoveSelection
-   selflag \_ AddSelection \| selflag \_ TakeSelection
-   selflag \_ RemoveSelection \| selflag \_ TakeSelection
-   selflag \_ ExtendSelection \| selflag \_ TakeSelection

**Hinweis für Clients:** Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Edit-und Rich Edit-Steuerelementen enthalten ist, da der Text als Zeichenfolge in der [Value-Eigenschaft](value-property.md)des Objekts verfügbar gemacht wird.

Informationen zum Ausführen komplexer Auswahl Vorgänge finden Sie unter Auswählen von untergeordneten [Objekten](selecting-child-objects.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">Führt keine Aktion aus. Die Auswahl oder der Fokus wird von Microsoft Active Accessibility nicht geändert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </dl></td>
<td style="text-align: left;">Legt den Fokus auf das-Objekt fest und macht ihn zum Auswahl Anker. Mit diesem Flag wird die Auswahl nicht geändert. Der Effekt ähnelt dem manuellen Verschieben des Fokus durch Drücken einer Pfeiltaste, während die STRG-Taste in Windows-Explorer oder in einem Listenfeld mit mehreren Auswahl Punkten gedrückt wird. <br/> Bei Objekten, die über die <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>verfügen, wird SELFLAG_TAKEFOCUS mit den folgenden Werten kombiniert:<br/>
<ul>
<li>SELFLAG_TAKESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li>
</ul>
Wenn Sie <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> mit dem SELFLAG_TAKEFOCUS-Flag für ein Objekt mit einem <strong>HWND</strong>aufgerufen haben, wird das Flag nur wirksam, wenn das übergeordnete Objekt bereits den Fokus besitzt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </dl></td>
<td style="text-align: left;">Wählt das-Objekt aus und entfernt die Auswahl aus allen anderen Objekten im Container. <br/> Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht. Der SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem einfachen Klicken auf ein Element in Windows-Explorer.<br/> Dieses Flag darf nicht mit den folgenden Flags kombiniert werden:<br/>
<ul>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </dl></td>
<td style="text-align: left;">Ändert die Auswahl, sodass alle Objekte zwischen dem Auswahl Anker und diesem Objekt den Auswahl Zustand des Anker Objekts übernehmen. Wenn das Ankerobjekt nicht ausgewählt ist, werden die Objekte aus der Auswahl entfernt. Wenn das Anker Objekt ausgewählt ist, wird die Auswahl so erweitert, dass Sie dieses Objekt und alle Objekte dazwischen enthält. Legen Sie den Auswahl Zustand fest, indem Sie dieses Flag mit SELFLAG_ADDSELECTION oder SELFLAG_REMOVESELECTION kombinieren. <br/> Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht. Der SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Hinzufügen eines Elements zu einer Auswahl, indem die UMSCHALTTASTE gedrückt gehalten und in Windows-Explorer auf ein nicht ausgewähltes Objekt geklickt wird.<br/> Dieses Flag wird nicht mit SELFLAG_TAKESELECTION kombiniert.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </dl></td>
<td style="text-align: left;">Fügt das-Objekt der aktuellen Auswahl hinzu. das mögliche Ergebnis ist eine nicht zusammenhängende Auswahl. <br/> Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht. Der SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Hinzufügen eines Elements zu einer Auswahl, indem Sie die STRG-Taste gedrückt halten und in Windows-Explorer auf ein nicht ausgewähltes Objekt klicken.<br/> Dieses Flag wird nicht mit SELFLAG_REMOVESELECTION oder SELFLAG_TAKESELECTION kombiniert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </dl></td>
<td style="text-align: left;">Entfernt das-Objekt aus der aktuellen Auswahl. das mögliche Ergebnis ist eine nicht zusammenhängende Auswahl. <br/> Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht. Der SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Entfernen eines Elements aus einer Auswahl, indem Sie die STRG-Taste gedrückt halten, während Sie auf ein ausgewähltes Objekt in Windows-Explorer klicken.<br/> Dieses Flag wird nicht mit SELFLAG_ADDSELECTION oder SELFLAG_TAKESELECTION kombiniert.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Auswählen von untergeordneten Objekten](selecting-child-objects.md)
</dt> </dl>

 

 





