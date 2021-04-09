---
description: Es kann vorkommen, dass eine Instanz, die als untergeordnetes Element einer übergeordneten Klasse erstellt wurde, übergeordnete Klassen ändern muss und das untergeordnete Element einer anderen übergeordneten Klasse werden muss.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Ändern der Vererbung einer Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865676"
---
# <a name="changing-the-inheritance-of-an-instance"></a>Ändern der Vererbung einer Instanz

Es kann vorkommen, dass eine Instanz, die als untergeordnetes Element einer übergeordneten Klasse erstellt wurde, übergeordnete Klassen ändern muss und das untergeordnete Element einer anderen übergeordneten Klasse werden muss. Angenommen, Sie verfügen über eine abgeleitete Klasse, **manualservice**, die einen manuellen Dienst beschreibt, und eine abgeleitete Klasse, **Autoservice**, die einen automatischen Dienst beschreibt. Beide Klassen verfügen über eine große Anzahl von Eigenschaften. Nicht alle Eigenschaften sind identisch. Um einen Dienst von manuell in automatisch zu ändern, müssen Sie auch die Instanz, die den Dienst darstellt, von **manualservice** zu **Autoservice** ändern. In der aktuellen Version von WMI können Sie die [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) -Methode nicht mit dem *pinst* -Parameter aufrufen, der auf eine Instanz von **Autoservice** verweist, und die Schlüsseleigenschaften, die die **manualservice** -Instanz beschreiben. Wenn Sie dies tun, löschen Sie implizit die ursprüngliche **manualservice** -Instanz. Im Wesentlichen können Sie nach dem Einrichten der Klasse einer Instanz nur die übergeordnete Klasse einer Instanz ändern, indem Sie die Instanz löschen und die Instanz als Instanz der neuen übergeordneten Klasse neu erstellen.

Im folgenden Verfahren wird beschrieben, wie Sie eine-Instanz von einer Klasse in eine andere Klasse verschieben.

**So verschieben Sie eine Instanz von einer Klasse in eine andere Klasse**

1.  Löschen Sie die Instanz aus der ursprünglichen Klasse.
2.  Erstellen Sie die-Instanz unter der neuen-Klasse.

    In WMI ist es nicht zulässig, dass Anwendungen eine Instanz verschieben, indem Sie Sie in der neuen Klasse erstellen und anschließend mit dem Schlüssel der ursprünglichen Instanz aktualisieren.

Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

 

 



