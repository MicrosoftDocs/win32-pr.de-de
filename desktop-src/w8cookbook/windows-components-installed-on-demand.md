---
title: Bedarfs gesteuerte Installation von Windows-Komponenten
description: Bedarfs gesteuerte Installation von Windows-Komponenten
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039738"
---
# <a name="windows-components-installed-on-demand"></a>Bedarfs gesteuerte Installation von Windows-Komponenten

## <a name="platform"></a>Plattform

**Clients:** Windows 8.1  







## <a name="description"></a>BESCHREIBUNG

Zwei Windows-Komponenten werden Bedarfs gesteuert in Windows 8.1 installiert: DirectPlay und ntvdm. Diese Komponenten werden in optionalen Komponenten unter dem Knoten "Legacy Komponenten" aufgeführt. Diese Komponenten werden lokal als Teil des Betriebssystems installiert und als optionale Komponenten komprimiert. Wenn eine APP auf eine dieser Komponenten verweist oder diese aufruft (in der Regel beim ersten Start der APP), wird die Installation automatisch ausgelöst. Benutzer werden benachrichtigt, dass die Komponente installiert wird, und Sie müssen die Aktion bestätigen, um den Vorgang fortzusetzen. Eine Erhöhung ist erforderlich, damit dies erfolgreich ist, wenn der Benutzer kein Administrator ist. Nach der Erstinstallation muss der Benutzer keine weiteren Aktionen ausführen, um die Komponente erneut zu verwenden.

## <a name="manifestation"></a>Ausstrahlung

Wenn eine APP auf eine Legacy Komponente in optionalen Komponenten (beim ersten Start) verweist oder diese aufruft, wird die APP angehalten, und das Dialogfeld für die Bedarfs gesteuerte Funktion wird geöffnet, und die Benutzer Berechtigung zum Installieren der Komponente wird angefordert. Wenn Benutzer auf OK klicken, wird möglicherweise auch eine Eingabeaufforderung für erhöhte Rechte angezeigt, in der Sie Ihre Anmelde Informationen eingeben müssen. Die Komponente wird dann installiert, und die APP wird fortgesetzt.

## <a name="mitigation"></a>Minderung

Um das Öffnen der Features für die Bedarfs gesteuerte Benutzeroberfläche zu gewährleisten, können Sie DirectPlay und NTVDM mithilfe von "dismus" oder der optionalen Komponenten-Benutzeroberfläche vorinstallieren.

## <a name="solution"></a>Lösung

Es wird dringend empfohlen, dass Sie in zukünftigen Versionen Ihrer APP nicht auf Komponenten verweisen oder diese aufrufen, die als optionale Legacy Komponenten in Windows aufgeführt sind. Optionale Legacy Komponenten enthalten nur ältere, weniger genutzte Komponenten, die möglicherweise Leistungs-und Sicherheitsprobleme für Benutzer verursachen.

## <a name="tests"></a>Tests

Aus Kompatibilitätsgründen sind keine weiteren Test Unterkünfte erforderlich. Beachten Sie, dass dieses Dialogfeld angezeigt wird, wenn die optionale Komponente aufgerufen wird oder referenziert wird. diese Installation erfordert eine Erhöhung der Rechte.

 

 




