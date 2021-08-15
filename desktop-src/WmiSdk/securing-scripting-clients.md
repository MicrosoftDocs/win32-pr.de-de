---
description: Skripts Visual Basic Anwendungen müssen DCOM-Sicherheit festlegen, insbesondere für den Remotezugriff, und möglicherweise müssen auch Berechtigungen aktiviert werden.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Sichern von Skriptclients
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a84e426071c71cfc51f13711eb6bbf133c6a176ca39d08fec92b87a1924006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922968"
---
# <a name="securing-scripting-clients"></a>Sichern von Skriptclients

Skripts Visual Basic Anwendungen müssen DCOM-Sicherheit festlegen, insbesondere für den Remotezugriff, und möglicherweise müssen auch Berechtigungen aktiviert werden.

## <a name="default-access-permissions"></a>Standardzugriffsberechtigungen

Der WMI-Zugriff unterscheidet sich zwischen lokalen computern und Remotecomputern. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

Im Folgenden finden Sie die Standardzugriffsberechtigungen nach Konto:

-   Everyone, LocalService, NetworkService

    Berechtigung zum Lesen oder Schreiben von Daten und zum Ausführen [*von Anbietermethoden*](gloss-p.md) auf dem lokalen Computer. Diese Konten können keine neuen Klassen erstellen oder neue Anbieter installieren.

-   Administratorkonten

    Vollsteuerung auf dem lokalen Computer. Beim Herstellen einer Verbindung mit einem Remotecomputer muss das Konto auch ein lokaler Administrator auf dem Remotecomputer sein.

## <a name="securing-a-scripting-client"></a>Sichern eines Skriptclients

WMI-Skripts und Visual Basic müssen DCOM-Sicherheitsebenen entsprechend den Betriebssystemen festlegen, auf die sie abzielen. Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsebene mit VBScript](setting-the-default-process-security-level-using-vbscript.md).

Wenn Sie eine Verbindung mit einem Remotecomputer herstellen, müssen Sie möglicherweise den Dienst (NTLM oder Kerberos) ändern, der die Authentifizierung verarbeitet. Weitere Informationen finden Sie unter [Festlegen des Authentifizierungsdiensts mit VBScript](setting-the-authentication-service-using-vbscript.md).

Für den Zugriff auf einige WMI-Klassen oder -Daten ist möglicherweise eine Berechtigung erforderlich, die nicht aktiviert ist. Beispielsweise müssen Sie beim Herstellen einer Verbindung mit der [**Win32 \_ NTEventlogFile-Klasse**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) die Berechtigung Sicherheit angeben. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge mit VBScript.](executing-privileged-operations-using-vbscript.md)

Wenn Sie auf WMI über eine Active Server Page (ASP) zugreifen, ist eine IIS-Konfiguration erforderlich. Weitere Informationen finden Sie unter [Konfigurieren von IIS 5.0 und höher für WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).

Möglicherweise versuchen Sie, eine Verbindung mit einem Namespace herzustellen, der eine verschlüsselte Verbindung erfordert, d. h. eine Verbindung, die eine Authentifizierungsebene von pktPrivacy erfordert. Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsebene mit VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
