---
description: Verwenden von benutzerdefinierten Eigenschaften.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Verwenden von benutzerdefinierten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345074"
---
# <a name="using-custom-properties"></a>Verwenden von benutzerdefinierten Eigenschaften

**Verwenden von benutzerdefinierten Eigenschaften**.

Ein Windows-Abbild Erfassungs Treiber (WIA) kann seine eigenen benutzerdefinierten Eigenschaften definieren. Aufrufer können benutzerdefinierte Eigenschaften genau wie normale WIA-Eigenschaften bearbeiten. Allerdings kann nur Ihre Anwendung oder Ihr benutzerdefiniertes UI-Modul auf diese benutzerdefinierten Eigenschaften zugreifen.

WIA-Treiber sollten die benutzerdefinierten Eigenschaften definieren, damit Eigenschaften Bezeichner vorhanden sind, die von WIA \_ private \_ devprop für Geräteeigenschaften versetzt werden, und \_ \_ für normale Element Eigenschaften, z. b. in [iwiaminidrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx), eine private ItemProp-Eigenschaft verwenden. Weitere Informationen finden Sie unter [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md).

Es gibt zwei Möglichkeiten, benutzerdefinierte Parameter an WIA-Treiber zu übergeben.

Die erste Option ist die Verwendung der **iwiaitemextras:: Escape** -Methode (beschrieben in der Platform SDK-Dokumentation). Dies ähnelt der [istiusd:: Escape-](https://msdn.microsoft.com/library/ms794396.aspx) Methode, lässt jedoch zu, dass Aufrufer WIA direkt anstelle der Verwendung von "STI"-Methoden verwenden können. Mithilfe von **iwiaitemextras:: Escape** können Sie alle Informationen an den Treiber übergeben, und der Treiber kann alle Informationen zurückgeben. Der WIA-Dienst verwaltet nur die Puffer, die zwischen dem Aufrufer und dem Treiber übergeben werden.

Die zweite Option besteht darin, benutzerdefinierte Eigenschaften zu verwenden. Die Verwendung der **iwiaitemextras:: Escape** -Methode ist flexibler als die Verwendung benutzerdefinierter WIA-Eigenschaften, aber benutzerdefinierte WIA-Eigenschaften ermöglichen es Ihnen, Informationen im Eigenschaftenstream des Elements zu speichern, damit der Treiber die Informationen zu einem anderen Zeitpunkt lesen kann.

 

 



