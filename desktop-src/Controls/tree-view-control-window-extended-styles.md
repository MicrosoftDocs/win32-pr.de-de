---
title: Erweiterte Stile Tree-View Steuerung (kommstrg. h)
description: In diesem Abschnitt werden erweiterte Stile aufgelistet, die beim Erstellen von Strukturansicht-Steuerelementen verwendet werden Der Wert erweiterter Stile ist eine bitweise Kombination dieser Stile.
ms.assetid: b45e7b7c-2c7b-49fa-8679-57c478b2f796
topic_type:
- apiref
api_name:
- TVS_EX_AUTOHSCROLL
- TVS_EX_DIMMEDCHECKBOXES
- TVS_EX_DOUBLEBUFFER
- TVS_EX_DRAWIMAGEASYNC
- TVS_EX_EXCLUSIONCHECKBOXES
- TVS_EX_FADEINOUTEXPANDOS
- TVS_EX_MULTISELECT
- TVS_EX_NOINDENTSTATE
- TVS_EX_NOSINGLECOLLAPSE
- TVS_EX_PARTIALCHECKBOXES
- TVS_EX_RICHTOOLTIP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec20467e6a6bdeb98d57661d30292b55d4532f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366966"
---
# <a name="tree-view-control-extended-styles"></a>Erweiterte Stile Tree-View Steuerung

In diesem Abschnitt werden erweiterte Stile aufgelistet, die beim Erstellen von Strukturansicht-Steuerelementen verwendet werden Der Wert erweiterter Stile ist eine bitweise Kombination dieser Stile.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl> <dt><strong>TVS_EX_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Entfernen Sie die horizontale Schiebe Leiste und den automatischen Bildlauf abhängig von der Mausposition.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl> <dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Einschließendschraffurzustand einschließen, wenn das Steuerelement über den <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> Stil verfügt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl> <dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Gibt an, wie der Hintergrund gelöscht oder ausgefüllt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl> <dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Ruft Informationen zum Kalender Raster ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl> <dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Kontrollkästchen Ausschluss Zustand einschließen, wenn das Steuerelement den <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> Stil hat.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl> <dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Blenden Sie expando-Schaltflächen ein bzw. aus, wenn sich der Mauszeiger oder der Mauszeiger über das Steuerelement bewegt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl> <dt><strong>TVS_EX_MULTISELECT</strong></dt> </dl></td>
<td style="text-align: left;">Wird nicht unterstützt. Darf nicht verwendet werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl> <dt><strong>TVS_EX_NOINDENTSTATE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Die Strukturansicht für die Expando-Schaltflächen nicht einziehen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl> <dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. <strong>Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</strong> Reduzieren Sie das zuvor ausgewählte Struktur Ansichts Element nicht, es sei denn, es hat dasselbe übergeordnete Element wie die neue Auswahl. Dieser Stil muss mit dem <a href="tree-view-control-window-styles.md"><strong>TVS_SINGLEEXPAND</strong></a> Stil verwendet werden. <br/>
<blockquote>
[!Note]<br />
Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht unterstützt. Außerdem ist dieser Stil nicht in "kommctrl. h" definiert. Fügen Sie die folgende Definition zu den Quelldateien Ihrer Anwendung hinzu, um diesen Stil zu verwenden: <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl> <dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Schließt den Teil CheckBox-Zustand ein, wenn das Steuerelement den <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> Stil hat.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl> <dt><strong>TVS_EX_RICHTOOLTIP</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Umfassende Quick Infos in der Strukturansicht zulassen (Benutzer definiert mit Symbol und Text).<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





