---
description: Dieser Leitfaden enthält die Informationen, die Sie benötigen, um Ihrer Microsoft Windows-Anwendung die Verwendung der nächsten Generation von Internetprotokoll, Version 6 (IPv6), zu ermöglichen.
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: IPv6-Leitfaden für Windows Sockets-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c52d86dfcdfa06df80dc71a3f3313de19f9201c7421a3f27f094589a6656dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741114"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>IPv6-Leitfaden für Windows Sockets-Anwendungen

Dieser Leitfaden enthält die Informationen, die Sie benötigen, um Ihrer Microsoft Windows-Anwendung die Verwendung der nächsten Generation von Internetprotokoll, Version 6 (IPv6), zu ermöglichen. Das Hinzufügen von IPv6-Funktionen zu Ihrer Anwendung ist nicht unbedingt ein Portierungsprozess. Zum Portieren einer Anwendung wird empfohlen, Code so zu ändern, dass er auf einer anderen Plattform funktioniert. Dies bedeutet, dass die vorherige Plattform zurückgelassen wird. Dieser Leitfaden ist speziell strukturiert, um einer Anwendung IPv6-Funktionen hinzuzufügen und gleichzeitig die IPv4-Funktionalität beizubehalten.

In diesem Leitfaden werden die Probleme im Zusammenhang mit dem Hinzufügen von IPv6-Funktionen erläutert. Anschließend werden die Entwicklungsbereiche behandelt, die am stärksten von der Umstellung betroffen sind. Jeder Bereich erhält eine umfassende Erläuterung der Fehler, auf die sie achten müssen, die strategien, die empfohlen werden, um sie zu vermeiden, und Tipps, wie neue programmgesteuerte Windows [Sockets 2-Elemente](what-s-new-for-windows-sockets-2.md) (Funktionen und Strukturen) optimal genutzt werden können. Weitere Informationen zu IPv6 finden Sie unter [IPv6-Unterstützung.](ipv6-support-2.md)

Dieser Leitfaden enthält auch Codebeispiele, mit denen Sie praktische Erfahrungen und visuelle Darstellungen der Probleme erhalten, die beim Ändern Ihrer Anwendungen auftreten können. Die Beispiele stammen aus vollständigen, funktionierenden Beispielen einer einfachen Windows Sockets-Anwendung, die geändert wurde, um sowohl IPv4 als auch IPv6 zu unterstützen. Quellcode für diese funktionierenden Beispiele ist vollständig in zwei Anhängen am Ende dieses Dokuments enthalten: [Anhang A: Nur IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md) enthält den Quellcode für eine Anwendung, bevor sie zur Unterstützung von IPv6 geändert wird. [Anhang B: Agnostic Source Code der IP-Version](appendix-b-ip-version-agnostic-source-code-2.md) stellt den Quellcode bereit, nachdem die Anwendung IPv6-fähig wurde.

Microsoft stellt ein Hilfsprogramm namens Checkv4.exe bereit, mit dem Sie potenziell portierenden Code in Ihrem Anwendungscode finden und Empfehlungen für Fehlerbehebungen abgeben können. Das hilfsprogramm Checkv4.exe wird in diesem Dokument veranschaulicht. Dabei wird die in den Anhängen enthaltene Beispielanwendung sowie Screenshots verwendet, die die Ausgabe anzeigen, die das hilfsprogramm Checkv4.exe erzeugt. Weitere Informationen finden Sie unter [Verwenden des hilfsprogramms Checkv4.exe](using-the-checkv4-exe-utility-2.md).

In diesem Leitfaden werden die folgenden Programmierbereiche behandelt:

-   [Ändern von Datenstrukturen für IPv6-Winsock-Appications](changing-data-structures-2.md)
-   [Funktionsaufrufe für IPv6-Winsock-Anwendungen](function-calls-2.md)
-   [Verwenden von hartcodierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
-   [Benutzeroberfläche Probleme bei IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
-   [Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
-   [Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)

Da es keine einheitliche Sequenz von Ereignissen gibt, sind die Abschnitte, die IPv6-aktivierungsprobleme behandeln, nicht sequenziell signifikant angeordnet, sodass Sie jederzeit auf jeden Abschnitt verweisen können. Es wird dringend empfohlen, jeden Abschnitt zu überprüfen, während Sie Ihrer Anwendung IPv6-Funktionen hinzufügen. Es empfiehlt sich auch, sich über das hilfsprogramm Checkv4.exe zu informieren, da es Tipps zur Reihenfolge enthält, in der IPv6-Aktivierungsprobleme behoben werden.

Informationen zum Checkv4.exe Hilfsprogramm und zur Überprüfung der Reihenfolge, in der Sie sich dem Portierungsprozess in Ihren Anwendungen nähern sollten, finden Sie unter [Verwenden des hilfsprogramms für Checkv4.exe](using-the-checkv4-exe-utility-2.md). Dieser Abschnitt enthält Informationen zu einem Kompilierzeitflag, das streng nach Programmierelementen sucht, die mit IPv6 nicht kompatibel sind.

Um direkt zur Beispielanwendung zu wechseln, lesen Sie [Anhang A: Nur IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md) und [Anhang B: Agnostic Source Code der IP-Version.](appendix-b-ip-version-agnostic-source-code-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internetprotokoll Version 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[IPv6-Unterstützung](ipv6-support-2.md)
</dt> <dt>

[IPv6 Technology Preview für Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Verwenden des Checkv4.exe-Hilfsprogramms](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Anhang A: Nur IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Anhang B: Agnostic Source Code der IP-Version](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



