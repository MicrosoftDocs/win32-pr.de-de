---
title: Kernelmodusssl
description: Kernelmodusssl
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- Kernelmodusssl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340452"
---
# <a name="kernel-mode-ssl"></a>Kernelmodusssl

Der kernelmodusssl wurde in Windows Server 2003 mit Service Pack 1 (SP1) mit eingeschränkter Unterstützung eingeführt. Für Computer, die unter Windows Server 2003 mit SP1 ausgeführt werden, muss ein Registrierungsschlüssel festgelegt werden, um Kernel-SSL zu aktivieren. Für Computer, die unter Windows Server 2008 und Windows Vista ausgeführt werden, wird eine vollständige Kernel Modus-Unterstützung für SSL bereitgestellt.

In den folgenden Abschnitten wird die SSL-Unterstützung im Kernel Modus beschrieben

-   Kernelmodusssl in Windows Server 2003 mit SP1
-   Kernelmodusssl in Windows Server 2008 und Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Kernelmodusssl in Windows Server 2003 mit SP1

In Windows Server 2003 mit SP1 bietet die HTTP-Server-API die Option zum Ausführen der SSL-Sicherheit im Kernel Modus (Benutzermodus SSL ist die Standardeinstellung). Die kernelmodusfunktion verbessert die SSL-Leistung durch Verschieben von Verschlüsselungs-und Entschlüsselungs Vorgängen in den Kernel, wodurch die Anzahl der Übergänge zwischen Kernel Modus und Benutzermodus verringert wird.

Die folgenden Funktionen werden nicht unterstützt, wenn SSL im Kernel Modus ausgeführt wird:

-   Clientzertifikate
-   RC2-Chiffren
-   Das PCT 1,0-Protokoll
-   Änderungen der Server Zertifikat Konfiguration erfordern einen Neustart des HTTP-Dienstanbieter
-   Unterstützung für die Massen Verschlüsselung und-Auslagerung

## <a name="configuring-kernel-mode-ssl"></a>Konfigurieren des Kernel Modus-SSL

Der kernelmodusssl wird durch den Registrierungs Wert **EnableKernelSSL** gesteuert und aktiviert, indem der Wert auf 1 festgelegt wird. Wenn Sie den kernelmodusssl aktivieren, wird SSL im Benutzermodus deaktiviert, und der HTTP-Dienst muss neu gestartet werden. Der Registrierungsschlüssel " **EnableKernelSSL** " befindet sich unter:

**HKEY \_ LOCAL \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **http** \\ **Parameters** \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>Kernelmodusssl in Windows Server 2008 und Windows Vista

Für Computer, die unter Windows Server 2008 und Windows Vista ausgeführt werden, bietet die HTTP-Server-API erweiterte SSL-Funktionalität.

Die folgenden neuen Features werden unterstützt:

-   Vollständige Client Zertifikat Unterstützung im Kernel Modus-SSL
-   Kernelmodusssl für alle HTTP-SSL-Transaktionen
-   Unterstützung für die Massen Verschlüsselung und-Auslagerung
-   Das PCT 1,0-Protokoll
-   RC2-Chiffren
-   Bessere Leistung im Benutzermodus (SSL)

## <a name="configuration"></a>Konfiguration

Der kernelmodusssl kann durch zwei Registrierungs Werte unter dem Schlüssel "http-Parameter" konfiguriert werden:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

Ein Benutzer muss über Administrator-/lokale System Berechtigungen verfügen, um die Registrierungs Werte zu ändern und die Protokolldateien und den Ordner zu ändern, in dem Sie enthalten sind.

Konfigurationsinformationen in den Registrierungs Werten werden gelesen, wenn der HTTP-Server-API-Treiber gestartet wird. Wenn die Einstellungen geändert werden, muss der Treiber daher beendet und neu gestartet werden, um die neuen Werte zu lesen. Dies kann mithilfe der folgenden Konsolenbefehle erreicht werden:

**NET stopphttp**

**NET Start http**

In der folgenden Tabelle sind die Registrierungs Konfigurationswerte aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Registrierungs Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 und Windows Vista:</strong> Dieser Registrierungs Wert ist veraltet.<br/></td>
</tr>
<tr class="even">
<td>Enablesslclosenotify</td>
<td>Ein <strong>DWORD</strong> -Wert, der auf <strong>true</strong> festgelegt ist, um close-notify zu aktivieren, oder <strong>false</strong> , um die Anforderung für die schließende Benachrichtigung zu deaktivieren. Close-Notify ist standardmäßig deaktiviert.<br/> Wenn Close-notify aktiviert ist, muss die Client Anwendung vor dem Schließen von TCP-Verbindungen eine Nachricht mit dem Schluss benachrichtigen senden. Die HTTP-Server-API sendet vor dem Schließen der Verbindung auch eine schließende Benachrichtigung.<br/> Wenn Close-notify aktiviert ist und der Client eine Nachricht mit der Meldung "Close-notify" sendet, wird die SSL-Sitzung von der HTTP-Server-API bei zukünftigen Verbindungen mit dem Client wieder verwendet. Wenn der Client keine close-notify-Benachrichtigung sendet, wird die gleiche SSL-Sitzung von der HTTP-Server-API bei zukünftigen Verbindungen nicht wieder verwendet. Daher wird ein vollständiger SSL-Handshake für die neue Verbindung ausgelöst, wodurch die Leistung reduziert wird. <br/>
<blockquote>
[!Note]<br />
Durch das Aktivieren von Close-notify werden abschneidender Angriffe gegen die HTTPS-Anforderungen und-Antworten minimiert.
</blockquote>
<br/> <br/> Wenn Close-notify deaktiviert ist, wird die SSL-Sitzung von der HTTP-Server-API für zukünftige Verbindungen erneut verwendet.<br/></td>
</tr>
<tr class="odd">
<td>Disablesslcertchaincacheonlyurlretrieval</td>
<td>Ein <strong>DWORD</strong> -Wert, der auf " <strong>true</strong> " festgelegt ist, damit die HTTP-Server-API zwischen Zertifikate aus dem Internet oder dem lokalen Speicher abrufen kann, oder " <strong>false</strong> ", um nur zwischen Zertifikate aus dem lokalen Speicher abzurufen. Der Standard Registrierungs Wert ist <strong>false</strong>.<br/> Standardmäßig erstellt die HTTP-Server-API eine Client Zertifikat Kette, indem die zwischen Zertifikate aus dem zwischen Zertifizierungsstellen-Speicher unter dem lokalen Computer Konto abgerufen werden. Wenn dieser Wert auf <strong>true</strong> festgelegt wird, kann die HTTP-Server-API die zwischen Zertifikate nicht nur aus dem lokalen Speicher abrufen, sondern auch von der zwischen Zertifizierungsstelle im Internet.<br/></td>
</tr>
</tbody>
</table>



 

 

 





