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
# <a name="handling-disc-ejections"></a><span data-ttu-id="d88f6-103">Behandlung von Disc-ejections</span><span class="sxs-lookup"><span data-stu-id="d88f6-103">Handling Disc Ejections</span></span>

<span data-ttu-id="d88f6-104">Wenn der Benutzer eine DVD vom Laufwerk eingibt, sendet der DVD-Navigator eine per EC- \_ DVD \_ \_ ausgeschriebene Nachricht an Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d88f6-104">When the user ejects a DVD from the drive, the DVD Navigator sends your application an EC\_DVD\_DISC\_EJECTED message.</span></span> <span data-ttu-id="d88f6-105">Die Anwendung kann diese Nachricht gefahrlos ignorieren und dem DVD-Navigator erlauben, den Status des Diagramms zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d88f6-105">The application can safely ignore this message and let the DVD Navigator manage the graph's state.</span></span> <span data-ttu-id="d88f6-106">Eine Anwendung kann auch die per EC \_ - \_ DVD \_ ausgeworfene Methode ausführen, um benutzerdefiniertes Verhalten zu implementieren, wenn eine Festplatte aussteht.</span><span class="sxs-lookup"><span data-stu-id="d88f6-106">An application can also handle the EC\_DVD\_DISC\_EJECTED method to implement custom behavior when a disc is ejected.</span></span> <span data-ttu-id="d88f6-107">Wenn Sie die Nachricht verarbeiten, müssen Sie das \_ Flag für die DVD resetonend mit der [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) -Methode auf **true** festlegen und dann [**IMediaControl::**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) End ausführen, bevor Sie die Anwendung schließen oder eine andere Festplatte abspielen.</span><span class="sxs-lookup"><span data-stu-id="d88f6-107">If you handle the message, you must set the DVD\_ResetOnStop flag to **TRUE** with the [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method and then call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) before closing the application or playing another disc.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d88f6-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d88f6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d88f6-109">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d88f6-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



