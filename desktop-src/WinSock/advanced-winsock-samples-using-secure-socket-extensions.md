---
description: Erweiterte Winsock-Beispiele mit Secure Socket Extensions
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Erweiterte Winsock-Beispiele mit Secure Socket Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958931"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Erweiterte Winsock-Beispiele mit Secure Socket Extensions

## <a name="secure-tcp-client-and-server-sample"></a>Beispiel für sicheres TCP-Client und-Server

Im Microsoft Windows Software Development Kit (SDK) finden Sie ein erweitertes Winsock-Beispiel, das die Verwendung von Secure Socket Extensions veranschaulicht. Das Beispiel enthält einen TCP-Client und-Server, die sicher mithilfe der Winsock-und Secure Socket-Erweiterungen eine Verbindung herstellen.

Der Winsock-Beispiel Quellcode wird standardmäßig im folgenden Verzeichnis installiert:

*C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 6.0 \\ Beispiele \\ netds \\ Winsock*

Ein Beispiel befindet sich im folgenden Ordner:

*Securesocket*

Der Beispielcode ist wie unten beschrieben in separate Verzeichnisse unterteilt:

-   stcpclient: der Ordner, der den sicheren TCP-Client Code enthält.
-   stcpcommon: der Ordner, der allgemeinen Bibliotheks Code enthält, der vom sicheren TCP-Client und-Server gemeinsam genutzt wird.
-   stcpserver: der Ordner, der den sicheren TCP-Servercode enthält.

Beachten Sie, dass die Beispiele auf zwei verschiedenen Computern mit Windows Vista oder höher ausgeführt werden sollen. Zusätzlich müssen die IPSec-Anmelde Informationen auf beiden Computern bereitgestellt werden, damit die Verbindung erfolgreich hergestellt werden kann, da im Beispiel IPSec zum Sichern des Datenverkehrs verwendet wird. Weitere Informationen zum Einrichten von IPSec-Anmelde Informationen finden Sie in der Dokumentation zur [IPSec-Konfiguration](/windows/desktop/FWP/ipsec-configuration) .

Beim Erstellen des Beispiels werden zwei ausführbare Dateien generiert:

*stcpclient.exe* und *stcpserver.exe*.

Kopieren Sie *stcpclient.exe* auf Computer a, und kopieren Sie *stcpserver.exe* auf Computer B. Starten Sie auf Computer B den TCP-Server, indem Sie den folgenden Befehl an einer Eingabeaufforderung ausführen:

**stcpserver.exe**

Führen Sie den folgenden Befehl aus, um weitere Verwendungs Optionen für den Server zu verwenden:

**stcpserver.exe/?**

Starten Sie dann auf Computer A den TCP-Client, indem Sie den folgenden Befehl an einer Eingabeaufforderung ausführen:

**stcpclient.exe <voll qualifizierter DNS-Name-for-Machine-B->**

An diesem Punkt sollte die Verbindung sicher hergestellt werden.

Führen Sie den folgenden Befehl aus, um weitere Verwendungs Optionen für den-Client zu verwenden:

**stcpclient.exe/?**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Windows-Filter Plattform](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Durchsetzung der Anwendungsschicht (ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[IPSec-Konfiguration](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[IPSec-Funktionen](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Verwenden von Secure Socket Extensions](using-secure-socket-extensions.md)
</dt> <dt>

[Security Support Provider Interface (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Windows-Filterplattform](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[API-Funktionen der Windows-Filter Plattform](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Winsock Secure Socket Extensions](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
