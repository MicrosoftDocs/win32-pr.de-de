---
title: Kernelmodus-SSL
description: Kernelmodus-SSL
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- Kernelmodus-SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfbc66e72f4e3e79c53207cbe9f4b77d3887b36
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475496"
---
# <a name="kernel-mode-ssl"></a>Kernelmodus-SSL

Ssl im Kernelmodus wurde in Windows Server 2003 mit Service Pack 1 (SP1) mit eingeschränkter Unterstützung eingeführt. Für Computer, die auf Windows Server 2003 mit SP1 ausgeführt werden, muss ein Registrierungsschlüssel festgelegt werden, um Kernel-SSL zu aktivieren. Für Computer, die auf Windows Server 2008 und Windows Vista ausgeführt werden, wird vollständige Kernelmodusunterstützung für SSL bereitgestellt.

In den folgenden Abschnitten wird die SSL-Unterstützung im Kernelmodus beschrieben:

-   Kernelmodi SSL in Windows Server 2003 mit SP1
-   Kernelmodus-SSL in Windows Server 2008 und Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Kernelmodi SSL in Windows Server 2003 mit SP1

In Windows Server 2003 mit SP1 bietet die HTTP-Server-API die Option zum Ausführen der SSL-Sicherheit im Kernelmodus (Benutzermodus SSL ist die Standardeinstellung). Das Kernelmodusfeature verbessert die SSL-Leistung, indem Verschlüsselungs- und Entschlüsselungsvorgänge auf den Kernel übertragen werden, wodurch die Anzahl der Übergänge zwischen Kernelmodus und Benutzermodus reduziert wird.

Die folgenden Features werden nicht unterstützt, wenn SSL im Kernelmodus ausgeführt wird:

-   Clientzertifikate
-   RC2-Verschlüsselungen
-   Das PCT 1.0-Protokoll
-   Änderungen an der Serverzertifikatkonfiguration erfordern einen Neustart des HTTP-Diensts.
-   Unterstützung für Massenverschlüsselung und -ausladung

## <a name="configuring-kernel-mode-ssl"></a>Konfigurieren von SSL im Kernelmodus

SSL im Kernelmodus wird durch den **Registrierungswert EnableKernelSSL** gesteuert und durch Festlegen des Werts auf 1 aktiviert. Wenn Sie SSL im Kernelmodus aktivieren, wird SSL im Benutzermodus deaktiviert, und der HTTP-Dienst muss neu gestartet werden, damit er wirksam wird. Der **Registrierungsschlüssel EnableKernelSSL** befindet sich unter:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **HTTP** \\ **Parameters** \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>Kernelmodus-SSL in Windows Server 2008 und Windows Vista

Für Computer, die auf Windows Server 2008 und Windows Vista ausgeführt werden, verfügt die HTTP-Server-API über erweiterte SSL-Funktionen.

Die folgenden neuen Features werden unterstützt:

-   Vollständige Clientzertifikatunterstützung im Kernelmodus SSL
-   Ssl im Kernelmodus für alle HTTP-SSL-Transaktionen
-   Unterstützung für Massenverschlüsselung und -ausladung
-   Das PCT 1.0-Protokoll
-   RC2-Verschlüsselungen
-   Höhere Leistung gegenüber SSL im Benutzermodus

## <a name="configuration"></a>Konfiguration

SSL im Kernelmodus kann über zwei Registrierungswerte unter dem SCHLÜSSEL HTTP-Parameter unter konfiguriert werden:

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

Ein Benutzer muss über Administrator-/lokale Systemberechtigungen verfügen, um die Registrierungswerte zu ändern und die Protokolldateien und den Ordner, in dem sie enthalten sind, anzeigen oder ändern zu können.

Konfigurationsinformationen in den Registrierungswerten werden gelesen, wenn der HTTP Server-API-Treiber gestartet wird. Wenn die Einstellungen geändert werden, muss der Treiber daher beendet und neu gestartet werden, um die neuen Werte zu lesen. Dies kann mithilfe der folgenden Konsolenbefehle erreicht werden:

**net stop http**

**net start http**

In der folgenden Tabelle sind die Registrierungskonfigurationswerte aufgeführt.




| Registrierungswert | BESCHREIBUNG | 
|----------------|-------------|
| EnableKernelSSL | <strong>Windows Server 2008 und Windows Vista:</strong> Dieser Registrierungswert ist veraltet.<br /> | 
| EnableSslCloseNotify | Ein <strong>DWORD-Wert,</strong> der auf <strong>TRUE</strong> festgelegt ist, um close-notify zu aktivieren, oder <strong>FALSE,</strong> um die Anforderung zum Schließen der Benachrichtigung zu deaktivieren. Close-Notify ist standardmäßig deaktiviert.<br /> Wenn close-notify aktiviert ist, muss die Clientanwendung vor dem Schließen von TCP-Verbindungen eine Benachrichtigung zum Schließen senden. Die HTTP-Server-API sendet auch eine Benachrichtigung zum Schließen, bevor die Verbindung geschlossen wird.<br /> Wenn close-notify aktiviert ist und der Client eine Benachrichtigung zum Schließen sendet, verwendet die HTTP-Server-API die SSL-Sitzung bei zukünftigen Verbindungen mit dem Client erneut. Wenn der Client keine Benachrichtigung zum Schließen sendet, verwendet die HTTP-Server-API bei zukünftigen Verbindungen nicht dieselbe SSL-Sitzung. Daher wird ein vollständiger SSL-Handshake für die neue Verbindung ausgelöst, wodurch die Leistung verringert wird. <br /><blockquote>[!Note]<br />Die Aktivierung von "Close-Notify" trägt dazu bei, Kürzungsangriffe auf HTTPS-Anforderungen und -Antworten zu minimieren.</blockquote><br /><br /> Wenn close-notify deaktiviert ist, verwendet die HTTP-Server-API die SSL-Sitzung für zukünftige Verbindungen erneut.<br /> | 
| DisableSslCertChainCacheOnlyUrlRetrieval | Ein <strong>DWORD-Wert,</strong> der auf <strong>TRUE</strong> festgelegt ist, um der HTTP-Server-API das Abrufen von Zwischenzertifikaten aus dem Internet oder dem lokalen Speicher zu ermöglichen, oder <strong>FALSE,</strong> um Nur Zwischenzertifikate aus dem lokalen Speicher abzurufen. Der Standardregistrierungswert ist <strong>FALSE.</strong><br /> Standardmäßig erstellt die HTTP-Server-API eine Clientzertifikatkette, indem sie die Zwischenzertifikate aus dem Zwischenzertifikatsspeicher unter dem Konto des lokalen Computers abruft. Wenn Sie diesen Wert auf <strong>TRUE</strong> festlegen, kann die HTTP-Server-API die Zwischenzertifikate nicht nur aus dem lokalen Speicher, sondern auch von der Zwischenzertifikatsstelle im Internet abrufen.<br /> | 




 

 

 





