---
description: Im Netzwerkmonitor Frame-Viewer werden Analysierte Daten in drei Bereichen angezeigt.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Anzeigen von analysierten Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558312"
---
# <a name="viewing-parsed-information"></a>Anzeigen von analysierten Informationen

Im Netzwerkmonitor Frame-Viewer werden Analysierte Daten in drei Bereichen angezeigt. Im oberen Bereich wird eine Zusammenfassung des Frames angezeigt, in dem das identifizierte Protokoll enthalten ist. Im mittleren Bereich werden die Eigenschaften für formatierte Daten angezeigt, die hierarchisch als Teil der parseranzeige organisiert werden können. Im unteren Bereich werden markierte Rohdaten angezeigt, die im mittleren Bereich ausgewählt werden.

Sie können angeben, wie die Informationen im Viewer angezeigt werden, wenn Sie einen eigenen Parser entwickeln. Die folgende Abbildung zeigt, wie Informationen im Netzwerkmonitor Frame-Viewer angezeigt werden können.

![Netzwerkmonitor-Frame Viewer](images/parseui.png)

> [!Note]  
> Parser zeigen keine Frames an. Parser erkennen Felder in den bereitgestellten Informationen und Benachrichtigen dann Netzwerkmonitor, den Frame anzuzeigen. Das Filtern ist ein Vorgang auf höherer Ebene, der es Filter Abfragen ermöglicht, Parser zu spannen.

 

Verwenden Sie in Ihrem Parser nur Funktionen, die in Microsoft Win32-Anwendungen ausgeführt werden können. Vor dem Anfügen von Eigenschaften an die Rohdaten muss ein Parser zunächst alle möglichen Eigenschaften mit dem Netzwerkmonitor Kernel registrieren. Der Parser sendet eine Nachricht an den Kernel, um eine Eigenschaften Datenbank zu erstellen, und füllt dann die Eigenschaften Datenbank mit jeder möglichen Eigenschaft für das zugehörige Protokoll aus. Jede Eigenschaft in der Eigenschaften Datenbank enthält Informationen, wie z. b. eine Textbeschreibung, einen Datentyp und einen Qualifizierer, die zum Formatieren der Rohdaten verwendet werden, und eine Formatierungs Routine, die zum Anzeigen der Daten verwendet wird.

 

 



