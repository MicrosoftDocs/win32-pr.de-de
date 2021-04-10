---
description: Behandlung von Disc-ejections
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Behandlung von Disc-ejections
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859958"
---
# <a name="handling-disc-ejections"></a>Behandlung von Disc-ejections

Wenn der Benutzer eine DVD vom Laufwerk eingibt, sendet der DVD-Navigator eine per EC- \_ DVD \_ \_ ausgeschriebene Nachricht an Ihre Anwendung. Die Anwendung kann diese Nachricht gefahrlos ignorieren und dem DVD-Navigator erlauben, den Status des Diagramms zu verwalten. Eine Anwendung kann auch die per EC \_ - \_ DVD \_ ausgeworfene Methode ausführen, um benutzerdefiniertes Verhalten zu implementieren, wenn eine Festplatte aussteht. Wenn Sie die Nachricht verarbeiten, müssen Sie das \_ Flag für die DVD resetonend mit der [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) -Methode auf **true** festlegen und dann [**IMediaControl::**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) End ausführen, bevor Sie die Anwendung schließen oder eine andere Festplatte abspielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



