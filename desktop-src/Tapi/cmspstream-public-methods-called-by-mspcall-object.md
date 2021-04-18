---
description: Die folgende Liste enthält die cmspstream-Methoden, die vom mspcalljekt aufgerufen werden.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Vom mspcallcenter-Objekt aufgerufene cmspstream-Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351792"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>Vom mspcallcenter-Objekt aufgerufene öffentliche cmspstream-Methoden



| Öffentliche cmspstream-Methoden                                 | BESCHREIBUNG                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Init**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | Wird von **mspcallaufgerufen** , wenn der Stream erstellt wird.                                   |
| [**Abschlusses**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | Wird von **mspcallaufgerufen** , um die Auswahl aller Terminal Objekte aufzuheben und das Aufruf Objekt freizugeben. |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | Wird vom mspcallobjekt aufgerufen, um den aktuellen Status des Streams abzurufen.                   |
| [**Handletspdata**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | Das abgeleitete calltobjekt kann diese Methode aufzurufen, damit der Stream die TSP-Befehle behandelt.     |
| [**Processgraphevent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | Wird vom mspcallobjekt aufgerufen, damit der Stream Diagramm Ereignisse behandelt.                     |



 

 

 



