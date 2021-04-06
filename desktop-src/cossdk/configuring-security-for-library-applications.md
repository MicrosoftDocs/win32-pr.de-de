---
description: Bei der Konfiguration der rollenbasierten Sicherheit und Authentifizierung für Bibliotheksanwendungen müssen besondere Aspekte berücksichtigt werden.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Konfigurieren der Sicherheit für Bibliotheksanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102d6a0f102bfd19da0073bca14df8a8211203b1
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "103961056"
---
# <a name="configuring-security-for-library-applications"></a>Konfigurieren der Sicherheit für Bibliotheksanwendungen

Bei der Konfiguration der rollenbasierten Sicherheit und Authentifizierung für Bibliotheksanwendungen müssen besondere Aspekte berücksichtigt werden.

## <a name="enabling-or-disabling-authentication"></a>Aktivieren oder Deaktivieren der Authentifizierung

Einer der Faktoren, die berücksichtigt werden sollten, ist, ob Aufrufer der Bibliotheks Anwendung die Sicherheitsüberprüfungen für den Host Prozess auf Prozessebene unterliegen sollen, d. –. ob die Authentifizierung aktiviert oder deaktiviert werden soll.

Wenn die Bibliotheks Anwendung beispielsweise von einem Browser gehostet wird, muss Sie möglicherweise nicht authentifizierte Rückrufe empfangen. Um diese Anforderung zu erfüllen, können Sie die Authentifizierung deaktivieren, sodass der Hostingprozess keine Sicherheitsüberprüfungen für Aufrufer der Bibliotheks Anwendung ausführt. Wenn Sie die Authentifizierung deaktivieren, wird die Bibliotheks Anwendung effektiv nicht authentifiziert – alle Aufrufe an diese werden erfolgreich ausgeführt. Aufrufer der Bibliotheks Anwendung unterliegen nicht den Sicherheitsüberprüfungen des Hostingprozesses. Im Grunde wird die Bibliotheks Anwendung als "nicht authentifiziert" gekennzeichnet, und Sicherheitsüberprüfungen werden bei Aufrufen der Bibliotheks Anwendung ausgelassen.

Informationen zum Aktivieren oder Deaktivieren der Authentifizierung finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md).

## <a name="enforcing-role-checks"></a>Erzwingen von Rollen Überprüfungen

Eine weitere Entscheidung besteht darin, ob die Bibliotheks Anwendung [rollenbasierte Sicherheit](role-based-security-administration.md)verwenden soll. Wenn rollenbasierte Sicherheit verwendet wird, müssen Sie für alle Zugriffs Überprüfungen die Sicherheit auf Komponentenebene verwenden. Die der Bibliotheks Anwendung zugewiesenen Rollen werden in der Prozess Sicherheits Beschreibung nicht widergespiegelt. Die einzige Autorisierung, die von der Bibliotheks Anwendung gesteuert werden kann, ist auf der Komponentenebene. Weitere Informationen zur Sicherheit auf Komponentenebene finden Sie unter [Sicherheitsgrenzen](security-boundaries.md).

Informationen zum Festlegen der Sicherheit auf Komponentenebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).

## <a name="configuration-scenarios"></a>Konfigurationsszenarien

Zum besseren Verständnis der Auswirkungen der Entscheidung, ob die Bibliotheks Anwendung rollenbasierte Sicherheit verwenden soll und ob die Bibliotheks Anwendung nicht authentifiziert werden soll, sollten Sie die folgenden Szenarien beachten:

-   **Die Authentifizierung ist aktiviert, und die rollenbasierte Sicherheit wird verwendet.** In diesem Szenario werden Sicherheitsüberprüfungen durch den Hostingprozess vorgenommen, und einigen Aufrufern wird der Zugriff auf Prozessebene verweigert. Außerdem erfolgt die Rollen Überprüfung auf der Anwendungsebene der Bibliothek, sodass einige Aufrufer, die Sie durch die Sicherheitsüberprüfung auf Prozessebene machen, den Zugriff auf die Bibliotheks Anwendung verweigert, wenn die Rollen Mitgliedschaft überprüft wird. Dies ist das übliche Szenario für eine COM+-Bibliotheks Anwendung, die rollenbasierte Sicherheit verwendet.

    Die folgende Abbildung zeigt das Szenario, in dem die Authentifizierung aktiviert ist, und die Rollen Überprüfung verwendet wird.

    ![Diagramm, das die Authentifizierung in einem Host Prozess anzeigt.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **Die Authentifizierung ist aktiviert, und die rollenbasierte Sicherheit wird nicht verwendet.** In diesem Szenario werden Sicherheitsüberprüfungen auf Prozessebene ausgeführt, aber die Rollen Mitgliedschaft wird nicht auf der Ebene der Bibliotheks Anwendung überprüft. Daher erhält jeder Aufrufer der Bibliotheks Anwendung, der die Sicherheitsüberprüfung auf Prozessebene durchführt, Zugriff auf die Bibliotheks Anwendung, da die Rollen Mitgliedschaft nicht überprüft wird. Diese Situation besteht, wenn eine COM-Anwendung, die keine rollenbasierte Sicherheit verwendet, zu einer COM+-Bibliotheks Anwendung migriert wird.

    Die folgende Abbildung zeigt das Szenario, in dem die Authentifizierung aktiviert ist, und die Rollen Überprüfung wird nicht verwendet.

    ![Diagramm, das die Authentifizierung auf Prozessebene für eine Bibliotheks Anwendung innerhalb des Host Prozesses anzeigt.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **Die Authentifizierung ist deaktiviert, und die rollenbasierte Sicherheit wird verwendet.** In diesem Szenario werden Sicherheitsüberprüfungen auf Prozessebene ausgeführt, aber Aufrufer der Bibliotheks Anwendung sind nicht authentifiziert. Tatsächlich sind Aufrufer der Bibliotheks Anwendung von der Sicherheitsüberprüfung auf Prozessebene ausgenommen. Da die Rollen Überprüfung aktiviert ist, bestimmt die Rollen Mitgliedschaft allein, wer Zugriff auf die Bibliotheks Anwendung erhält. Dieses Szenario kann sinnvoll sein, wenn die Sicherheitsüberprüfung, die durch den Hostingprozess durchgeführt wird, zu restriktiv ist, Sie jedoch eine bestimmte Zugriffsbeschränkung für die Bibliotheks Anwendung oder bestimmte Schnittstellen oder Methoden benötigen. Dieses Szenario ermöglicht es Ihnen, die Prozesssicherheit effektiv zu deaktivieren und weiterhin mithilfe der rollenbasierten Sicherheit Überprüfungen auf ebenenzugriff zu verfügen.

    Das Szenario, in dem die Authentifizierung deaktiviert ist und die Rollen Überprüfung verwendet wird, ist in der folgenden Abbildung dargestellt.

    ![Diagramm, das die "Überprüfung der Rollen Mitgliedschaft" in einer Bibliotheks Anwendung innerhalb eines Host Prozesses anzeigt.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **Die Authentifizierung ist deaktiviert, und die rollenbasierte Sicherheit wird nicht verwendet.** In diesem Szenario werden Sicherheitsüberprüfungen weiterhin auf Prozessebene durchgeführt, aber wie im vorhergehenden Szenario übergeben Aufrufer der Bibliotheks Anwendung immer diese Sicherheitsüberprüfung. Da die Rollen Überprüfung ebenfalls deaktiviert ist, wird die Rollen Mitgliedschaft nicht auf der Ebene der Bibliotheks Anwendung überprüft. Im Wesentlichen kann jeder die Bibliotheks Anwendung anrufen. Dieses Szenario sollte ausgewählt werden, wenn Ihr COM-Objekt nicht authentifizierte Rückrufe empfangen muss, wie es bei einem ActiveX-Steuerelement der Fall sein kann, das von Internet Explorer und einem Microsoft Management Console-Snap-in gehostet wird. Natürlich muss dieses COM-Objekt vertrauenswürdig sein, damit es sich beim Empfang nicht authentifizierter Aufrufe entsprechend verhält. Beispielsweise sollte er nicht auf beliebige Dateien im Namen seiner Aufrufer zugreifen.

    Das Szenario, in dem die Authentifizierung deaktiviert ist und die Rollen Überprüfung nicht verwendet wird, ist in der folgenden Abbildung dargestellt.

    ![Diagramm, das Aufrufe einer Bibliotheks Anwendung anzeigt, die innerhalb des Host Prozesses nicht authentifiziert sind.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Nachdem Sie entschieden haben, ob Sie die Authentifizierung für Ihre COM+-Bibliotheks Anwendung aktivieren oder deaktivieren möchten, finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md) eine schrittweise Anleitung, in der erläutert wird, wie die Authentifizierung mithilfe des Verwaltungs Programms Komponenten Dienste deaktiviert (oder aktiviert) wird. Wenn Ihre Bibliotheks Anwendung rollenbasierte Sicherheit verwendet, finden Sie weitere Informationen unter [Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit der Bibliothek Anwendungen](library-application-security.md)
</dt> </dl>

 

 



