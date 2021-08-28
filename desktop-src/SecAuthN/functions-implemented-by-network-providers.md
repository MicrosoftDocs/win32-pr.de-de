---
description: Die folgenden Funktionen werden von einer Netzwerkanbieter-DLL implementiert, um mit dem Multiple Provider Router (MPR) zu kommunizieren.
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Von Netzwerkanbietern implementierte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892bcb5c19f54e5de667eb72119f6b9e5fc9b183b8d5038ce37b7e556ae5d3a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016320"
---
# <a name="functions-implemented-by-network-providers"></a>Von Netzwerkanbietern implementierte Funktionen

Die folgenden Funktionen werden von einer Netzwerkanbieter-DLL implementiert, um mit dem [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) zu kommunizieren. Beachten Sie, dass nur die [Funktionenfunktionen](capabilities-functions.md) von einem Netzwerkanbieter implementiert werden müssen. Die Implementierung der anderen Funktionstypen ist optional und hängt von den Anforderungen des Netzwerkanbieters ab.



| Funktionssatz                                                                                    | BESCHREIBUNG                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funktionenfunktionen](capabilities-functions.md)<br/>                                 | Ermöglicht dem Aufrufer, die Funktionen des Netzwerkanbieters zu bestimmen.<br/>                                                                |
| [Benutzernamenfunktionen](user-name-functions.md)<br/>                                       | Fordert den Netzwerkanbieter zur Eingabe des Benutzernamens auf, der einer Verbindung zugeordnet ist.<br/>                                                            |
| [Geräteumleitungsfunktionen](device-redirecting-functions.md)<br/>                     | Ermöglicht einem Netzwerkanbieter das Umleiten von Geräten, Laufwerkbuchstaben und LPT-Ports, die auf dem Microsoft MS-DOS-Betriebssystem standard sind.<br/> |
| [Anbieterspezifische Dialogfeldfunktionen](provider-specific-dialog-box-functions.md)<br/> | Ermöglicht es einem Netzwerkanbieter, netzwerkspezifische Informationen anzuzeigen oder darauf zu reagieren.<br/>                                                            |
| [Administrative Funktionen](administrative-functions.md)<br/>                             | Ermöglicht es einem Netzwerkanbieter, spezielle Netzwerkverzeichnisse anzuzeigen oder darauf zu reagieren.<br/>                                                             |
| [Enumerationsfunktionen](enumeration-functions.md)<br/>                                   | Ermöglicht dem Benutzer das Durchsuchen von Netzwerkressourcen.<br/>                                                                                            |



 

Weitere Informationen zum Erstellen und Registrieren eines Netzwerkanbieters finden Sie unter [Implementieren eines Netzwerkanbieters](implementing-a-network-provider.md) und [Registrieren von Netzwerkanbietern und Anmeldeinformations-Managern.](registering-network-providers-and-credential-managers.md)

 

