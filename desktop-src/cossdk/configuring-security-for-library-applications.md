---
description: Bei der Konfiguration der rollenbasierten Sicherheit und Authentifizierung für Bibliotheksanwendungen müssen besondere Aspekte berücksichtigt werden.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Konfigurieren der Sicherheit für Bibliotheksanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0d8b3993a00512c20409f1f029b7402d5f9ace97984cbe9757453b5672125f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548907"
---
# <a name="configuring-security-for-library-applications"></a>Konfigurieren der Sicherheit für Bibliotheksanwendungen

Bei der Konfiguration der rollenbasierten Sicherheit und Authentifizierung für Bibliotheksanwendungen müssen besondere Aspekte berücksichtigt werden.

## <a name="enabling-or-disabling-authentication"></a>Aktivieren oder Deaktivieren der Authentifizierung

Einer der zu berücksichtigenden Faktoren ist, ob Aufrufer der Bibliotheksanwendung den Sicherheitsüberprüfungen auf Prozessebene des Hostprozesses unterliegen sollten, d.&a0;b. ob die Authentifizierung aktiviert oder deaktiviert werden soll.

Wenn die Bibliotheksanwendung beispielsweise von einem Browser gehostet wird, muss sie möglicherweise nicht authentifizierte Rückrufe empfangen. Um diesen Bedarf zu erfüllen, können Sie die Authentifizierung deaktivieren, damit der Hostingprozess keine Sicherheitsüberprüfungen für Aufrufer der Bibliotheksanwendung vorsingt. Wenn Sie die Authentifizierung deaktivieren, wird die Bibliotheksanwendung effektiv nicht authentifiziert– alle Aufrufe an sie werden erfolgreich sein. Aufrufer der Bibliotheksanwendung unterliegen nicht den Sicherheitsüberprüfungen des Hostingprozesses. Im Grunde wird die Bibliotheksanwendung als "nicht authentifiziert" gekennzeichnet, und Sicherheitsüberprüfungen werden für Aufrufe der Bibliotheksanwendung ausgelassen.

Informationen zum Aktivieren oder Deaktivieren der Authentifizierung finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheksanwendung.](enabling-authentication-for-a-library-application.md)

## <a name="enforcing-role-checks"></a>Erzwingen von Rollenüberprüfungen

Eine weitere Entscheidung ist, ob die Bibliotheksanwendung [rollenbasierte Sicherheit verwenden soll.](role-based-security-administration.md) Wenn rollenbasierte Sicherheit verwendet wird, müssen Sie sicherheit auf Komponentenebene verwenden, damit Zugriffsüberprüfungen durchgeführt werden können. Die der Bibliotheksanwendung zugewiesenen Rollen werden nicht in der Prozesssicherheitsbeschreibung widergespiegelt. Die einzige Autorisierung, die die Bibliotheksanwendung steuern kann, ist die Komponentenebene. Weitere Informationen zur Sicherheit auf Komponentenebene finden Sie unter [Sicherheitsgrenzen](security-boundaries.md).

Informationen zum Festlegen der Sicherheit auf Komponentenebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen.](setting-a-security-level-for-access-checks.md)

## <a name="configuration-scenarios"></a>Konfigurationsszenarien

Um die Auswirkungen der Entscheidung zu verstehen, ob die Bibliotheksanwendung rollenbasierte Sicherheit verwenden soll und ob die Bibliotheksanwendung nicht authentifiziert werden soll, sollten Sie die folgenden Szenarien in Betracht ziehen:

-   **Die Authentifizierung ist aktiviert, und die rollenbasierte Sicherheit wird verwendet.** In diesem Szenario werden Sicherheitsüberprüfungen vom Hostingprozess durchgeführt, und einigen Aufrufern wird der Zugriff auf Prozessebene verweigert. Außerdem erfolgt die Rollenüberprüfung auf Bibliotheksanwendungsebene, sodass einigen Aufrufern, die die Sicherheitsüberprüfung auf Prozessebene durchgeführt haben, der Zugriff auf die Bibliotheksanwendung verweigert wird, wenn die Rollenmitgliedschaft überprüft wird. Dies ist das übliche Szenario für eine COM+-Bibliotheksanwendung, die rollenbasierte Sicherheit verwendet.

    Die folgende Abbildung zeigt das Szenario, in dem die Authentifizierung aktiviert und die Rollenüberprüfung verwendet wird.

    ![Diagramm, das die Authentifizierung innerhalb eines Hostprozesses zeigt.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **Die Authentifizierung ist aktiviert, und die rollenbasierte Sicherheit wird nicht verwendet.** In diesem Szenario werden Sicherheitsüberprüfungen auf Prozessebene durchgeführt, die Rollenmitgliedschaft wird jedoch nicht auf bibliotheksanwendungsebene überprüft. Daher erhält jeder Aufrufer der Bibliotheksanwendung, die die Sicherheitsüberprüfung auf Prozessebene durchfingt, Zugriff auf die Bibliotheksanwendung, da die Rollenmitgliedschaft nicht überprüft wird. Diese Situation würde bestehen, wenn eine COM-Anwendung, die keine rollenbasierte Sicherheit verwendet, zu einer COM+-Bibliotheksanwendung migriert wird.

    Die folgende Abbildung zeigt das Szenario, in dem die Authentifizierung aktiviert ist und die Rollenüberprüfung nicht verwendet wird.

    ![Diagramm, das die Authentifizierung auf Prozessebene für eine Bibliotheksanwendung innerhalb des Hostprozesses zeigt.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **Die Authentifizierung ist deaktiviert, und die rollenbasierte Sicherheit wird verwendet.** In diesem Szenario werden Sicherheitsüberprüfungen auf Prozessebene durchgeführt, aber Aufrufer der Bibliotheksanwendung sind nicht authentifiziert. Aufrufer der Bibliotheksanwendung sind von der Sicherheitsüberprüfung auf Prozessebene ausgenommen. Da die Rollenüberprüfung aktiviert ist, bestimmt die Rollenmitgliedschaft allein, wer Zugriff auf die Bibliotheksanwendung erhält. Dieses Szenario kann geeignet sein, wenn die Vom Hostingprozess durchgeführte Sicherheitsüberprüfung zu restriktiv ist, Sie jedoch eine Zugriffseinschränkung für die Bibliotheksanwendung oder für bestimmte Schnittstellen oder Methoden benötigen. In diesem Szenario können Sie die Prozesssicherheit effektiv deaktivieren und dennoch über eine geeignete Ebene für Zugriffsüberprüfungen mithilfe der rollenbasierten Sicherheit verfügen.

    Das Szenario, in dem die Authentifizierung deaktiviert ist und die Rollenüberprüfung verwendet wird, ist in der folgenden Abbildung dargestellt.

    ![Diagramm, das "Überprüfung auf Rollenmitgliedschaft" in einer Bibliotheksanwendung innerhalb eines Hostprozesses zeigt.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **Die Authentifizierung ist deaktiviert, und die rollenbasierte Sicherheit wird nicht verwendet.** In diesem Szenario werden sicherheitsüberprüfungen weiterhin auf Prozessebene durchgeführt, aber wie im vorherigen Szenario bestehen Aufrufer der Bibliotheksanwendung diese Sicherheitsüberprüfung immer. Da die Rollenüberprüfung ebenfalls deaktiviert ist, wird die Rollenmitgliedschaft nicht auf Bibliotheksanwendungsebene überprüft. Im Wesentlichen kann jeder die Bibliotheksanwendung aufrufen. Dieses Szenario sollte ausgewählt werden, wenn Ihr COM-Objekt nicht authentifizierte Rückrufe empfangen muss, wie dies bei einem ActiveX-Steuerelement der Fall sein kann, das von Internet Explorer und mit einem Microsoft Management Console-Snap-In gehostet wird. Dieses COM-Objekt muss natürlich als vertrauenswürdig eingestuft werden, damit es sich beim Empfangen nicht authentifizierter Aufrufe entsprechend verhält. Beispielsweise sollte er nicht im Namen seiner Aufrufer auf beliebige Dateien zugreifen.

    Das Szenario, in dem die Authentifizierung deaktiviert und die Rollenüberprüfung nicht verwendet wird, ist in der folgenden Abbildung dargestellt.

    ![Diagramm, das Aufrufe einer Bibliotheksanwendung zeigt, die innerhalb des Hostprozesses nicht authentifiziert sind.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Nachdem Sie entschieden haben, ob die Authentifizierung für [](enabling-authentication-for-a-library-application.md) Ihre COM+-Bibliotheksanwendung aktiviert oder deaktiviert werden soll, finden Sie unter Aktivieren der Authentifizierung für eine Bibliotheksanwendung eine schritt-für-Schritt-Prozedur, in der erläutert wird, wie die Authentifizierung mit dem Verwaltungstool komponentendienste deaktiviert (oder aktiviert) wird. Wenn Ihre Bibliotheksanwendung rollenbasierte Sicherheit verwendet, finden Sie weitere Informationen unter [Konfigurieren Role-Based Sicherheit.](configuring-role-based-security.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit von Bibliotheksanwendung](library-application-security.md)
</dt> </dl>

 

 



