---
description: Monitore können Frames im reinen Modus oder im gemischten-Modus untersuchen.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only-und Promiscuous-Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354512"
---
# <a name="local-only-and-promiscuous-modes"></a>Local-Only-und Promiscuous-Modi

Monitore können Frames im reinen Modus oder im gemischten-Modus untersuchen.

Im reinen Modus gibt der Netzwerk Paketanbieter (NPP) Frames zurück, die an den bzw. von dem Computer gesendet werden, auf dem der Monitor ausgeführt wird, einschließlich der Übertragungen und mit, die an den lokalen Computer weitergeleitet werden. Der lokale Modus ist zwar auf Lokal gesteuerte Frames beschränkt, aber auch der lokale Modus ist weitaus weniger Prozessor intensiv.

Im gemischten-Modus kann der Monitor auch auf Datenverkehr achten, der nicht an den lokalen Computer weitergeleitet wird. Wenn für den Monitor nicht das Flag, MCS \_ Create \_ pmode \_ , \_ in der [onloadingdll](onloadingdll.md) -Funktion nicht erforderlich angegeben ist, geht der Monitor Steuerungs Dienst (Monitor Control Service, mcsvc) davon aus, dass der Monitor beim Laden der Monitor-DLL den gemischten-Modus erfordert.

 

 



