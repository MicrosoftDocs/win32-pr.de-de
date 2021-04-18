---
title: Verwenden von Tree-View Steuerelementen
description: Dieser Abschnitt enthält Implementierungsdetails und Beispielcode für die Arbeit mit Strukturansicht-Steuerelementen.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9ed8d1040a635964e772b8399a5c476e67f9aba
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338496"
---
# <a name="using-tree-view-controls"></a>Verwenden von Tree-View Steuerelementen

Dieser Abschnitt enthält Implementierungsdetails und Beispielcode für die Arbeit mit Strukturansicht-Steuerelementen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen eines Tree-View-Steuer Elements](create-a-tree-view-control.md)<br/>       | Um ein Strukturansicht-Steuerelement zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", die den [**WC- \_ TreeView**](common-control-window-classes.md) -Wert für die Fenster Klasse angibt. Die Strukturansicht-Fenster Klasse wird beim Laden der allgemeinen Steuerelement-DLL im Adressraum der Anwendung registriert. Um sicherzustellen, dass die dll geladen wird, verwenden Sie die Funktion [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) . <br/>                                                                    |
| [Initialisieren der Bildliste](initialize-the-image-list.md)<br/>         | Jedem Element in einem Strukturansicht-Steuerelement können zwei Bilder zugeordnet werden. Ein Element zeigt ein Bild an, wenn es ausgewählt wird, und das andere, wenn dies nicht der Fall ist. Um Bilder in Struktur Ansichts Elemente einzuschließen, verwenden Sie zuerst die Funktionen der [Bild](image-lists.md) Liste, um eine Bildliste zu erstellen und Ihr Bilder hinzuzufügen. Ordnen Sie dann die Bildliste dem Strukturansicht-Steuerelement mithilfe der [**TVM-Meldung " \_ SetImageList**](tvm-setimagelist.md) " zu. <br/>                                                                     |
| [Vorgehensweise beim Hinzufügen von Tree-View Elementen](add-tree-view-items.md)<br/>                     | Sie fügen ein Element zu einem Strukturansicht-Steuerelement hinzu, indem Sie die [**TVM \_ InsertItem**](tvm-insertitem.md) -Meldung an das Steuerelement senden. Die Nachricht enthält die Adresse einer [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) -Struktur, die das übergeordnete Element, das Element, nach dem das neue Element eingefügt wird, und eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die die Attribute des Elements definiert, angibt. Die Attribute enthalten die Bezeichnung des Elements, die ausgewählten und nicht ausgewählten Images sowie einen von der 32-Bit-Anwendung definierten Wert. <br/> |
| [Ziehen eines Tree-View Elements](drag-a-tree-view-item.md)<br/>                 | In diesem Thema wird der Code für die Behandlung von Drag & Drop von Struktur Ansichts Elementen veranschaulicht. Der Beispielcode besteht aus drei Funktionen. Die erste Funktion startet den Zieh Vorgang, die zweite Funktion zieht das Bild, und die dritte Funktion beendet den Zieh Vorgang. <br/>                                                                                                                                                                                                                                  |
| [Arbeiten mit Zustands Image Indizes](work-with-state-image-indexes.md)<br/> | Häufig gibt es Verwirrung beim Festlegen und Abrufen des Zustands Bild Indexes in einem Strukturansicht-Steuerelement. In den folgenden Beispielen wird die richtige Methode zum Festlegen und Abrufen des Zustands Bild Indexes veranschaulicht. In den Beispielen wird davon ausgegangen, dass im Strukturansicht-Steuerelement nur zwei Status Bild Indizes vorhanden sind, deaktiviert und überprüft werden. Wenn die Anwendung mehr als zwei enthält, müssen diese Funktionen geändert werden, um diesen Fall zu verarbeiten. <br/>                                                               |
| [Verwenden von Tree-View infotips](use-tree-view-infotips.md)<br/>               | Wenn Sie den [**\_ infotip**](tree-view-control-window-styles.md) -Stil für das TV auf ein Strukturansicht-Steuerelement anwenden, werden [TVN \_ getinfotip](tvn-getinfotip.md) -Benachrichtigungen generiert, wenn sich der Cursor über einem Element in der Strukturansicht befindet. Wenn Sie auf diese Benachrichtigung reagieren, können Sie den Text festlegen, der im infotip angezeigt wird. <br/>                                                                                                                                                                                    |



 

 

