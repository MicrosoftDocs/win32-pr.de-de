---
description: Die Langlebigkeit von IPv4 führte dazu, dass viele bekannte IPv4-Adressen hart codiert werden, wie z. b. Loopback Adressen (127. x. x. x), ganzzahlige Konstanten wie z. b. inaddr \_ Loopback.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Verwendung von hart codierten IPv4-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343458"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Verwendung von hart codierten IPv4-Adressen

Die Langlebigkeit von IPv4 führte dazu, dass viele bekannte IPv4-Adressen hart codiert werden, wie z. b. Loopback Adressen (127. x. x. x), ganzzahlige Konstanten wie z. b. inaddr \_ Loopback. Die Praxis der hart Codierung dieser Adressen stellt offensichtliche Probleme dar, wenn und vorhandene Anwendungen geändert werden, um IPv6 zu unterstützen oder neue, von der Version unabhängige Programme zu erstellen.

Bewährte Methode

-   Der beste Ansatz besteht darin, die hart Codierung von Adressen zu vermeiden.

Zu Vermeider Code

-   Vermeiden Sie die Verwendung von hart codierten Adressen im Code.

**So ändern Sie die vorhandene Codebasis von IPv4 zu IPv4-und IPv6-Interoperabilität**

1.  Erwerben Sie das *Checkv4.exe* -Hilfsprogramm. Das *Checkv4.exe* -Hilfsprogramm wird als Teil des Microsoft Windows Software Development Kit (SDK) installiert, das für Windows Vista und höher veröffentlicht wurde. Der Windows SDK ist über ein MSDN-Abonnement verfügbar und kann auch von der Microsoft-Website heruntergeladen werden ( https://msdn.microsoft.com) .
2.  Führen Sie das *Checkv4.exe* -Hilfsprogramm für den Code aus. Erfahren Sie, wie Sie das *Checkv4.exe* -Hilfsprogramm für Ihre Dateien ausführen, [indem Sie das Checkv4.exe-Hilfsprogramm verwenden](using-the-checkv4-exe-utility-2.md).
3.  Das *Checkv4.exe* -Hilfsprogramm warnt Sie bei der Anwesenheit allgemeiner Definitionen für IPv4-Adressen, z. b. inaddr- \_ Loopback. Ändern Sie den Code, der Literalzeichenfolgen verwendet, mit Code, der Protokoll Versions agnostisch ist.
4.  Durchsuchen Sie die Codebasis nach anderen möglichen Literalzeichenfolgen.

Mit dem *Checkv4.exe* -Hilfsprogramm können Sie allgemeine Literalzeichenfolgen finden, aber es gibt möglicherweise andere, die für Ihre Anwendung spezifisch sind. Sie sollten eine gründliche Suche und Tests durchführen, um sicherzustellen, dass die Codebasis mögliche Probleme mit Literalzeichenfolgen beseitigt hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6-Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Funktionsaufrufe für IPv6-Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 



