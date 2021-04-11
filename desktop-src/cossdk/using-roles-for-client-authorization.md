---
description: Mithilfe der rollenbasierten Sicherheit richten Sie eine Autorisierungs Richtlinie ein, um zu bestimmen, welche Clients und mit welcher Autorität Sie zulassen müssen. Sie entscheiden, wer welche Aktionen ausführen und auf welche Ressourcen zugreifen soll.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Verwenden von Rollen für die Client Autorisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ae748ddfec438a79e3d0440a00ed7c2f672aed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127005"
---
# <a name="using-roles-for-client-authorization"></a>Verwenden von Rollen für die Client Autorisierung

Mithilfe der rollenbasierten Sicherheit richten Sie eine Autorisierungs Richtlinie ein, um zu bestimmen, welche Clients und mit welcher Autorität Sie zulassen müssen. Sie entscheiden, wer welche Aktionen ausführen und auf welche Ressourcen zugreifen soll.

Rollen vereinfachen dies, indem Sie als Zugriffs Steuerungsmechanismus fungieren, der immer dann aufgerufen wird, wenn ein Benutzer versucht, auf eine Anwendungs Ressource zuzugreifen. Eine Rolle ist im Grunde genommen eine Liste von Benutzern – genauer genommen eine symbolische Kategorie von Benutzern, die dieselbe Sicherheits Berechtigung gemeinsam nutzen. Wenn Sie einer Anwendungs Ressource eine Rolle zuweisen, erteilen Sie jeder Person, die Mitglied dieser Rolle ist, die Zugriffsberechtigung für diese Ressource.

Daher können Sie eine bestimmte Sicherheits Berechtigung definieren, indem Sie Sie als Rolle deklarieren und die Rolle dann bestimmten Ressourcen zuweisen. Wenn die Anwendung bereitgestellt wird, kann der Systemadministrator die Rolle mit den tatsächlichen Benutzern und Benutzergruppen auffüllen. Wenn die Anwendung ausgeführt wird, erzwingt com+ die Richtlinie durch Ausführen von Rollen Überprüfungen.

Grundsätzlich helfen Rollen dabei, Ihren Code zu schützen, d. –. die Methoden, die von Clients einer COM+-Anwendung aufgerufen werden können. Die Rollen Mitgliedschaft wird geprüft, wenn ein Client versucht, eine Methode aufzurufen, die von einer Komponente in einer Anwendung verfügbar gemacht wird. Wenn sich der Aufrufer in einer Rolle befindet, die der aufgerufenen Methode oder Ressource zugewiesen ist, wird der Aufruf erfolgreich ausgeführt. Andernfalls tritt ein Fehler auf.

## <a name="declarative-role-based-security"></a>Sicherheit deklarativer Role-Based

Mit der deklarativen rollenbasierten Sicherheit deklarieren Sie Rollen administrativ – entweder mithilfe des Verwaltungs Programms Komponenten Dienste oder der administrativen Funktionen – und weisen Sie Sie den Anwendungs Ressourcen administrativ zu. Wo und wie Sie die deklarative Sicherheit festlegen, legen fest, wo Sicherheitsgrenzen für Ihre Anwendung gezeichnet werden. Weitere Details finden Sie unter [Sicherheitsgrenzen](security-boundaries.md).

Sie können der gesamten Anwendung eine bestimmte Rolle, einer bestimmten Komponente, einer bestimmten Schnittstelle in einer Komponente oder einer bestimmten Methode in einer Schnittstelle zuweisen. Rollenzuweisungen werden in der natürlichen Inklusions Kette geerbt – d. h., wenn Sie einer Komponente eine Rolle zuweisen, wird Sie implizit jeder Schnittstelle und Methode zugewiesen, die von dieser Komponente verfügbar gemacht wird.

Mit der Verfügbarkeit von Rollenzuweisungen auf Methoden Ebene können Sie Komponenten und Schnittstellen, die nicht im Hinblick auf Sicherheit entwickelt wurden, effektiv schützen. Wenn die Methoden selbst jedoch nicht mit deklarativen Rollenzuweisungen Sicherungs fähig sind, müssen Sie möglicherweise eine programmgesteuerte Rollen Überprüfung durchführen. Im Allgemeinen empfiehlt es sich, die Sicherheit zu berücksichtigen, wenn Sie entscheiden, wie Sie Geschäftsfunktionen durch Methoden gestalten möchten. Andernfalls könnten Sie in der letzten Minute in Sicherheits bezogenes Code hinzufügen.

Ausführliche Verfahren zum Festlegen der rollenbasierten Sicherheit finden Sie unter [Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Programmgesteuerte Sicherheit

Unter bestimmten Umständen möchten Sie ggf. Sicherheitslogik in Komponenten platzieren, während Sie weiterhin rollenbasierte Sicherheit verwenden. Es kann sein, dass Sie nicht in der Lage sind, zu – oder nicht zu – alle Zugriffs Entscheidungen durch Methoden zu berücksichtigen. Angenommen, Sie verfügen über eine private Anwendungs Ressource, z. b. eine bestimmte Datenbank, auf die nur einige Aufrufer einer Methode zugreifen können, während Sie andere ausschließen. Oder Sie verfügen möglicherweise über eine einzige TransferMoney-Methode und möchten einige Aufrufer einschränken, indem Sie den Betrag begrenzen, den Sie übertragen können.

Unter diesen Umständen können Sie die Rollen Überprüfung im Code durchführen. Es wird eine einfache API bereitgestellt, mit der Sie überprüfen können, ob Sicherheit aktiviert ist und ob ein Aufrufer oder ein bestimmter Benutzer eine bestimmte Rolle hat. Diese Funktionalität ist nur verfügbar, wenn rollenbasierte Sicherheit aktiviert ist. Dies bedeutet, dass Sie immer noch von der deklarativen rollenbasierten Sicherheit profitieren können, wenn dies ausreicht, und Sie können Sie bei Bedarf Programm gesteuert auf eine präzisere Granularitätsstufe ausdehnen.

Wenn Sie die rollenbasierte Sicherheit verwenden, haben Sie außerdem programmgesteuerten Zugriff auf Informationen über alle Upstreamaufrufer in der Kette von Aufrufen Ihrer Komponente. Dies ist besonders nützlich, wenn Sie einen detaillierten Überwachungs Pfad beibehalten möchten.

Beschreibungen zum Durchführen der Rollen Überprüfung im Code und zum Zugreifen auf Kontextinformationen des Sicherheits Aufrufens finden Sie Unterprogramm gesteuerte [Komponentensicherheit](programmatic-component-security.md).

## <a name="authorization-and-authentication"></a>Autorisierung und Authentifizierung

Eine sinnvolle Autorisierung setzt voraus, dass Sie sicher sind, dass die Clients tatsächlich von den Benutzern stammen. Die Überprüfung der Client Identität erfolgt separat durch einen Authentifizierungsdienst. Ohne Authentifizierung erlauben Sie im Grunde Aufrufern das-System für die untergeordnete Steuerung. Beschreibungen der Authentifizierung bei com+-Anwendungen finden Sie unter [Client Authentifizierung](client-authentication.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Informationen zum Sicherheits Aufrufkontext](security-call-context-information.md)
</dt> <dt>

[Sicherheitskontext Eigenschaft](security-context-property.md)
</dt> </dl>

 

 



