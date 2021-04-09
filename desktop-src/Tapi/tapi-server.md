---
description: Der TAPI-Server (tapisrv) ist das zentrale Repository von Telefoniedaten auf einem Benutzer Computer.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: TAPI-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866912"
---
# <a name="tapi-server"></a>TAPI-Server

Der TAPI-Server (tapisrv) ist das zentrale Repository von Telefoniedaten auf einem Benutzer Computer. Dieser Dienst Prozess verfolgt lokale und Remote Telefonieressourcen, für die Verarbeitung von unterstützten Telefonieanforderungen registrierte Anwendungen und ausstehende asynchrone Funktionen und ermöglicht außerdem eine konsistente Schnittstelle mit Telefoniedienstanbietern (Telefoniedienstanbietern). Weitere Informationen und ein Diagramm, das die Beziehung zwischen dem TAPI-Server und anderen Komponenten und einer Übersicht über seine Rollen veranschaulicht, finden Sie unter [Microsoft Telefonie-Programmiermodell](microsoft-telephony-programming-model.md).

Für Computer, die unter Windows Server 2003-Betriebssystemen, Windows XP und Windows 2000 ausgeführt werden, wird tapisrv innerhalb des Kontexts von Svchost.exe ausgeführt. Für Computer, die unter Windows NT ausgeführt werden, wird dieser als separater Dienst Prozess ausgeführt. Wenn eine Anwendung eine TAPI-dll in ihren Prozessbereich lädt und einen Initialisierungs Vorgang ausführt, stellt die dll einen RPC-Link zum TAPI-Server her. Der TAPI-Server lädt Telefondienstanbieter (TSPS) in seinen Prozessbereich. Unabhängig davon, wie viele Anwendungen auf die Geräte eines bestimmten Anbieters zugreifen, ist nur eine Instanz eines bestimmten TSP vorhanden.

 

 



