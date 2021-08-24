---
title: Häufige Onboardingprobleme für Online Musik Stores
description: Häufige Onboardingprobleme für Online Musik Stores
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Windows Media Player Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c4cb38f088f463d6bea8ca15b3a92cea9610cc8541f27d55c48df07f9286d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763960"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>Häufige Onboardingprobleme für Online Musik Stores

Im Folgenden finden Sie eine Liste der allgemeinen Windows Media Player Onboardingprobleme, die Sie vermeiden sollten. Jedes dieser Probleme kann dazu führen, dass Ihr Speicher bei Validierungstests fehlschlägt. Wenn der RC2-Durchlauf fehlschlägt, wird der Start auf das nächste verfügbare Startfenster verschoben.

1.  Fehler beim Übergang von Testservern zu Produktionsservern
    -   Fehlende Seiten
    -   IIS-Einstellungen (Access, VRoots, HTTPS oder andere Sicherheitseinstellungen)
    -   Testkonten funktionieren nicht mehr.
    -   Für Testkonten wird kein Guthaben angewendet.
    -   Vom Dienst gehostete Logos werden nicht verschoben.
    -   IP-Einschränkungen, die zuvor umgegangen sind, treten erneut auf. Insbesondere für E-Commerce-Systeme gelten möglicherweise andere Einschränkungen als für die Musikwebsite.
    -   Das ServiceInfo-Dokument wird nicht aktualisiert, um auf die Produktion zu verweisen.
2.  Der Link Kaufen (oder Shoplink) im Bereich Jetzt wiedergeben ist ungültig. Dies ist ein häufig übersehenes Problem, das dazu führt, dass Ihr Speicher fehlschlägt, auch wenn alles andere funktioniert.
3.  Die Tester von Microsoft müssen über ausreichende Einkaufsleistung verfügen. Das Überprüfungsteam von Microsoft durchläuft mehrere Kaufszenarien, die von kleinen Käufen bis hin zu sehr großen Käufen reichen. Sie müssen ihnen eine angemessene Möglichkeit bieten, als Verbraucher in Ihrem Geschäft zu fungieren. Dies kann von der Bereitstellung einer Vielzahl von Konten bis hin zur Bereitstellung einer Dummy-Kreditkarte reichen. Beispielsweise schlägt ein Store in RC2 fehl, wenn ein Validierungstester versucht, ein Album zu kaufen, aber nur über genügend Guthaben verfügt, um eine einzelne Spur zu kaufen.
4.  Wenn Sie ActiveX-Steuerelemente auf Ihren Dienstseiten verwenden, stellen Sie sicher, dass sie auf allen anwendbaren Versionen von Windows korrekt installiert und deinstalliert werden. Dies ist ein typisches Problem. Die Entwickler und Tester in einem Onlineshop haben häufig die ActiveX-Steuerelemente auf ihren eigenen Computern registriert, vergessen jedoch, die Steuerelemente auf dem Computer des Benutzers zu installieren.

    Wenn Ihr Speicher ein Plug-In oder ein ActiveX-Steuerelement installiert, müssen Sie dem Benutzer eine einfache Möglichkeit zur Deinstallation bereitstellen. Beispielsweise hat Microsoft kürzlich festgestellt, dass einige Onlineshops ActiveX-Steuerelementen in Windows Media Player 11 für Windows Vista installiert sind, die nicht über das Menü Programme hinzufügen/entfernen entfernt werden konnten. Nach einer Untersuchung hat Microsoft festgestellt, dass die ActiveX Steuerelemente über den Add-On-Manager in Internet Explorer entfernt werden konnten. Es ist wichtig, dass Sie (zumindest über eine Hilfedatei) über die Installation und Deinstallation ActiveX Steuerelemente und Plug-Ins kommunizieren.

    Weitere Informationen zum Integrieren Ihres Geschäfts in die Sicherheitsinfrastruktur in Windows Vista finden Sie im Artikel ["Best Practices und Richtlinien für Entwickler für Anwendungen in einer Umgebung mit den geringsten Berechtigungen".](/previous-versions/aa905330(v=msdn.10))

 

 