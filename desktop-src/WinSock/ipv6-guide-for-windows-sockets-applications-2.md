---
description: Dieses Handbuch enthält die Informationen, die Sie benötigen, um Ihre Microsoft Windows-Anwendung für die Verwendung der nächsten Generation von Internet Protocol, Version 6 (IPv6), zu aktivieren.
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: IPv6-Handbuch für Windows Sockets-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129169"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>IPv6-Handbuch für Windows Sockets-Anwendungen

Dieses Handbuch enthält die Informationen, die Sie benötigen, um Ihre Microsoft Windows-Anwendung für die Verwendung der nächsten Generation von Internet Protocol, Version 6 (IPv6), zu aktivieren. Das Hinzufügen von IPv6-Funktionen zu Ihrer Anwendung ist nicht notwendigerweise ein Portierungs Prozess. Um eine Anwendung zu portieren, empfiehlt es sich, Code so zu ändern, dass er auf einer anderen Plattform funktioniert Dieses Handbuch ist speziell so strukturiert, dass einer Anwendung IPv6-Funktionen hinzugefügt werden können, während IPv4-Funktionen beibehalten werden.

In diesem Leitfaden werden die Probleme im Zusammenhang mit dem Hinzufügen von IPv6-Funktionen erläutert. Anschließend werden die Entwicklungsbereiche als Ziel des Übergangs behandelt. Jeder Bereich erhält eine ausführliche Erläuterung der zu überwachenden Fehler, der Strategien, die zur Vermeidung von Problemen vorgeschlagen werden, und Tipps, wie Sie neue programmgesteuerte Elemente von [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (Funktionen und Strukturen) optimal nutzen können. Weitere Informationen zu IPv6 finden Sie [unter IPv6-Unterstützung](ipv6-support-2.md).

Dieses Handbuch enthält auch Codebeispiele, mit denen Sie praktische Erfahrungen und visuelle Darstellungen der Probleme erhalten können, die beim Ändern Ihrer Anwendungen auftreten können. Die Beispiele stammen aus den umfassenden, funktionierenden Beispielen einer einfachen Windows Sockets-Anwendung, die zur Unterstützung von IPv4 und IPv6 geändert wurde. Der Quellcode für diese funktionierenden Beispiele ist vollständig in zwei Anhänge am Ende dieses Dokuments enthalten: [Anhang A: nur-IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md) enthält den Quellcode für eine Anwendung, bevor Sie zur Unterstützung von IPv6 geändert wird. [Anhang B:](appendix-b-ip-version-agnostic-source-code-2.md) der Quellcode für die unabhängige IP-Version stellt den Quellcode bereit, nachdem die Anwendung IPv6-aktiviert ist.

Microsoft stellt ein Dienstprogramm namens Checkv4.exe bereit, mit dessen Hilfe Sie potenziell Portierungs relevanten Code in Ihrem Anwendungscode finden und auch Empfehlungen für Korrekturen erhalten. Das Checkv4.exe-Hilfsprogramm wird in diesem Dokument mit der Beispielanwendung, die in den Appendixes enthalten ist, zusammen mit Bildschirmfotos veranschaulicht, die die Ausgabe des Checkv4.exe Hilfsprogramms anzeigen. Weitere Informationen finden Sie unter [Verwenden des Checkv4.exe Hilfsprogramms](using-the-checkv4-exe-utility-2.md).

Die in diesem Handbuch behandelten Programmier Bereiche lauten wie folgt:

-   [Ändern von Datenstrukturen für IPv6-Winsock-Appications](changing-data-structures-2.md)
-   [Funktionsaufrufe für IPv6-Winsock-Anwendungen](function-calls-2.md)
-   [Verwendung von hart codierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
-   [Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
-   [Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
-   [Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)

Da es keine einheitliche Abfolge von Ereignissen gibt, werden die Abschnitte, die Probleme mit der IPv6-Aktivierung behandeln, nicht nacheinander angeordnet, sodass Sie jederzeit auf jeden Abschnitt verweisen können. Es wird dringend empfohlen, jeden Abschnitt zu überprüfen, während Sie der Anwendung IPv6-Funktionen hinzufügen. Außerdem empfiehlt es sich, über das Checkv4.exe-Hilfsprogramm zu lesen, da es Tipps zur Reihenfolge enthält, in der Probleme mit der IPv6-Aktivierung behandelt werden.

Weitere Informationen zum Checkv4.exe-Hilfsprogramm und zum Überprüfen der Reihenfolge, in der Sie den Portierungs Prozess in Ihren Anwendungen verwenden sollten, finden Sie unter [Verwenden des Checkv4.exe Hilfsprogramms](using-the-checkv4-exe-utility-2.md). Dieser Abschnitt enthält Informationen zu einem Kompilierzeit Kennzeichen, das strikt auf Programmierungs Elemente überprüft, die mit IPv6 nicht kompatibel sind.

Um direkt zur Beispielanwendung zu wechseln, finden Sie weitere Informationen unter [Anhang A: nur-IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md) und [Anhang B: Quell Code, der der IP-Version agnostisch](appendix-b-ip-version-agnostic-source-code-2.md)ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internet Protokoll Version 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[IPv6-Unterstützung](ipv6-support-2.md)
</dt> <dt>

[IPv6-Technologievorschau für Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Verwenden des Checkv4.exe Hilfsprogramms](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Anhang A: nur-IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Anhang B: Quell Code für die unabhängige IP-Version](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



