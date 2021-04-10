---
description: Skripts und Visual Basic Anwendungen müssen die DCOM-Sicherheit festlegen, insbesondere für den Remote Zugriff. Außerdem müssen Sie möglicherweise Berechtigungen aktivieren.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Sichern von Skript Clients
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215328"
---
# <a name="securing-scripting-clients"></a>Sichern von Skript Clients

Skripts und Visual Basic Anwendungen müssen die DCOM-Sicherheit festlegen, insbesondere für den Remote Zugriff. Außerdem müssen Sie möglicherweise Berechtigungen aktivieren.

## <a name="default-access-permissions"></a>Standard Zugriffsberechtigungen

Der WMI-Zugriff unterscheidet sich zwischen lokalen Computern und Remote Computern. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

Im folgenden sind die Standard Zugriffsberechtigungen nach Konto aufgeführt:

-   Alle, LocalService, Network Service

    Berechtigung zum Lesen oder Schreiben von Daten und zum Ausführen von [*Anbieter Methoden*](gloss-p.md) auf dem lokalen Computer. Diese Konten können keine neuen Klassen erstellen oder neue Anbieter installieren.

-   Administratorkonten

    Vollzugriff auf dem lokalen Computer. Beim Herstellen einer Verbindung mit einem Remote Computer muss das Konto auch ein lokaler Administrator auf dem Remote Computer sein.

## <a name="securing-a-scripting-client"></a>Sichern eines Skript Clients

WMI-Skripting-und Visual Basic Anwendungen müssen DCOM-Sicherheitsstufen entsprechend für die Betriebssysteme festlegen, auf die Sie abzielen. Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

Beim Herstellen einer Verbindung mit einem Remote Computer müssen Sie möglicherweise den Dienst (NTLM oder Kerberos) ändern, der die Authentifizierung behandelt. Weitere Informationen finden Sie unter [Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript](setting-the-authentication-service-using-vbscript.md).

Der Zugriff auf einige WMI-Klassen oder-Daten erfordert möglicherweise eine Berechtigung, die nicht aktiviert ist. Beispielsweise müssen Sie beim Herstellen einer Verbindung mit der Win32-Klasse [**" \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) " die Sicherheits Berechtigung einschließen. Weitere Informationen finden Sie unter [Ausführen von privilegierten Vorgängen mit VBScript](executing-privileged-operations-using-vbscript.md).

Wenn Sie von einer Active Server Seite (ASP) aus auf WMI zugreifen, ist eine IIS-Konfiguration erforderlich. Weitere Informationen finden Sie unter [Konfigurieren von IIS 5,0 und höher für die WMI-ASP-Skript](configuring-iis-5-for-wmi-asp-scripting.md)Erstellung.

Möglicherweise versuchen Sie, eine Verbindung mit einem Namespace herzustellen, für den eine verschlüsselte Verbindung erforderlich ist, d. h. eine, die eine Authentifizierungs Ebene von PKTPRIVACY erfordert. Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
