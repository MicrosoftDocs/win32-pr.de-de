---
description: Erweiterte Winsock-Beispiele mit Secure Socket-Erweiterungen
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Erweiterte Winsock-Beispiele mit Secure Socket-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ead38a7e62be527e91474ac921803327647ca6cefd1ec68778d03e1c68c1bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412170"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Erweiterte Winsock-Beispiele mit Secure Socket-Erweiterungen

## <a name="secure-tcp-client-and-server-sample"></a>Beispiel für sicheren TCP-Client und -Server

Ein erweitertes Winsock-Beispiel, das die Verwendung sicherer Socketerweiterungen veranschaulicht, ist im Microsoft Windows Software Development Kit (SDK) enthalten. Das Beispiel enthält einen TCP-Client und -Server, die über Winsock und die Secure Socket-Erweiterungen eine sichere Verbindung herstellen.

Standardmäßig wird der Winsock-Beispielquellcode im folgenden Verzeichnis installiert:

*C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v6.0 \\ Samples \\ NetDs \\ winsock*

Ein Beispiel befindet sich im folgenden Ordner:

*securesocket*

Der Beispielcode wird wie unten beschrieben in separate Verzeichnisse unterteilt:

-   stcpclient: Der Ordner, der den sicheren TCP-Clientcode enthält.
-   stcpcommon: Der Ordner, der allgemeinen Bibliothekscode enthält, der vom sicheren TCP-Client und -Server gemeinsam genutzt wird.
-   stcpserver: Der Ordner, der den sicheren TCP-Servercode enthält.

Beachten Sie, dass die Beispiele auf zwei verschiedenen Computern mit Windows Vista oder höher ausgeführt werden sollen. Darüber hinaus müssen IPsec-Anmeldeinformationen auf beiden Computern bereitgestellt werden, damit die Verbindung erfolgreich hergestellt werden kann, da im Beispiel IPsec zum Sichern des Datenverkehrs verwendet wird. Weitere Informationen zum Einrichten von IPsec-Anmeldeinformationen finden Sie in der Dokumentation zur [IPsec-Konfiguration.](/windows/desktop/FWP/ipsec-configuration)

Beim Erstellen des Beispiels werden zwei ausführbare Dateien generiert:

*stcpclient.exe* und *stcpserver.exe*.

Kopieren Sie *stcpclient.exe* auf Computer A, und kopieren Sie *stcpserver.exe* auf Computer B. Starten Sie auf Computer B den TCP-Server, indem Sie an einer Eingabeaufforderung Folgendes ausführen:

**stcpserver.exe**

Führen Sie den folgenden Befehl aus, um weitere Verwendungsoptionen für den Server zu verwenden:

**stcpserver.exe /?**

Starten Sie dann auf Computer A den TCP-Client, indem Sie an einer Eingabeaufforderung Folgendes ausführen:

**stcpclient.exe <vollqualifizierte DNS-Name-für-Computer-B->**

An diesem Punkt sollte die Verbindung sicher hergestellt werden.

Führen Sie den folgenden Befehl aus, um weitere Verwendungsoptionen für den Client zu nutzen:

**stcpclient.exe /?**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Filterplattform](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Anwendungsschichterzwingung (Application Layer Enforcement, ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[IPsec-Konfiguration](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[IPsec-Funktionen](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Verwenden von Secure Socket-Erweiterungen](using-secure-socket-extensions.md)
</dt> <dt>

[Security Support Provider Interface (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Windows-Filterplattform](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Windows Filtern von Plattform-API-Funktionen](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Winsock Secure Socket-Erweiterungen](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
