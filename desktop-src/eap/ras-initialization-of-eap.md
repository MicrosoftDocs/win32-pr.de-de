---
title: Zugriffspunkt Initialisierung von EAP
description: Bei der Initialisierung fragt der Zugriffspunkt die Registrierung nach installierten Authentifizierungs Protokollen ab.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185557c4b908780c09714aa9cc7fa4c80399812f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390325"
---
# <a name="access-point-initialization-of-eap"></a>Zugriffspunkt Initialisierung von EAP

Bei der Initialisierung fragt der Zugriffspunkt die Registrierung nach installierten Authentifizierungs Protokollen ab. Der AP ruft dann die exportierte Funktion [**raseapgetinfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) für jedes Authentifizierungsprotokoll auf. Die **raseapgetinfo** -Funktion empfängt einen einzelnen Parameter vom Typ [**PPP \_ EAP \_ Info**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). Der Zugriffspunkt verwendet den **dbewaffnung Type Eid** -Member dieser Struktur, um das Authentifizierungsprotokoll anzugeben. Beachten Sie, dass eine einzelne dll möglicherweise mehr als ein Protokoll unterstützt. Wenn **raseapgetinfo** einen anderen Wert als **No \_ Error** zurückgibt, geht der Zugriffspunkt davon aus, dass das Authentifizierungsprotokoll nicht verfügbar ist.

Bei der Rückgabe von [**raseapgetinfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) enthält die [**PPP- \_ EAP- \_ Informations**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) Struktur Zeiger auf die Funktionen " [**raseapinitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85))", " [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))", " [**raseapmakemess Age**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))" und " [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) " in der EAP-dll. Der AP-Dienst verwendet diese Funktionen für die Interaktion mit dem Authentifizierungsprotokoll. Der AP ruft sofort **raseapinitialize** für jedes Authentifizierungsprotokoll auf, um ihn zu initialisieren. Wenn der Dienst heruntergefahren wird, ruft er erneut **raseapinitialize** auf. dieses Mal wird der *finitialize* -Parameter auf **false** festgelegt, um anzugeben, dass das Authentifizierungsprotokoll heruntergefahren werden soll.

 

 