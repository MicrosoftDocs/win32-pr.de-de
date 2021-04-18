---
title: Gegenseitige Authentifizierung mithilfe von Kerberos
description: Die gegenseitige Authentifizierung ist eine Sicherheitsfunktion, bei der ein Client Prozess die Identität eines Diensts nachweisen muss, und der Dienst muss die Identität des Clients nachweisen, bevor der Anwendungs Datenverkehr über die Client-/Dienst-Verbindung übertragen wird.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, Verwendung von gegenseitiger Authentifizierung
- Active Directory, Verwendung, Sicherheit, gegenseitige Authentifizierung
- Sicherheits-AD
- Sicherheits-AD, gegenseitige Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106340258"
---
# <a name="mutual-authentication-using-kerberos"></a>Gegenseitige Authentifizierung mithilfe von Kerberos

Die gegenseitige Authentifizierung ist eine Sicherheitsfunktion, bei der ein Client Prozess die Identität eines Diensts nachweisen muss, und der Dienst muss die Identität des Clients nachweisen, bevor der Anwendungs Datenverkehr über die Client-/Dienst-Verbindung übertragen wird.

Active Directory Domain Services und Windows unterstützen Dienst Prinzipal Namen (Service Principal Names, SPN), bei denen es sich um eine Schlüsselkomponente im Kerberos-Mechanismus handelt, mit der ein Client einen Dienst authentifiziert. Ein SPN ist ein eindeutiger Name, der eine Instanz eines Diensts identifiziert und dem Anmelde Konto zugeordnet ist, unter dem die Dienst Instanz ausgeführt wird. Die Komponenten eines SPN sind so, dass ein Client einen SPN für einen Dienst ohne das Dienst Anmelde Konto verfassen kann. Dies ermöglicht es dem Client, den Dienst zum Authentifizieren seines Kontos aufzufordern, auch wenn der Client nicht über den Kontonamen verfügt.

Dieser Abschnitt enthält eine Übersicht über:

-   Gegenseitige Authentifizierung mithilfe von Kerberos.
-   Erstellen eines eindeutigen SPN.
-   Gibt an, wie ein Dienst Installationsprogramm SPNs für das Konto Objekt registriert, das einer Dienst Instanz zugeordnet ist.
-   Wie eine Client Anwendung das Dienst Verbindungspunkt-Objekt (Service Connection Point, Dienst Verbindungspunkt) einer Dienst Instanz in Active Directory Domain Services verwendet, um Daten abzurufen, aus denen ein SPN für den Dienst verfasst werden soll.
-   Wie eine Client Anwendung einen Dienst-SPN in Verbindung mit der Security Support Provider Interface (SSPI) zum Authentifizieren des Diensts verwendet.
-   Ein Codebeispiel für eine Windows Sockets-Client-/Dienst-Anwendung, die einen SCP und SSPI verwendet, um die gegenseitige Authentifizierung auszuführen.
-   Ein Codebeispiel für einen RPC-Client/-Dienst, der die gegenseitige Authentifizierung mit dem RPC-Namensdienst und der RPC-Authentifizierung ausführt.
-   Verwendung von SPNs für die gegenseitige Authentifizierung durch einen Windows Sockets Registration and Resolution-Dienst (RNR).

In diesem Abschnitt wird die Verwendung Active Directory-Domäne Dienstanbieter für die gegenseitige Authentifizierung erläutert, insbesondere der Zweck von Dienst Verbindungs Punkten und Dienst Prinzipal Namen bei gegenseitiger Authentifizierung. Es handelt sich nicht um eine umfassende Erörterung der Verwendung von SSPI für die gegenseitige Authentifizierung oder die Authentifizierungs-und Sicherheitsunterstützung, die für RPC-und Windows Sockets-Anwendungen verfügbar ist.

Weitere Informationen finden Sie unter

-   [Veröffentlichen mit Dienst Verbindungs Punkten](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 