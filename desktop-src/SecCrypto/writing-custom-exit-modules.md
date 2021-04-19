---
description: Benutzerdefinierte Beendigungs Module müssen die icertexit-Schnittstelle implementieren, die von der Server-Engine aufgerufen wird.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Schreiben von benutzerdefinierten Exit-Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362632"
---
# <a name="writing-custom-exit-modules"></a>Schreiben von benutzerdefinierten Exit-Modulen

Benutzerdefinierte Beendigungs Module müssen die [**icertexit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) -Schnittstelle implementieren, die von der Server-Engine aufgerufen wird. Die [**icertexit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) -Methode wird von der Server-Engine aufgerufen, wenn das Beendigungs Modul geladen wird. Dadurch kann das Beendigungs Modul eine Initialisierung durchführen und einen Wert zurückgeben, der der Server-Engine mitteilt, welche Arten von Ereignissen eine Benachrichtigung erhalten soll. Die [**icertexit:: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) -Methode muss eine Beschreibungs Zeichenfolge zurückgeben, wenn die Server-Engine Sie anfordert. Die [**icertexit:: notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) -Methode wird von der Server-Engine aufgerufen, um das Beendigungs Modul zu benachrichtigen, dass ein Ereignis aufgetreten ist.

Exit-Module können die [**icertserverexit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) -Schnittstelle aufrufen, die viele der gleichen Methoden wie die [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) -Schnittstelle unterstützt, mit Ausnahme der Methoden [**setcertificateextension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) und [**setcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .

Weitere Informationen zum Entfernen des vorhandenen Beendigungs Moduls und zum Installieren eines neuen Beendigungs Moduls finden Sie im Thema zum Beenden der Modul Anpassung in der-Hilfe.

 

 



