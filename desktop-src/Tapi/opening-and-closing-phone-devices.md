---
description: Nachdem Sie die Funktionen eines Telefon Geräts ermittelt haben, muss eine Anwendung das Gerät öffnen, bevor es auf die Funktionen auf diesem Telefon zugreifen kann.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Öffnen und Schließen von Telefongeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345779"
---
# <a name="opening-and-closing-phone-devices"></a>Öffnen und Schließen von Telefongeräten

Nachdem Sie die Funktionen eines Telefon Geräts ermittelt haben, muss eine Anwendung das Gerät öffnen, bevor es auf die Funktionen auf diesem Telefon zugreifen kann. Nachdem ein Telefongerät erfolgreich geöffnet wurde, wird der Anwendung ein Handle zurückgegeben, das das geöffnete Telefon darstellt. Ein Telefongerät kann in verschiedenen Modi geöffnet werden, sodass eine strukturierte Methode zur Freigabe eines Telefon Geräts bereitgestellt wird.

Die [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) -Funktion öffnet das angegebene Telefongerät, damit die Anwendung Zugriff auf Funktionen auf dem Telefon erhält. Ein Telefongerät wird mit dem zugehörigen Geräte Bezeichner als **phoneopen** identifiziert, das als *dwtoviceid* -Parameter übergeben wird.

 

 



