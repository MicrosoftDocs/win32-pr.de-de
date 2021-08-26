---
description: Der Netzwerkmonitor Frame-Viewer zeigt analysierte Daten in drei Bereichen an.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Anzeigen analysierter Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f01cfc0df45f2fb6ef0e1342d7fe54e5ed5701bad8ba1635dc13f4546b10e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962685"
---
# <a name="viewing-parsed-information"></a>Anzeigen analysierter Informationen

Der Netzwerkmonitor Frame-Viewer zeigt analysierte Daten in drei Bereichen an. Im oberen Bereich wird eine Zusammenfassung des Frames angezeigt, der das identifizierte Protokoll enthält. Im mittleren Bereich werden die formatierten Dateneigenschaften angezeigt, die im Rahmen der Parseranzeige hierarchisch organisiert werden können. Im unteren Bereich werden hervorgehobene Rohdaten angezeigt, die im mittleren Bereich ausgewählt sind.

Sie können angeben, wie die Informationen im Viewer angezeigt werden, wenn Sie einen eigenen Parser entwickeln. Die folgende Abbildung zeigt, wie Informationen im Netzwerkmonitor Frame-Viewer angezeigt werden können.

![Frame-Viewer des Netzwerkmonitors](images/parseui.png)

> [!Note]  
> Parser zeigen keine Frames an. Parser erkennen Felder in den bereitgestellten Informationen und benachrichtigen dann Netzwerkmonitor, um den Frame anzuzeigen. Das Filtern ist ein Vorgang auf höherer Ebene, mit dem Filterabfragen Parser umfassen können.

 

Verwenden Sie in Ihrem Parser nur Funktionen, die in Microsoft Win32-Anwendungen ausgeführt werden können. Vor dem Anfügen von Eigenschaften an die Rohdaten muss ein Parser zunächst alle möglichen Eigenschaften beim Netzwerkmonitor Kernel registrieren. Der Parser sendet eine Nachricht an den Kernel, um eine Eigenschaftendatenbank zu erstellen, und füllt dann die Eigenschaftendatenbank mit jeder möglichen Eigenschaft für sein Protokoll auf. Jede Eigenschaft in der Eigenschaftendatenbank enthält Informationen wie eine Textbeschreibung, einen Datentyp und einen Qualifizierer, die zum Formatieren der Rohdaten verwendet werden, und eine Formatierungsroutine, die zum Anzeigen der Daten verwendet wird.

 

 



