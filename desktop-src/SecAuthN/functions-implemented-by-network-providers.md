---
description: Die folgenden Funktionen werden von einer Netzwerkanbieter-dll implementiert, um mit dem MultiProvider-Router (MPR) zu kommunizieren.
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Von Netzwerkanbietern implementierte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960548"
---
# <a name="functions-implemented-by-network-providers"></a>Von Netzwerkanbietern implementierte Funktionen

Die folgenden Funktionen werden von einer Netzwerkanbieter-dll implementiert, um mit dem [*MultiProvider-Router*](/windows/desktop/SecGloss/m-gly) (MPR) zu kommunizieren. Beachten Sie, dass nur die Funktionen [Funktionen](capabilities-functions.md) von einem Netzwerkanbieter implementiert werden müssen. Die Implementierung der anderen Arten von Funktionen ist optional und hängt von den Anforderungen des Netzwerk Anbieters ab.



| Funktions Satz                                                                                    | BESCHREIBUNG                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funktionen-Funktionen](capabilities-functions.md)<br/>                                 | Ermöglicht dem Aufrufer, die Funktionen des Netzwerk Anbieters zu bestimmen.<br/>                                                                |
| [Benutzernamen Funktionen](user-name-functions.md)<br/>                                       | Fordert den Netzwerkanbieter zum Benutzernamen an, der einer Verbindung zugeordnet ist.<br/>                                                            |
| [Funktionen zum Umleiten von Geräten](device-redirecting-functions.md)<br/>                     | Ermöglicht einem Netzwerkanbieter das Umleiten von Geräten, Laufwerk Buchstaben und LPT-Ports, die auf dem Microsoft MS-DOS-Betriebssystem standardmäßig sind.<br/> |
| [Anbieterspezifische Dialog Feld Funktionen](provider-specific-dialog-box-functions.md)<br/> | Ermöglicht es einem Netzwerkanbieter, Netzwerk spezifische Informationen anzuzeigen oder darauf zu reagieren.<br/>                                                            |
| [Verwaltungsfunktionen](administrative-functions.md)<br/>                             | Ermöglicht es einem Netzwerkanbieter, spezielle Netzwerk Verzeichnisse anzuzeigen oder darauf zu reagieren.<br/>                                                             |
| [Enumerationsfunktionen](enumeration-functions.md)<br/>                                   | Ermöglicht dem Benutzer das Durchsuchen von Netzwerkressourcen.<br/>                                                                                            |



 

Weitere Informationen zum Erstellen und Registrieren eines Netzwerk Anbieters finden Sie unter [Implementieren eines Netzwerk Anbieters](implementing-a-network-provider.md) und Registrieren von [Netzwerkanbietern und Anmelde Informations Managern](registering-network-providers-and-credential-managers.md).

 

