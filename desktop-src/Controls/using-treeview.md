---
title: Verwenden von Tree-View-Steuerelementen
description: Dieser Abschnitt enthält Implementierungsdetails und Beispielcode für die Arbeit mit Strukturansichtssteuerelementen.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8beac9ef5163b52582a2ea89820278cc10f9f68ad865354404efd72a61b04993
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318589"
---
# <a name="using-tree-view-controls"></a>Verwenden von Tree-View-Steuerelementen

Dieser Abschnitt enthält Implementierungsdetails und Beispielcode für die Arbeit mit Strukturansichtssteuerelementen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen eines Tree-View-Steuerelements](create-a-tree-view-control.md)<br/>       | Verwenden Sie zum Erstellen eines Strukturansichtssteuerelements die [**CreateWindowEx-Funktion,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) und geben Sie den [**WC \_ TREEVIEW-Wert**](common-control-window-classes.md) für die Fensterklasse an. Die Strukturansichtsfensterklasse wird im Adressraum der Anwendung registriert, wenn die allgemeine Steuerelement-DLL geladen wird. Um sicherzustellen, dass die DLL geladen wird, verwenden Sie die [**InitCommonControls-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) <br/>                                                                    |
| [Initialisieren der Bildliste](initialize-the-image-list.md)<br/>         | Jedem Element in einem Strukturansichtssteuerelement können zwei Bilder zugeordnet sein. Ein Element zeigt ein Bild an, wenn es ausgewählt ist, und das andere, wenn es nicht ausgewählt ist. Verwenden Sie zum Einschließen von Bildern mit Strukturansichtselementen zunächst die [Bildlistenfunktionen,](image-lists.md) um eine Bildliste zu erstellen und ihr Bilder hinzuzufügen. Ordnen Sie dann die Bildliste mithilfe der [**TVM \_ SETIMAGELIST-Nachricht**](tvm-setimagelist.md) dem Strukturansichtssteuerelement zu. <br/>                                                                     |
| [Hinzufügen von Tree-View Elementen](add-tree-view-items.md)<br/>                     | Sie fügen einem Strukturansichtssteuerelement ein Element hinzu, indem Sie die [**TVM \_ INSERTITEM-Nachricht**](tvm-insertitem.md) an das Steuerelement senden. Die Nachricht enthält die Adresse einer [**TVINSERTSTRUCT-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) die das übergeordnete Element, das Element, nach dem das neue Element eingefügt wird, und eine [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) angibt, die die Attribute des Elements definiert. Zu den Attributen gehören die Bezeichnung des Elements, die ausgewählten und nicht ausgewählten Bilder und ein von der Anwendung definierter 32-Bit-Wert. <br/> |
| [Ziehen eines Tree-View Elements](drag-a-tree-view-item.md)<br/>                 | In diesem Thema wird Code zum Ziehen und Löschen von Strukturansichtselementen veranschaulicht. Der Beispielcode besteht aus drei Funktionen. Die erste Funktion startet den Ziehvorgang, die zweite Funktion zieht das Bild, und die dritte Funktion beendet den Ziehvorgang. <br/>                                                                                                                                                                                                                                  |
| [Arbeiten mit Zustandsbildindizes](work-with-state-image-indexes.md)<br/> | Es gibt häufig Verwirrung darüber, wie der Zustandsbildindex in einem Strukturansichtssteuerelement festgelegt und abgerufen wird. Die folgenden Beispiele veranschaulichen die richtige Methode zum Festlegen und Abrufen des Zustandsbildindexes. In den Beispielen wird davon ausgegangen, dass nur zwei Zustandsbildindizes im Strukturansichtssteuerelement vorhanden sind: deaktiviert und aktiviert. Wenn Ihre Anwendung mehr als zwei Enthält, müssen diese Funktionen geändert werden, um diesen Fall zu behandeln. <br/>                                                               |
| [Verwenden von Tree-View InfoTips](use-tree-view-infotips.md)<br/>               | Wenn Sie den [**TVS \_ INFOTIP-Stil**](tree-view-control-window-styles.md) auf ein Strukturansichtssteuerelement anwenden, werden [TVN \_ GETINFOTIP-Benachrichtigungen](tvn-getinfotip.md) generiert, wenn sich der Cursor über einem Element in der Strukturansicht befindet. Wenn Sie auf diese Benachrichtigung reagieren, können Sie den Text festlegen, der in der Infotip angezeigt wird. <br/>                                                                                                                                                                                    |



 

 

