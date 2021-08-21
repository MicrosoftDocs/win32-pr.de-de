---
title: Windows bei Bedarf installierte Komponenten
description: Windows bei Bedarf installierte Komponenten
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765768d2e16005ca0a465b53f076c64c6a30f31b8739113954ccc11959c8e0c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028798"
---
# <a name="windows-components-installed-on-demand"></a>Windows bei Bedarf installierte Komponenten

## <a name="platform"></a>Plattform

**Clients –** Windows 8.1  







## <a name="description"></a>BESCHREIBUNG

Zwei Windows-Komponenten werden bei Bedarf in Windows 8.1 installiert: DirectPlay und NTVDM. Diese Komponenten sind unter optionale Komponenten unter dem Knoten "Legacykomponenten" aufgeführt. Diese Komponenten werden lokal als Teil des Betriebssystems installiert und als optionale Komponenten komprimiert. Wenn eine App auf eine dieser Komponenten verweist oder diese aufruft (in der Regel beim ersten Start der App), wird die Installation automatisch ausgelöst. Benutzer werden benachrichtigt, dass die Komponente installiert wird, und sie müssen die Aktion bestätigen, um fortfahren zu können. Eine Erhöhung der Rechte ist erforderlich, damit dies erfolgreich ist, wenn der Benutzer kein Administrator ist. Nach der Erstinstallation muss der Benutzer keine weiteren Aktionen ausführen, um die Komponente erneut zu verwenden.

## <a name="manifestation"></a>Manifestation

Wenn eine App auf eine Legacykomponente in optionalen Komponenten verweist oder aufruft (beim ersten Start), wird die App angehalten, und das Dialogfeld Feature on Demand wird geöffnet, und der Benutzer fordert die Berechtigung zum Installieren der Komponente an. Wenn Benutzer auf OK klicken, wird möglicherweise auch eine Eingabeaufforderung für rechte Rechte angezeigt, in der sie ihre Anmeldeinformationen eingeben müssen. Die Komponente wird dann installiert, und die App wird fortgesetzt.

## <a name="mitigation"></a>Minderung

Damit die Benutzeroberfläche "Features bei Bedarf" nicht geöffnet wird, können Sie DirectPlay und NTVDM mithilfe von DISM oder der Benutzeroberfläche für optionale Komponenten vorinstallieren.

## <a name="solution"></a>Lösung

Es wird dringend empfohlen, in zukünftigen Versionen Ihrer App nicht auf Komponenten zu verweisen oder diese auf diese zu verweisen, die in Windows als Legacy Optional Components aufgeführt wurden. Ältere optionale Komponenten enthalten nur ältere, weniger verwendete Komponenten, die möglicherweise Leistungs- und Sicherheitsprobleme für Benutzer verursachen können.

## <a name="tests"></a>Tests

Aus Kompatibilitäts-Grund sind keine zusätzlichen Testumgebungen erforderlich. Es ist wichtig zu beachten, dass dieses Dialogfeld angezeigt wird, wenn die optionale Komponente aufgerufen oder referenziert wird und diese Installation eine Erhöhung erfordert.

 

 




