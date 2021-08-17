---
title: Kernelmodus SSL
description: Kernelmodus SSL
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- Kernelmodus SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9dcfeb87b1a98539d7bd6a3b8b82dcfd5ee41fc9ad4c4c306f4c399aebd18a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393918"
---
# <a name="kernel-mode-ssl"></a>Kernelmodus SSL

Der Kernelmodus SSL wurde in Windows Server 2003 mit Service Pack 1 (SP1) mit eingeschränkter Unterstützung eingeführt. Für Computer, die auf Windows Server 2003 mit SP1 ausgeführt werden, muss ein Registrierungsschlüssel festgelegt werden, um Kernel-SSL zu aktivieren. Für Computer, die auf Windows Server 2008 und Windows Vista ausgeführt werden, wird die vollständige Kernelmodusunterstützung für SSL bereitgestellt.

In den folgenden Abschnitten wird die Kernelmodus-SSL-Unterstützung beschrieben:

-   Kernelmodi SSL in Windows Server 2003 mit SP1
-   Kernelmodus-SSL in Windows Server 2008 und Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Kernelmodi SSL in Windows Server 2003 mit SP1

In Windows Server 2003 mit SP1 bietet die HTTP-Server-API die Option zum Ausführen der SSL-Sicherheit im Kernelmodus (Ssl im Benutzermodus ist die Standardeinstellung). Das Kernelmodusfeature verbessert die SSL-Leistung, indem Verschlüsselungs- und Entschlüsselungsvorgänge in den Kernel verschoben werden, wodurch die Anzahl der Übergänge zwischen Kernelmodus und Benutzermodus reduziert wird.

Die folgenden Features werden nicht unterstützt, wenn SSL im Kernelmodus ausgeführt wird:

-   Clientzertifikate
-   RC2-Verschlüsselungen
-   Das PCT 1.0-Protokoll
-   Änderungen der Serverzertifikatkonfiguration erfordern einen Neustart des HTTP-Diensts.
-   Unterstützung für Massenverschlüsselung und Auslagerung

## <a name="configuring-kernel-mode-ssl"></a>Konfigurieren von SSL im Kernelmodus

Kernelmodus-SSL wird durch den **Registrierungswert EnableKernelSSL** gesteuert und durch Festlegen des Werts auf 1 aktiviert. Durch aktivieren des Kernelmodus SSL wird ssl im Benutzermodus deaktiviert, und der HTTP-Dienst muss neu gestartet werden, damit er wirksam wird. Der **Registrierungsschlüssel EnableKernelSSL** befindet sich unter:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **HTTP** \\ **Parameters** \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>Kernelmodus-SSL in Windows Server 2008 und Windows Vista

Für Computer, die auf Windows Server 2008 und Windows Vista ausgeführt werden, bietet die HTTP-Server-API erweiterte SSL-Funktionen.

Die folgenden neuen Features werden unterstützt:

-   Vollständige Clientzertifikatunterstützung im Kernelmodus SSL
-   Kernelmodus-SSL für alle HTTP SSL-Transaktionen
-   Unterstützung für Massenverschlüsselung und Auslagerung
-   Das PCT 1.0-Protokoll
-   RC2-Verschlüsselungen
-   Höhere Leistung gegenüber SSL im Benutzermodus

## <a name="configuration"></a>Konfiguration

Ssl im Kernelmodus kann über zwei Registrierungswerte unter dem HTTP-Parameterschlüssel konfiguriert werden, der sich unter befindet:

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

Ein Benutzer muss über Administrator-/Lokale Systemberechtigungen verfügen, um die Registrierungswerte zu ändern und die Protokolldateien und den Ordner, in dem sie enthalten sind, anzuzeigen oder zu ändern.

Konfigurationsinformationen in den Registrierungswerten werden gelesen, wenn der HTTP Server-API-Treiber gestartet wird. Wenn die Einstellungen geändert werden, muss der Treiber daher angehalten und neu gestartet werden, um die neuen Werte zu lesen. Dies kann mithilfe der folgenden Konsolenbefehle erreicht werden:

**net stop http**

**net start http**

In der folgenden Tabelle sind die Registrierungskonfigurationswerte aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Registrierungswert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 und Windows Vista:</strong> Dieser Registrierungswert ist veraltet.<br/></td>
</tr>
<tr class="even">
<td>EnableSslCloseNotify</td>
<td>Ein <strong>DWORD-Wert,</strong> der auf <strong>TRUE</strong> festgelegt ist, um close-notify zu aktivieren, oder <strong>FALSE,</strong> um die Anforderung zum Schließen von Benachrichtigungen zu deaktivieren. Close-notify ist standardmäßig deaktiviert.<br/> Wenn close-notify aktiviert ist, muss die Clientanwendung vor dem Schließen von TCP-Verbindungen eine Meldung zum Schließen der Benachrichtigung senden. Die HTTP-Server-API sendet auch eine Benachrichtigung zum Schließen, bevor die Verbindung geschlossen wird.<br/> Wenn close-notify aktiviert ist und der Client eine Meldung zum Schließen der Benachrichtigung sendet, verwendet die HTTP-Server-API die SSL-Sitzung bei zukünftigen Verbindungen mit dem Client wieder. Wenn der Client keine Schließen-Benachrichtigung sendet, verwendet die HTTP-Server-API bei zukünftigen Verbindungen nicht dieselbe SSL-Sitzung wieder. Daher wird bei der neuen Verbindung ein vollständiger SSL-Handshake ausgelöst, wodurch die Leistung reduziert wird. <br/>
<blockquote>
[!Note]<br />
Das Aktivieren von "Close-Notify" hilft dabei, Abschneideangriffe auf HTTPS-Anforderungen und -Antworten zu verringern.
</blockquote>
<br/> <br/> Wenn close-notify deaktiviert ist, verwendet die HTTP-Server-API die SSL-Sitzung für zukünftige Verbindungen wieder.<br/></td>
</tr>
<tr class="odd">
<td>DisableSslCertChainCacheOnlyUrlRetrieval</td>
<td>Ein <strong>DWORD-Wert,</strong> der auf <strong>TRUE</strong> festgelegt ist, damit die HTTP-Server-API Zwischenzertifikate entweder aus dem Internet oder dem lokalen Speicher abrufen kann, oder <strong>FALSE,</strong> um nur Zwischenzertifikate aus dem lokalen Speicher abzurufen. Der Standardregistrierungswert ist <strong>FALSE.</strong><br/> Standardmäßig erstellt die HTTP-Server-API eine Clientzertifikatkette, indem die Zwischenzertifikate aus dem Zwischenspeicher der Zertifizierungsstelle unter dem lokalen Computerkonto abgerufen werden. Wenn Sie diesen Wert auf <strong>TRUE</strong> festlegen, kann die HTTP-Server-API die Zwischenzertifikate nicht nur aus dem lokalen Speicher, sondern auch von der Zwischenzertifizierungsstelle im Internet abrufen.<br/></td>
</tr>
</tbody>
</table>



 

 

 





