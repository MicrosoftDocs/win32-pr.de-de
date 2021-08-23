---
description: Monitore können Frames im lokalen modus oder im promiscuous-Modus untersuchen.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only und promiscuous-Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8155c968f82154712ec8926f114e63380cdb1099bf7908d5a4dde86d7646dc20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555890"
---
# <a name="local-only-and-promiscuous-modes"></a>Local-Only und promiscuous-Modi

Monitore können Frames im lokalen modus oder im promiscuous-Modus untersuchen.

Im ausschließlich lokalen Modus gibt der Netzwerkpaketanbieter (Network Packet Provider, NPP) Frames zurück, die an oder von dem Computer gesendet werden, auf dem der Monitor ausgeführt wird, einschließlich Broadcasts und Multicasts, die an den lokalen Computer geleitet werden. Obwohl dies auf lokal gerichtete Frames beschränkt ist, ist der lokale Modus auch viel weniger prozessorintensiv.

Im promiscuous-Modus kann der Monitor auch auf Datenverkehr achten, der nicht an den oder vom lokalen Computer geleitet wird. Sofern der Monitor das Flag MCS CREATE PMODE NOT REQUIRED nicht angegeben hat, geht der \_ \_ Monitor Control Service \_ \_ (MCSVC) in der [OnLoadingDLL-Funktion](onloadingdll.md) davon aus, dass der Monitor beim Laden der Monitor-DLL den promiscuous-Modus erfordert.

 

 



