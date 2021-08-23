---
description: Verwenden von benutzerdefinierten Eigenschaften.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Verwenden von benutzerdefinierten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee01bc0df80acecec9805ea15cd8da65fa23a441c9c7818a88223aa47b963d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813630"
---
# <a name="using-custom-properties"></a>Verwenden von benutzerdefinierten Eigenschaften

**Verwenden von benutzerdefinierten Eigenschaften.**

Ein wia-Treiber (Windows Image Acquisition) kann eigene benutzerdefinierte Eigenschaften definieren. Aufrufer können benutzerdefinierte Eigenschaften genauso bearbeiten wie normale WIA-Eigenschaften. Allerdings kann nur Ihre Anwendung oder ihr benutzerdefiniertes Benutzeroberflächenmodul auf diese benutzerdefinierten Eigenschaften zugreifen.

WIA-Treiber sollten die benutzerdefinierten Eigenschaften so definieren, dass sie Über Eigenschaftenbezeichner verfügen, die von WIA \_ PRIVATE \_ DEVPROP für Geräteeigenschaften versetzt werden, und WIA \_ PRIVATE \_ ITEMPROP für normale Elementeigenschaften verwenden, z. B. in [IWiaMiniDrv::d rvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx). Weitere Informationen finden Sie unter [Definieren von benutzerdefinierten Eigenschaften.](-wia-defining-custom-properties.md)

Es gibt zwei Möglichkeiten, benutzerdefinierte Parameter an WIA-Treiber zu übergeben.

Die erste Option ist die Verwendung der **IWiaItemExtras::Escape-Methode** (in der Dokumentation zum Plattform-SDK beschrieben). Dies ähnelt der [IStiUSD::Escape-Methode,](https://msdn.microsoft.com/library/ms794396.aspx) ermöglicht Aufrufern jedoch die direkte Verwendung von WIA anstelle von STI-Methoden. Mit **IWiaItemExtras::Escape** können Sie beliebige Informationen an den Treiber übergeben, und der Treiber kann alle Informationen zurückgeben. Der WIA-Dienst verwaltet nur die Puffer, die zwischen dem Aufrufer und dem Treiber übergeben werden.

Die zweite Option ist die Verwendung benutzerdefinierter Eigenschaften. Die Verwendung der **IWiaItemExtras::Escape-Methode** ist flexibler als die Verwendung von benutzerdefinierten WIA-Eigenschaften, aber benutzerdefinierte WIA-Eigenschaften ermöglichen es Ihnen, Informationen im Eigenschaftenstream des Elements zu speichern, sodass der Treiber die Informationen zu einem anderen Zeitpunkt lesen kann.

 

 



