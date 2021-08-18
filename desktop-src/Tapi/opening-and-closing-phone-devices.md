---
description: Nachdem die Funktionen eines Telefongeräts bestimmt wurden, muss eine Anwendung das Gerät öffnen, bevor sie auf Funktionen auf diesem Telefon zugreifen kann.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Öffnen und Schließen Telefon Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dacda3e98e96ed4a11334443a7b99b949e6d1b3823e42e1790c5a346b52dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012520"
---
# <a name="opening-and-closing-phone-devices"></a>Öffnen und Schließen Telefon Geräten

Nachdem die Funktionen eines Telefongeräts bestimmt wurden, muss eine Anwendung das Gerät öffnen, bevor sie auf Funktionen auf diesem Telefon zugreifen kann. Nachdem ein Telefongerät erfolgreich geöffnet wurde, wird der Anwendung ein Handle zurückgegeben, das das geöffnete Telefon darstellt. Ein Telefongerät kann in verschiedenen Modi geöffnet werden, wodurch eine strukturierte Möglichkeit zum Freigeben eines Telefongeräts zur Verfügung stehen kann.

Die [**phoneOpen-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) öffnet das angegebene Telefongerät, um der Anwendung Zugriff auf Funktionen auf dem Smartphone zu geben. Ein Telefongerät wird als **phoneOpen identifiziert,** indem seine Geräte-ID verwendet wird, die als *dwDeviceID-Parameter übergeben* wird.

 

 



