---
description: In den folgenden Abschnitten werden häufige Probleme beschrieben, die Entwickler beim Erstellen einer WMI-Remote Verbindung haben können.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Problembehandlung bei einer Remote-WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345237"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Problembehandlung bei einer Remote-WMI-Verbindung

In den folgenden Abschnitten werden häufige Probleme beschrieben, die Entwickler beim Erstellen einer WMI-Remote Verbindung haben können.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [DCOM-Zugriff verweigert](#dcom-access-denied)
-   [Fehler beim Herstellen der Verbindung](#failure-to-connect)
-   [Timeout bei WMI-Verbindung.](#wmi-connection-timed-out)
-   [Zugehörige Themen](#related-topics)

## <a name="dcom-access-denied"></a>DCOM-Zugriff verweigert

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom
</dt> <dd>

bei der Verbindung ist der Fehler "DCOM-Zugriff verweigert" zusammen mit dem Dezimalwert-2147024891 oder Hex value0x80070005 aufgetreten.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Betrifft
</dt> <dd>

DCOM kann nicht konfiguriert werden, um eine WMI-Verbindung zuzulassen.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Lösungs
</dt> <dd>

Sie können DCOM-Einstellungen für WMI mithilfe des DCOM-Konfigurations Hilfsprogramms (**DCOMCnfg.exe**) konfigurieren, das Sie in der **Systemsteuerung** unter **Verwaltung** finden. Dieses Hilfsprogramm macht die Einstellungen verfügbar, mit denen bestimmte Benutzer eine Remote Verbindung mit dem Computer über DCOM herstellen können. Mitglieder der Gruppe "Administratoren" können standardmäßig eine Remote Verbindung mit dem Computer herstellen. Mit diesem Hilfsprogramm können Sie die Sicherheit festlegen, um den WMI-Dienst zu starten, darauf zuzugreifen und ihn zu konfigurieren.

Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md).

</dd> </dl>

## <a name="failure-to-connect"></a>Fehler beim Herstellen der Verbindung

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom
</dt> <dd>

Es ist nicht möglich, eine Verbindung mit WMI auf einem Remote System herzustellen.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Betrifft
</dt> <dd>

Möglicherweise versuchen Sie, eine Verbindung mit einem System herzustellen, das WMI nicht unterstützt. Die folgenden Verbindungen zwischen Betriebssystemversionen werden nicht unterstützt:

-   Sie können keine Verbindung mit einem Computer herstellen, auf dem eine Starter-, Basic-oder Home-Edition ausgeführt wird.

Alternativ können Sie versuchen, eine Verbindung mit einem Namespace herzustellen, für den eine verschlüsselte Verbindung erforderlich ist, die eine Authentifizierungs Ebene von `pktPrivacy` , **wbemauthenticationlevelpzprivacy** oder **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** erfordert.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Lösungs
</dt> <dd>

Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md), [Sichern von C++-Clients und-Anbietern](securing-c---clients-and-providers.md)oder [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Timeout bei WMI-Verbindung.

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom
</dt> <dd>

Timeout bei der WMI-Verbindung.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Betrifft
</dt> <dd>

Aufgrund von Problemen mit der Netzwerkverzögerung kann der Computer nicht rechtzeitig antworten.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Lösungs
</dt> <dd>

Beim Herstellen einer Verbindung mit WMI durch einen Aufruf von "WS [**. ConnectServer**](swbemlocator-connectserver.md) " oder " [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)" können Sie das Flag " **wbemconnectflagusemaxwait** " (Skripterstellung) oder das **WBEM- \_ Flag " \_ \_ use \_ Max \_ Wait** in C++ Value" auf "128 (0x80)" festlegen, um einen zwei (2) Timeout

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



