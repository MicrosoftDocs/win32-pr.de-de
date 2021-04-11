---
title: Popup-Menü Unterstützung
description: Popup-Menü Unterstützung
ms.assetid: a8a1cf91-c18a-497f-89a7-b47536eaca0a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890d7eab6595200cb00e8422644b10f39807bab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315038"
---
# <a name="pop-up-menu-support"></a>Popup-Menü Unterstützung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Der Microsoft-Agent enthält für jedes Zeichen ein Popup Menü (auch als Kontextmenü bezeichnet). Der Server zeigt dieses Popup Menü automatisch an, wenn ein Benutzer mit der rechten Maustaste auf das Zeichen klickt. Sie können dem Menübefehle für Ihre Client Anwendung hinzufügen, indem Sie eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren. Für jeden Befehl in der Auflistung, den Sie definieren, können Sie [**Beschriftung**](caption-property.md) und [**sichtbare**](visible-property.md) Eigenschaften angeben. Die **Beschriftung** ist der Text, der im Menü angezeigt wird, wenn die **Visible** -Eigenschaft auf **true** festgelegt ist. Sie können auch die [**aktivierte**](enabled-property.md) Eigenschaft verwenden, um den Befehl im Menü als deaktiviert anzuzeigen, und [**HelpContextID**](helpcontextid-property.md) , um Hilfe Unterstützung für die Eigenschaft zu unterstützen. Definieren Sie den Zugriffsschlüssel für den Menütext, indem Sie ein kaufmännisches und-Zeichen (&) vor dem Textzeichen der **Beschriftungs** Texteinstellung einschließen.

Der Server fügt automatisch die Menübefehle zum Öffnen des Fensters "Sprachbefehle" hinzu und blendet das Zeichen sowie die [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) für andere Clients des Zeichens aus, damit Benutzer zwischen Clients wechseln können. Der Server fügt dem Menü automatisch ein Trennzeichen zwischen den Menüeinträgen und den vom Client definierten Menüeinträgen hinzu. Trennzeichen werden nur angezeigt, wenn im Menü Elemente getrennt sind.

Um Befehle aus einem Menü zu entfernen, verwenden Sie die [**Remove**](remove-method.md) -Methode. Beachten Sie, dass Menüeinträge nicht geändert werden, während das Menü angezeigt wird. Wenn Sie Befehle hinzufügen oder entfernen oder deren Eigenschaften ändern, werden die Änderungen im Menü angezeigt, wenn der Benutzer das Menü erneut anzeigt.

Wenn Sie Ihre eigenen Popup-Menü Dienste für ein Zeichen bereitstellen möchten, können Sie mit der [**autopopupmenu**](autopopupmenu-property.md) -Eigenschaft die Server Behandlung der Rechtsklick Aktion deaktivieren. Sie können dann die [**Click**](click-event.md) -Ereignis Benachrichtigung verwenden, um ein eigenes Menü Behandlungs Verhalten zu erstellen.

Wenn der Benutzer einen Befehl aus dem Popupmenü eines Zeichens oder dem Fenster "Sprachbefehle" auswählt, löst der Server das [**Befehls**](command-event.md) Ereignis des zugeordneten Clients aus und übergibt die Parameter der Eingabe mithilfe des [**UserInput**](/windows/desktop/lwef/iagentuserinput) -Objekts zurück.

Der Server stellt außerdem ein Popup Menü für das Symbol der Taskleiste des Zeichens bereit. Wenn das Zeichen angezeigt wird, klicken Sie mit der rechten Maustaste auf dieses Menü, um dieselben Befehle anzuzeigen, die durch Klicken mit der rechten Maustaste auf das Zeichen angezeigt werden. Wenn das Zeichen jedoch ausgeblendet wird, werden nur die vom Server bereitgestellten Befehle eingeschlossen.

 

 