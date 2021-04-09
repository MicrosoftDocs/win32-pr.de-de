---
description: TAPI bietet Zugriff auf die Anzeige von Smartphones.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129308"
---
# <a name="display"></a><span data-ttu-id="7a743-103">Anzeige</span><span class="sxs-lookup"><span data-stu-id="7a743-103">Display</span></span>

<span data-ttu-id="7a743-104">TAPI bietet Zugriff auf die Anzeige eines Telefons.</span><span class="sxs-lookup"><span data-stu-id="7a743-104">TAPI provides access to a phone's display.</span></span> <span data-ttu-id="7a743-105">Die Anzeige wird als alphanumerischer Bereich mit Zeilen und Spalten modelliert.</span><span class="sxs-lookup"><span data-stu-id="7a743-105">The display is modeled as an alphanumeric area with rows and columns.</span></span> <span data-ttu-id="7a743-106">Die Gerätefunktionen eines Telefons geben die Größe der Anzeige eines Telefons als Anzahl von Zeilen und die Anzahl der Spalten an.</span><span class="sxs-lookup"><span data-stu-id="7a743-106">A phone's device capabilities indicate the size of a phone's display as the number of rows and the number of columns.</span></span> <span data-ttu-id="7a743-107">Beide Zahlen sind 0 (null), wenn auf dem Telefongerät keine Anzeige vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7a743-107">Both these numbers are zero if the phone device does not have a display.</span></span> <span data-ttu-id="7a743-108">Verwenden Sie " [**phonesetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) ", um Informationen in die Anzeige eines geöffneten Telefon Geräts zu schreiben, und [**phonegetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) , um den aktuellen Inhalt der Anzeige eines Telefons abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7a743-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) to write information to the display of an open phone device, and [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) to retrieve the current contents of a phone's display.</span></span>

<span data-ttu-id="7a743-109">Wenn die Anzeige eines Telefon Geräts geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendungsfunktion gesendet, um die Anwendung über die Statusänderung zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="7a743-109">When the display of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="7a743-110">Die Parameter für diese Nachricht geben Aufschluss über die Änderung.</span><span class="sxs-lookup"><span data-stu-id="7a743-110">Parameters to this message provide an indication of the change.</span></span>

 

 



