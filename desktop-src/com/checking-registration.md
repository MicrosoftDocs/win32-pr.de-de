---
title: Überprüfen der Registrierung
description: Überprüfen der Registrierung
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d7f03f1d76b780b49bec5d744a02beca9a3dc45417bf8c6efddd8ff5a9e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501650"
---
# <a name="checking-registration"></a>Überprüfen der Registrierung

Jedes Mal, wenn eine Anwendung geladen wird, sollte ihre Registrierung überprüft werden, um Folgendes zu ermitteln:

-   Gibt an, ob die CLSIDs in der Registrierung vorhanden sind. Wenn sie nicht vorhanden sind, sollte sich die Anwendung als ursprüngliches Setup registrieren.
-   Gibt an, ob die CLSIDs der Anwendung im Register vorhanden sind, aber keine OLE 2-bezogenen Informationen enthalten. Wenn dies der Fall ist, sollte sich die Anwendung als ursprüngliches Setup registrieren.
-   Gibt an, ob der Pfad mit den Servereinträgen[(LocalServer](localserver.md) und [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) und [InprocServer32](inprocserver32.md)und [DefaultIcon)](defaulticon.md)auf den Speicherort verweist, an dem die Anwendung derzeit installiert ist. Wenn der Pfad dies nicht tut, schreiben Sie die Pfadeinträge so um, dass sie auf den aktuellen Speicherort verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 




