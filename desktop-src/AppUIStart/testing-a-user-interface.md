---
title: Testen einer Benutzeroberfläche
description: In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Testen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e86282c03502642541c0ea1318b8ccaf6d16b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949031"
---
# <a name="testing-a-user-interface"></a>Testen einer Benutzeroberfläche

In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Testen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.

-   [Introduction (Einführung)](#introduction)
-   [Benutzerbarkeits Tests](#usability-testing)
-   [Barrierefreiheits Tests](#accessibility-testing)

## <a name="introduction"></a>Einführung

Zum vollständigen ermitteln der Effektivität und der allgemeinen Nutzbarkeit einer Anwendungs Benutzeroberfläche muss Sie getestet werden. Das Testen gibt an, wie einfach oder schwierig die Benutzeroberfläche für ein möglichst breites Publikum verwendet werden kann. Die Zeit, die für das Testen einer Anwendung benötigt wird, ist sehr wertvoll.

Dieses Thema konzentriert sich auf drei primäre Testszenarien: allgemeine Benutzerfreundlichkeit, Barrierefreiheit und Automatisierung.

## <a name="usability-testing"></a>Nutzbarkeitstests

Das Testen der Benutzerfreundlichkeit bietet die Möglichkeit, ein Produkt zu evaluieren, indem Sie prüfen, wie echte Benutzer das Produkt tatsächlich verwenden. Diese Analyse stellt sicher, dass wichtige Annahmen über beabsichtigte Benutzer und Schnittstellen Entwürfe mit echten Daten unterstützt (oder gestellt) werden. Nur durch das Sammeln dieser Daten können Sie feststellen, wie gut die Benutzeroberfläche für ein Produkt den Anforderungen und Erwartungen der Benutzer entspricht.

Durch das Beobachten der Benutzerinteraktion mit dem Produkt und das Lauschen auf Benutzer Feedback werden wichtige Features identifiziert, die möglicherweise schwer zu finden und zu verwenden sind. Basierend auf diesen Ergebnissen können bei Bedarf Anpassungen an der Benutzeroberfläche vorgenommen werden. Es ist fast unmöglich, ein nützliches Produkt zu erstellen, ohne eine gewisse Benutzerfreundlichkeit zu testen, da die Ergebnisse die Grundlage für bessere Entscheidungen über das Produkt und eine Verbesserung der allgemeinen Benutzerfreundlichkeit bilden.

Das Testen der Benutzerfreundlichkeit bietet nur dann eine deutliche Rückzahlung, wenn Sie in den gesamten Projektlebenszyklus integriert ist. Mit einer einzelnen Nutzbarkeits Studie können Probleme identifiziert werden, aber ohne nachfolgenden Tests ist es schwierig zu bestimmen, ob die Lösungen diese Probleme gelöst oder neue eingeführt haben.

Die wichtigsten Szenarien für die Verwendbarkeit von Tests sind:

-   Wenn Sie ein Softwareprodukt Hersteller sind, bedeutet das Testen von echten Benutzern Ihres Produkts, dass Sie den Entwurf Auswerten. Können Benutzer basierend auf der Art und Weise, wie Sie die Anwendung entworfen haben, die Aufgaben ausführen, die Sie ausführen müssen? Das Testen von echten Benutzern, die echte Aufgaben ausführen, kann auch darauf hinweisen, ob die Benutzeroberflächen-Richtlinien, die Sie befolgen, innerhalb des Kontexts Ihres Produkts funktionieren und ob die Fähigkeit eines Benutzers, seine Arbeit zu erledigen, von der Konsistenz unterstützt wird.
-   Wenn Sie ein Softwareprodukt Käufer sind, können Sie Nutz barkeits Tests durchführen, um ein Produkt für den Kauf zu evaluieren. Beispielsweise kann Ihr Unternehmen in Erwägung gezogen, ein Produkt für seine 20000-Mitarbeiter zu kaufen. Bevor das Unternehmen sein Geld verbringt, möchte ich sicherstellen, dass das betreffende Produkt den Mitarbeitern wirklich hilft, ihre Arbeit zu verbessern. Benutzeroberflächentests können auch hilfreich sein, um festzustellen, ob die vorgeschlagene Anwendung den Richtlinien für die Richtlinien für das veröffentlichte UI (intern oder extern Es empfiehlt sich, Benutzeroberflächen-Richtlinien als Hilfsanweisungen anstelle der primären Quelle von Informationen zum Treffen von Kaufentscheidungen zu verwenden.

Weitere Informationen finden Sie unter [Benutzerfreundlichkeit in der Praxis: benutzerbarkeits Tests](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing).

## <a name="accessibility-testing"></a>Barrierefreiheits Tests

Barrierefreiheits Tests umfassen zwei Bereiche eines UI-Entwurfs: Unterstützung für Benutzer mit Behinderungen und Programm gesteuerter Zugriff durch automatisierte Test-Frameworks.

Um sicherzustellen, dass eine Anwendung für Benutzer mit Behinderungen zugänglich ist, müssen Sie Folgendes testen:

-   Konformität: erfüllt die Anwendung verschiedene gesetzliche Anforderungen bezüglich der Barrierefreiheit?
-   Effektivität: können Benutzer mit Behinderungen die Anwendung verwenden?
-   Nützlichkeit: macht die Anwendung für Benutzer mit Behinderungen eine angemessene Funktionalität verfügbar?
-   Zufriedenheit: wie wird die Anwendung von Benutzern mit Behinderungen wahrgenommen?

Das Testen dieser Aspekte einer Anwendung kann über eine Barrierefreiheits Überwachung durchgeführt werden. hierzu gehört eine manuelle Überprüfung der Anwendung durch einen Barrierefreiheits Experten und eine gezielte Nutz barkeits Studie von deaktivierten Benutzern und hilfstechnologiegeräten.

Obwohl es scheinbar nicht zusammenhängend ist, gibt es eine enge Korrelation zwischen den programmgesteuerten Zugriffs Anforderungen automatisierter Test Frameworks und den Geräten von Hilfstechnologien. Die Unterstützung eines solchen hat den zusätzlichen Vorteil, der andere zu aktivieren. Weitere Informationen zu Barrierefreiheit und Testautomatisierung in Windows-Anwendungen finden Sie unter [Barrierefreiheit](/windows/desktop/accessibility), [TestTools](/windows/desktop/WinAuto/testing-tools)und [Windows Automation-API](/windows/desktop/WinAuto/windows-automation-api-portal).

 

 