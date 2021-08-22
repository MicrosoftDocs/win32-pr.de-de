---
title: Access Point Initialization of EAP
description: Bei der Initialisierung fragt der Zugriffspunkt (ACCESS POINT, AP) die Registrierung nach installierten Authentifizierungsprotokollen ab.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ff650df29a446527224d8160b4080a252d525d26d32efedae254755ac9514a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984430"
---
# <a name="access-point-initialization-of-eap"></a>Access Point Initialization of EAP

Bei der Initialisierung fragt der Zugriffspunkt (ACCESS POINT, AP) die Registrierung nach installierten Authentifizierungsprotokollen ab. Die AP ruft dann die exportierte Funktion [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) für jedes Authentifizierungsprotokoll auf. Die **RasEapGetInfo-Funktion** empfängt einen einzelnen Parameter vom Typ [**EQ \_ EAP \_ INFO**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). Die AP verwendet den **dwEapTypeId-Member** dieser Struktur, um das Authentifizierungsprotokoll anzugeben. Beachten Sie, dass eine einzelne DLL möglicherweise mehr als ein Protokoll unterstützt. Wenn **RasEapGetInfo** einen anderen Wert als **NO \_ ERROR** zurückgibt, geht die AP davon aus, dass das Authentifizierungsprotokoll nicht verfügbar ist.

Bei der Rückgabe von [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) enthält die [**\_ EAP \_ INFO-Struktur von ADR**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) Zeiger auf die Funktionen [**RasEapInitialize,**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)) [**RasEapBegin,**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))und [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) in der EAP-DLL. Der AP-Dienst verwendet diese Funktionen, um mit dem Authentifizierungsprotokoll zu zusammenarbeiten. Die AP ruft sofort **RasEapInitialize** für jedes Authentifizierungsprotokoll auf, um es zu initialisieren. Wenn der Dienst heruntergefahren wird, ruft er **Erneut RasEapInitialize** auf. Dieses Mal wird der *fInitialize-Parameter* auf **FALSE** festgelegt, um anzugeben, dass das Authentifizierungsprotokoll sich selbst herunterfahren soll.

 

 