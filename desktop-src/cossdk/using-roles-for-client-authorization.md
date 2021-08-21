---
description: Sie verwenden die rollenbasierte Sicherheit, um eine Autorisierungsrichtlinie zu erstellen, die bestimmt, welchen Client bzw. welche Clients ein- und mit welcher Autorität verwendet werden soll. Sie entscheiden, wer welche Aktionen ausführen und auf welche Ressourcen zugreifen soll.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Verwenden von Rollen für die Clientautorisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a808abc08d5360ba0b7fae0a7c31af80a4cab28c43e6014076c549204e6f28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499644"
---
# <a name="using-roles-for-client-authorization"></a>Verwenden von Rollen für die Clientautorisierung

Sie verwenden die rollenbasierte Sicherheit, um eine Autorisierungsrichtlinie zu erstellen, die bestimmt, welchen Client bzw. welche Clients ein- und mit welcher Autorität verwendet werden soll. Sie entscheiden, wer welche Aktionen ausführen und auf welche Ressourcen zugreifen soll.

Rollen erleichtern dies, indem sie als Zugriffssteuerungsmechanismus agieren, der aufgerufen wird, wenn ein Benutzer versucht, auf eine Anwendungsressource zu zugreifen. Eine Rolle ist im Grunde eine Liste von Benutzern– genauer gesagt eine symbolische Kategorie von Benutzern, die die gleichen Sicherheitsberechtigungen haben. Wenn Sie einer Anwendungsressource eine Rolle zuweisen, erteilen Sie der Person, die Mitglied dieser Rolle ist, die Zugriffsberechtigung für diese Ressource.

Daher können Sie ein sehr bestimmtes Sicherheitsprivileg definieren, indem Sie es als Rolle deklarieren und die Rolle dann bestimmten Ressourcen zuweisen. Wenn die Anwendung bereitgestellt wird, kann der Systemadministrator die Rolle mit tatsächlichen Benutzern und Benutzergruppen auffüllen. Wenn die Anwendung ausgeführt wird, erzwingt COM+ die Richtlinie durch Durchführen von Rollenüberprüfungen.

Im Wesentlichen tragen Rollen zum Schutz Ihres Codes bei, d.&amp;160;B. die Methoden, die von Clients einer COM+-Anwendung aufgerufen werden können. Die Rollenmitgliedschaft wird immer dann überprüft, wenn ein Client versucht, eine Methode auf aufruft, die von einer Komponente in einer Anwendung verfügbar gemacht wird. Wenn sich der Aufrufer in einer Rolle befindet, die der aufgerufenen Methode oder Ressource zugewiesen ist, ist der Aufruf erfolgreich. andernfalls schlägt dies fehl.

## <a name="declarative-role-based-security"></a>Deklarative Role-Based Sicherheit

Mit deklarativer rollenbasierter Sicherheit deklarieren Sie Rollen – entweder mithilfe des Komponentendienste-Verwaltungstools oder der Verwaltungsfunktionen – und weisen sie Anwendungsressourcen administratorisch zu. Wo und wie Sie die deklarative Sicherheit festlegen, bestimmt, wo Sicherheitsgrenzen für Ihre Anwendung gezogen werden. Weitere Informationen finden Sie unter [Sicherheitsgrenzen.](security-boundaries.md)

Sie können eine bestimmte Rolle der gesamten Anwendung, einer bestimmten Komponente, einer bestimmten Schnittstelle in einer Komponente oder einer bestimmten Methode auf einer Schnittstelle zuweisen. Rollenzuweisungen werden in der natürlichen Inklusionskette vererbt. Wenn Sie also einer Komponente eine Rolle zuweisen, wird sie implizit jeder Schnittstelle und Methode zugewiesen, die von dieser Komponente verfügbar gemacht wird.

Mit der Verfügbarkeit von Rollenzuweisungen auf Methodenebene können Sie effektiv dabei helfen, Komponenten und Schnittstellen zu schützen, die nicht im Sinne der Sicherheit entworfen wurden. Wenn die Methoden selbst jedoch nicht mit deklarativen Rollenzuweisungen sicherungsfähig sind, müssen Sie möglicherweise eine programmgesteuerte Rollenüberprüfung durcharbeiten. Im Allgemeinen ist es eine gute Idee, die Sicherheit im Hinterkopf zu behalten, wenn Sie entscheiden, wie Geschäftsfunktionen durch Methoden faktor werden sollen. Andernfalls könnten Sie in letzter Minute sicherheitsbezogenen Code hinzufügen.

Ausführliche Verfahren zum Festlegen der rollenbasierten Sicherheit finden Sie unter [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Programmgesteuerte Sicherheit

Unter bestimmten Umständen sollten Sie Sicherheitslogik in Komponenten unter Verwendung der rollenbasierten Sicherheit einteilen. Es kann sein, dass Sie nicht in der Lage sind oder sich dafür entscheiden, alle Zugriffsentscheidungen über Methoden zu berücksichtigen. Beispielsweise können Sie über eine private Anwendungsressource verfügen, z. B. eine bestimmte Datenbank, auf die nur einige Aufrufer einer Methode zugreifen können sollen, während andere davon ausgenommen werden. Oder Sie verfügen über eine einzelne TransferMoney-Methode und möchten einige Aufrufer einschränken, indem Sie den Betrag einschränken, den sie übertragen können.

In solchen Fällen können Sie rollenüberprüfungen im Code ausführen. Es wird eine einfache API bereitgestellt, mit der Sie überprüfen können, ob die Sicherheit aktiviert ist und ob sich ein Aufrufer oder ein bestimmter Benutzer in einer bestimmten Rolle befindet. Diese Funktionalität ist nur verfügbar, wenn die rollenbasierte Sicherheit aktiviert ist. Dies bedeutet, dass Sie weiterhin die deklarative rollenbasierte Sicherheit dort nutzen können, wo sie ausreichend ist, und sie dann programmgesteuert auf eine höhere Granularitätsstufe erweitern können, wenn dies erforderlich ist.

Darüber hinaus haben Sie bei Verwendung der rollenbasierten Sicherheit programmgesteuerten Zugriff auf Informationen zu allen Upstreamaufrufern in der Kette der Aufrufe ihrer Komponente. Dies ist besonders nützlich, wenn Sie einen detaillierten Überwachungspfad behalten möchten.

Beschreibungen zum Ausführen der Rollenüberprüfung im Code und zum Zugreifen auf Kontextinformationen für Sicherheitsaufrufe finden Sie unter [Programmgesteuerte Komponentensicherheit.](programmatic-component-security.md)

## <a name="authorization-and-authentication"></a>Autorisierung und Authentifizierung

Durch eine sinnvolle Autorisierung können Sie sicher sein, dass Clients tatsächlich die Person sind, von der sie sagen, dass sie es sind. Die Überprüfung der Clientidentität wird separat von einem Authentifizierungsdienst ausgeführt. Ohne Authentifizierung lassen Sie Aufrufer im Honor-System grundsätzlich zu. Beschreibungen der Authentifizierung mit Auswirkungen auf COM+-Anwendungen finden Sie unter [Clientauthentifizierung](client-authentication.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Kontextinformationen zu Sicherheitsaufrufen](security-call-context-information.md)
</dt> <dt>

[Sicherheitskontexteigenschaft](security-context-property.md)
</dt> </dl>

 

 



