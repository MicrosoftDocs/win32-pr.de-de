---
title: Testen eines Benutzeroberfläche
description: In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Testen einer Benutzeroberfläche für eine Windows Anwendung ausführlich beschrieben.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f3d6686cdcd892aa5608944cf8c1a20df0d44106a0fdac01b2bbbd855fe523
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507434"
---
# <a name="testing-a-user-interface"></a>Testen eines Benutzeroberfläche

In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Testen einer Benutzeroberfläche für eine Windows Anwendung ausführlich beschrieben.

-   [Introduction (Einführung)](#introduction)
-   [Benutzerfreundlichkeitstests](#usability-testing)
-   [Barrierefreiheitstests](#accessibility-testing)

## <a name="introduction"></a>Einführung

Um die Effektivität und allgemeine Nutzbarkeit einer Anwendungsoberfläche vollständig zu bestimmen, muss sie getestet werden. Tests machen die Benutzerfreundlichkeit oder Die Benutzerfreundlichkeit der Benutzeroberfläche für eine möglichst breite Zielgruppe sichtbar. Die Zeit, die zum Testen einer Anwendung benötigt wird, lohnt sich.

Dieses Thema konzentriert sich auf drei primäre Testszenarien: allgemeine Benutzerfreundlichkeit, Barrierefreiheit und Automatisierung.

## <a name="usability-testing"></a>Nutzbarkeitstests

Benutzerfreundlichkeitstests bieten die Möglichkeit, ein Produkt zu bewerten, indem untersucht wird, wie echte Benutzer das Produkt tatsächlich verwenden. Diese Analyse stellt sicher, dass wichtige Annahmen zu beabsichtigten Benutzern und Schnittstellenentwürfen mit echten Daten unterstützt (oder herausgefordert) werden. Nur durch das Sammeln dieser empirischen Daten können Sie herausfinden, wie gut die Benutzeroberfläche für ein Produkt den Anforderungen und Erwartungen Ihrer Benutzer entspricht.

Durch das Beobachten der Benutzerinteraktion mit dem Produkt und das Lauschen auf Benutzerfeedback werden wichtige Features identifiziert, die möglicherweise schwer zu finden und zu verwenden sind. Basierend auf diesen Ergebnissen können Bei Bedarf Anpassungen an der Benutzeroberfläche vorgenommen werden. Es ist fast unmöglich, ein nützliches Produkt ohne ein gewisses Maß an Benutzerfreundlichkeitstests zu erstellen, da die Ergebnisse die Grundlage für bessere Entscheidungen über das Produkt und die Verbesserung der allgemeinen Benutzerfreundlichkeit bilden.

Benutzerfreundlichkeitstests bieten nur dann eine erhebliche Auszahlung, wenn sie gut in den gesamten Projektlebenszyklus integriert sind. Eine einzelne Benutzerfreundlichkeitsstudie kann Probleme identifizieren, aber ohne Folgetests ist es schwierig zu bestimmen, ob die Lösungen diese Probleme gelöst oder neue eingeführt haben.

Die wichtigsten Szenarien für Benutzerfreundlichkeitstests sind:

-   Wenn Sie softwareproduktanbieter sind, bedeutet das Testen realer Benutzer Ihres Produkts, dass Sie den Entwurf auswerten. Können Benutzer basierend auf der Art und Weise, wie Sie die Anwendung entworfen haben, die Aufgaben ausführen, die sie ausführen müssen? Das Testen von echten Benutzern, die echte Aufgaben ausführen, kann auch darauf hinweisen, ob die von Ihnen befolgen Benutzeroberflächenrichtlinien im Kontext Ihres Produkts funktionieren und wenn Konsistenz die Fähigkeit eines Benutzers zur Durchführung seiner Arbeit erleichtert oder beeinträchtigt.
-   Wenn Sie ein Softwareprodukthersteller sind, können Sie Benutzerfreundlichkeitstests durchführen, um ein Produkt für den Kauf auszuwerten. Ihr Unternehmen könnte beispielsweise erwägen, ein Produkt für seine 20.000 Mitarbeiter zu kaufen. Bevor das Unternehmen sein Geld ausgibt, möchte es sicherstellen, dass das betreffende Produkt mitarbeitern wirklich hilft, ihre Arbeit besser zu erledigen. Benutzerfreundlichkeitstests können auch nützlich sein, um festzustellen, ob die vorgeschlagene Anwendung veröffentlichten Richtlinien für den Benutzeroberflächenstil folgt (intern oder extern). Es ist am besten, Benutzeroberflächenrichtlinien als zusätzliche und nicht als primäre Informationsquelle zu verwenden, um Kaufentscheidungen zu treffen.

Weitere Informationen finden Sie unter [Usability in Practice: Usability Testing](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing).

## <a name="accessibility-testing"></a>Barrierefreiheitstests

Barrierefreiheitstests umfassen zwei Bereiche eines Benutzeroberflächenentwurfs: Unterstützung für Benutzer mit Behinderungen und programmgesteuerter Zugriff durch automatisierte Testframeworks.

Um sicherzustellen, dass Benutzer mit Behinderungen auf eine Anwendung zugreifen können, müssen Folgendes getestet werden:

-   Compliance: Entspricht die Anwendung verschiedenen rechtlichen Anforderungen in Bezug auf die Barrierefreiheit?
-   Effektivität: Können Benutzer mit Behinderungen die Anwendung verwenden?
-   Nützlichkeit: Macht die Anwendung eine angemessene Funktionalität für Benutzer mit Behinderungen verfügbar?
-   Zufriedenheit: Wie wird die Anwendung von Benutzern mit Behinderungen wahrgenommen?

Tests für diese Aspekte einer Anwendung können durch eine Barrierefreiheitsüberwachung durchgeführt werden, die eine manuelle Überprüfung der Anwendung durch einen Barrierefreiheitsexperten und eine fokussierte Benutzerfreundlichkeitsstudie für deaktivierte Benutzer und Hilfstechnologiegeräte umfasst.

Obwohl scheinbar nichts zu tun hat, besteht eine enge Korrelation zwischen den programmgesteuerten Zugriffsanforderungen von automatisierten Testframeworks und denen von Hilfstechnologiegeräten. Die Unterstützung des einen hat den zusätzlichen Vorteil, dass der andere aktiviert wird. Weitere Informationen zur Barrierefreiheit und Zur Testautomatisierung in Windows Anwendungen finden Sie unter [Barrierefreiheit,](/windows/desktop/accessibility) [Testtools](/windows/desktop/WinAuto/testing-tools)und die [Windows Automation-API.](/windows/desktop/WinAuto/windows-automation-api-portal)

 

 