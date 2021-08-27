---
title: 'Tree-View-Steuerelement : Erweiterte Stile (CommCtrl.h)'
description: In diesem Abschnitt werden erweiterte Stile aufgelistet, die beim Erstellen von Strukturansichtssteuerelementen verwendet werden. Der Wert erweiterter Stile ist eine bitweise Kombination dieser Stile.
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
ms.openlocfilehash: eed135e5c1cfd335333251c183b408a59d2768ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477386"
---
# <a name="tree-view-control-extended-styles"></a>Tree-View-Steuerelement : Erweiterte Stile

In diesem Abschnitt werden erweiterte Stile aufgelistet, die beim Erstellen von Strukturansichtssteuerelementen verwendet werden. Der Wert erweiterter Stile ist eine bitweise Kombination dieser Stile.




| Konstante | BESCHREIBUNG | 
|----------|-------------|
| <span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl><dt><strong>TVS_EX_AUTOHSCROLL</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Entfernen Sie die horizontale Bildlaufleiste, und scrollen Sie je nach Mausposition automatisch.<br /> | 
| <span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl><dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Schließen Sie den abgeblendeten Kontrollkästchenzustand ein, wenn das Steuerelement über den <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> Stil verfügt.<br /> | 
| <span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl><dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Gibt an, wie der Hintergrund gelöscht oder ausgefüllt wird.<br /> | 
| <span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl><dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Ruft Kalenderrasterinformationen ab.<br /> | 
| <span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl><dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Schließen Sie den Status des Ausschlusskontrollkästchens ein, wenn das Steuerelement über den <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> Stil verfügt.<br /> | 
| <span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl><dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Blenden Sie Expando-Schaltflächen ein oder aus, wenn die Maus weg bewegt wird oder sich in einen Zustand bewegt, in dem der Mauszeiger über das Steuerelement bewegt wird.<br /> | 
| <span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl><dt><strong>TVS_EX_MULTISELECT</strong></dt></dl> | Wird nicht unterstützt. Darf nicht verwendet werden.<br /> | 
| <span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl><dt><strong>TVS_EX_NOINDENTSTATE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Die Strukturansicht für die Expandoschaltflächen sollte nicht eingerückt werden.<br /> | 
| <span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl><dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. <strong>Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen.</strong> Reduzieren Sie das zuvor ausgewählte Strukturansichtselement nur, wenn es über das gleiche übergeordnete Element wie die neue Auswahl verfügt. Dieser Stil muss mit dem <a href="tree-view-control-window-styles.md"><strong>TVS_SINGLEEXPAND</strong></a> Verwendet werden. <br /><blockquote>[!Note]<br />Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht mehr unterstützt. Außerdem ist dieser Stil in commctrl.h nicht definiert. Fügen Sie den Quelldateien Ihrer Anwendung die folgende Definition hinzu, um diesen Stil zu verwenden: <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code></blockquote><br /> | 
| <span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl><dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Fügen Sie den Status eines partiellen Kontrollkästchens ein, wenn das Steuerelement über den <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> Stil verfügt.<br /> | 
| <span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl><dt><strong>TVS_EX_RICHTOOLTIP</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Lassen Sie umfangreiche QuickInfos in der Strukturansicht zu (benutzerdefiniertes Zeichnen mit Symbol und Text).<br /> | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





