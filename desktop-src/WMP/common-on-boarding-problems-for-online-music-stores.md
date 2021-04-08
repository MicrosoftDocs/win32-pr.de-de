---
title: Häufige Probleme bei der Integration von Online Musik Stores
description: Häufige Probleme bei der Integration von Online Musik Stores
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f600d1035e0fd20be7786af4d4ffed4482138a72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729385"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>Häufige Probleme bei der Integration von Online Musik Stores

Im folgenden finden Sie eine Liste allgemeiner Probleme bei der Windows Media Player-Einbindung, die Sie vermeiden sollten. Diese Probleme können dazu führen, dass für den Speicher ein Überprüfungs Test fehlschlägt. Wenn der RC2-Pass fehlschlägt, wird der Startvorgang auf das nächste verfügbare Startfenster verschoben.

1.  Fehler beim Übergang von Testservern zu Produktionsservern
    -   Fehlende Seiten
    -   IIS-Einstellungen (Zugriff, Vroots, HTTPS oder andere Sicherheitseinstellungen)
    -   Test Konten funktionieren nicht mehr.
    -   Für Test Konten werden keine Gutschriften angewendet.
    -   Von Diensten gehostete Logos werden nicht verschoben.
    -   IP-Einschränkungen, die zuvor bereits umgangen wurden, sind wieder aufgetreten. Insbesondere e-Commerce-Systeme haben möglicherweise einen anderen Satz von Einschränkungen von der Musik Website.
    -   Das serviceInfo-Dokument wird nicht aktualisiert, um auf die Produktion zu verweisen.
2.  Der Link "kaufen" (oder "Shop") im Bereich "jetzt wiedergeben" ist ungültig. Dies ist ein häufig übersehenes Problem, das dazu führt, dass Ihr Speicher fehlschlägt, auch wenn alles andere in der richtigen Reihenfolge ist.
3.  Die Tester von Microsoft müssen über eine angemessene Erwerbs Leistung verfügen. Das Validierungs Team von Microsoft führt verschiedene Kauf Szenarien aus, die von kleinen Käufen bis zu sehr großen Käufen reichen. Sie müssen eine erneut aufladbare Methode bereitstellen, damit Sie als Consumer innerhalb Ihres Stores agieren können. Dies kann von der Bereitstellung einer Vielzahl von Konten über die Bereitstellung einer Dummy-Kreditkarte reichen. Beispielsweise schlägt ein Speicher in RC2 fehl, wenn ein Überprüfungs Tester versucht, ein Album zu kaufen, aber nur über ausreichende Gutschriften zum Erwerb eines einzelnen Titels verfügt.
4.  Wenn Sie ActiveX-Steuerelemente innerhalb der Dienst Seiten verwenden, stellen Sie sicher, dass Sie ordnungsgemäß installiert und deinstalliert werden, und zwar beide auf allen anwendbaren Versionen von Windows. Wenn dies nicht der Fall ist, ist dies ein typisches Problem. Häufig sind die ActiveX-Steuerelemente für die Entwickler und Tester in einem Online Shop auf Ihren eigenen Computern registriert, aber vergessen Sie nicht, die Steuerelemente auf dem Computer des Benutzers zu installieren.

    Wenn Ihr Speicher ein Plug-in oder ein ActiveX-Steuerelement installiert, müssen Sie dem Benutzer eine einfache Möglichkeit zur Deinstallation bereitstellen. Beispielsweise hat Microsoft kürzlich festgestellt, dass einige Online-ActiveX-Steuerelemente in Windows Media Player 11 für Windows Vista gespeichert haben, die nicht über das Menü "Software" entfernt werden konnten. Nach einiger Untersuchung stellte Microsoft fest, dass die ActiveX-Steuerelemente über den Add-on-Manager in Internet Explorer entfernt werden konnten. Es ist wichtig, dass Sie (zumindest über eine Hilfedatei) die Methode zum Installieren und Deinstallieren von ActiveX-Steuerelementen und Plug-ins miteinander kommunizieren.

    Weitere Informationen zur Integration Ihres Stores in die Sicherheitsinfrastruktur in Windows Vista finden Sie im Artikel ["bewährte Methoden für Entwickler und Richtlinien für Anwendungen in einer Umgebung mit geringsten Rechten"](/previous-versions/aa905330(v=msdn.10)).

 

 