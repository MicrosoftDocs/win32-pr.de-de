---
description: In den folgenden Abschnitten werden häufige Probleme beschrieben, die Entwickler beim Erstellen einer WMI-Remoteverbindung haben können.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Problembehandlung bei einer WMI-Remoteverbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10603f713fecf861750d70c4166da91e081dc273a0d6d6134ed916a7f84f2bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312416"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Problembehandlung bei einer WMI-Remoteverbindung

In den folgenden Abschnitten werden häufige Probleme beschrieben, die Entwickler beim Erstellen einer WMI-Remoteverbindung haben können.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [DCOM-Zugriff verweigert](#dcom-access-denied)
-   [Fehler beim Verbinden](#failure-to-connect)
-   [Timed out der WMI-Verbindung](#wmi-connection-timed-out)
-   [Zugehörige Themen](#related-topics)

## <a name="dcom-access-denied"></a>DCOM-Zugriff verweigert

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom
</dt> <dd>

Die Verbindung ist mit dem Fehler "DCOM-Zugriff verweigert" zusammen mit dem Dezimalwert -2147024891 oder hexadezimalen Wert0x80070005 fehlgeschlagen.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problem
</dt> <dd>

DCOM ist möglicherweise nicht so konfiguriert, dass eine WMI-Verbindung zulässig ist.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Auflösung
</dt> <dd>

Sie können DCOM-Einstellungen für WMI mithilfe des DCOM-Konfigurationsprogramms (**DCOMCnfg.exe**) konfigurieren, das sich unter **Verwaltung** **in** Systemsteuerung. Dieses Hilfsprogramm macht die Einstellungen verfügbar, die es bestimmten Benutzern ermöglichen, eine Remoteverbindung mit dem Computer über DCOM herzustellen. Mitglieder der Gruppe Administratoren dürfen standardmäßig eine Remoteverbindung mit dem Computer herstellen. Mit diesem Hilfsprogramm können Sie die Sicherheit so festlegen, dass der WMI-Dienst gestartet, darauf zugreifen und konfiguriert wird.

Weitere Informationen finden Sie unter [Sichern einer WMI-Remoteverbindung.](securing-a-remote-wmi-connection.md)

</dd> </dl>

## <a name="failure-to-connect"></a>Fehler beim Verbinden

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom
</dt> <dd>

Sie können keine Verbindung mit WMI auf einem Remotesystem herstellen.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problem
</dt> <dd>

Möglicherweise versuchen Sie, eine Verbindung mit einem System herzustellen, das WMI nicht unterstützt. Die folgenden Verbindungen zwischen Betriebssystemversionen werden nicht unterstützt:

-   Sie können keine Verbindung mit einem Computer herstellen, auf dem eine Starter-, Basic- oder Home-Edition ausgeführt wird.

Alternativ können Sie versuchen, eine Verbindung mit einem Namespace herzustellen, der eine verschlüsselte Verbindung erfordert, die die Authentifizierungsebene `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** oder **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT PRIVACY \_ erfordert.**

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Auflösung
</dt> <dd>

Weitere Informationen finden Sie unter [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), oder [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Timed out der WMI-Verbindung

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom
</dt> <dd>

Bei der WMI-Verbindung wird ein Zeitsendzeit her.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problem
</dt> <dd>

Aufgrund von Netzwerkverzögerungsproblemen kann der Computer einfach nicht zeitbedingt reagieren.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Auflösung
</dt> <dd>

Wenn Sie eine Verbindung mit WMI über einen Aufruf von [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) oder [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)herstellen, können Sie das **wbemConnectFlagUseMaxWait-Flag** (Skripterstellung) oder den **WBEM-FLAG \_ CONNECT USE MAX \_ \_ \_ \_ WAIT** in C++-Wert auf 128 (0x80) festlegen, um ein Time out von zwei (2) Minuten für den Aufruf zu erzwingen.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



