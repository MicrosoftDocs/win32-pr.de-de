---
title: Registrierung wird überprüft
description: Registrierung wird überprüft
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947531"
---
# <a name="checking-registration"></a>Registrierung wird überprüft

Jedes Mal, wenn eine Anwendung geladen wird, sollte die Registrierung überprüft werden, um Folgendes zu bestimmen:

-   Gibt an, ob die CLSIDs in der Registrierung vorhanden sind. Wenn Sie nicht vorhanden sind, sollte die Anwendung als ursprüngliches Setup registriert werden.
-   Gibt an, ob die CLSIDs der Anwendung im Register vorhanden sind, aber keine OLE 2-bezogenen Informationen enthalten. Wenn dies der Fall ist, sollte die Anwendung als ursprüngliches Setup registriert werden.
-   Gibt an, ob der Pfad mit den Server Einträgen ([LocalServer](localserver.md) und [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) und [InProcServer32](inprocserver32.md)und [DefaultIcon](defaulticon.md)) auf den Speicherort verweist, an dem die Anwendung zurzeit installiert ist. Wenn der Pfad nicht, schreiben Sie die Pfad Einträge so um, dass Sie auf den aktuellen Speicherort zeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 




