---
description: Der TAPI-Server (TAPISRV) ist das zentrale Repository für Telefoniedaten auf einem Benutzercomputer.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: TAPI-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19eb335ddef68f5f4cc588e34edab4931ad8be1e5e1d768e07a142989afe2291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002678"
---
# <a name="tapi-server"></a>TAPI-Server

Der TAPI-Server (TAPISRV) ist das zentrale Repository für Telefoniedaten auf einem Benutzercomputer. Dieser Dienstprozess verfolgt lokale und Remotetelefonieressourcen, Anwendungen, die für die Verarbeitung von telefonunterstützten Telefonieanforderungen registriert sind, sowie ausstehende asynchrone Funktionen und ermöglicht außerdem eine konsistente Schnittstelle mit Telefoniedienstanbietern (TSPs). Weitere Informationen und ein Diagramm, das die Beziehung des TAPI-Servers zu anderen Komponenten und eine Übersicht über ihre Rollen veranschaulicht, finden Sie unter [Microsoft-Telefonieprogrammiermodell](microsoft-telephony-programming-model.md).

Für Computer, die auf Windows Server 2003-Betriebssystemen, Windows XP und Windows 2000 ausgeführt werden, wird TAPISRV im Kontext Svchost.exe. Für Computer, die auf Windows NT ausgeführt werden, wird sie als separater Dienstprozess ausgeführt. Wenn eine Anwendung eine TAPI-DLL in ihren Prozessbereich lädt und einen Initialisierungsvorgang ausführt, richtet die DLL eine RPC-Verknüpfung mit dem TAPI-Server ein. Der TAPI-Server lädt Telefondienstanbieter (TSPs) in seinen Prozessbereich. Unabhängig davon, wie viele Anwendungen auf die Geräte eines bestimmten Anbieters zugreifen, ist nur eine Instanz eines bestimmten TSP vorhanden.

 

 



