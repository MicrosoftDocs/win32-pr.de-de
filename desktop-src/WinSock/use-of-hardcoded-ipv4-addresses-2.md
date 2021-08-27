---
description: Die Länge von IPv4 führte zu harter Codierung vieler bekannter IPv4-Adressen, z. B. Loopbackadressen (127.x.x.x) und ganzzahligen Konstanten wie INADDR \_ LOOPBACK.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Verwenden von hartcodierten IPv4-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0506f200776402464c4b2904435157c435ece7fc2c6d9e0b10bfd1c1d66491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121200"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Verwenden von hartcodierten IPv4-Adressen

Die Länge von IPv4 führte zu harter Codierung vieler bekannter IPv4-Adressen, z. B. Loopbackadressen (127.x.x.x) und ganzzahligen Konstanten wie INADDR \_ LOOPBACK. Die Praxis, diese Adressen hart zu codieren, stellt offensichtliche Probleme bei der Änderung und vorhandenen Anwendung zur Unterstützung von IPv6 oder beim Erstellen neuer, versionsunabhängiger IP-Programme vor.

Bewährte Methode

-   Der beste Ansatz besteht in der Vermeidung der Hartcodierung von Adressen.

Code, der vermieden werden soll

-   Vermeiden Sie die Verwendung von hartcodierten Adressen im Code.

**So ändern Sie Ihre vorhandene Codebasis von IPv4 in IPv4- und IPv6-Interoperabilität**

1.  Erwerben Sie *dasCheckv4.exe* Hilfsprogramm. Das Checkv4.exe-Hilfsprogramm wird als Teil des Microsoft Windows Software Development Kit (SDK) installiert, das für Windows Vista und höher veröffentlicht wurde. Das Windows SDK ist über ein MSDN-Abonnement verfügbar und kann auch von der Microsoft-Website () heruntergeladen https://msdn.microsoft.com) werden.
2.  Führen Sie *Checkv4.exe* Hilfsprogramm für Ihren Code aus. Informationen zum Ausführen des Hilfsprogramms *Checkv4.exe* -Hilfsprogramms für Ihre Dateien finden Sie im Abschnitt Verwenden des Checkv4.exe [Hilfsprogramms](using-the-checkv4-exe-utility-2.md).
3.  Das Checkv4.exe-Hilfsprogramm warnt Sie, wenn allgemeine Definitionen für IPv4-Adressen vorliegen, z. B. INADDR \_ LOOPBACK. Ändern Sie beliebigen Code, der Literalzeichenfolgen mit protokollversionsunabhängigem Code verwendet.
4.  Suchen Sie in Ihrer Codebasis nach anderen potenziellen Literalzeichenfolgen.

Das *Checkv4.exe* hilfsprogramm kann Ihnen helfen, allgemeine Literalzeichenfolgen zu finden, aber es gibt möglicherweise andere, die für Ihre Anwendung spezifisch sind. Sie sollten gründlich suchen und testen, um sicherzustellen, dass Ihre Codebasis potenzielle Probleme im Zusammenhang mit Literalzeichenfolgen hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Leitfaden für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6 Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Funktionsaufrufe für IPv6 Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Benutzeroberfläche von IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6 Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 



