---
title: Informationen zu Bluetooth
description: Bluetooth ist ein Industriestandard Protokoll, das drahtlose Konnektivität für eine Vielzahl von Geräten ermöglicht, einschließlich Computern, Druckern, Mobiltelefonen und Hand Held Geräten.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, beschrieben
- Bluetooth Bluetooth, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038603"
---
# <a name="about-bluetooth"></a>Informationen zu Bluetooth

Bluetooth ist ein Industriestandard Protokoll, das drahtlose Konnektivität für eine Vielzahl von Geräten ermöglicht, einschließlich Computern, Druckern, Mobiltelefonen und Hand Held Geräten.

Zu den wichtigsten Bluetooth-Features gehören:

-   Kostengünstiger drahtlos Protokoll mit geringem Energieverbrauch mit Industriestandard-Unterstützung und weltweiten Akzeptanz.
-   Eine definierte und vertraute Programmierschnittstelle, mit der Entwickler Anwendungen schnell entwickeln oder portieren können.
-   Eine offizielle Website und eine branchenweite kooperative Organisation, in der Bluetooth-Technologie erläutert, herauf gestuft und standardisiert wird. Weitere Informationen finden Sie unter [www.Bluetooth.com](https://www.bluetooth.com/).

Bluetooth unter Windows bietet Kerndienste, die mit den von Transmission Control Protocol (TCP/IP) verfügbar gemachten Diensten vergleichbar sind. Wie viele Netzwerkprotokolle und-Dienste werden Bluetooth-Konnektivität und Datenübertragung mithilfe von Windows Sockets-Funktionsaufrufen programmiert, wobei gängige Windows Sockets-Programmiertechniken und bestimmte Bluetooth-Erweiterungen verwendet werden. Da jedoch bedeutende Unterschiede zwischen einem verkabelten, einem Netzwerk und einem drahtlosen Ad-hoc-Netzwerk bestehen, bietet Bluetooth Erweiterungen wie die Dienst-/gerätermittlung und die Benachrichtigung, mit deren Hilfe Anwendungen in der drahtlos Umgebung ordnungsgemäß ausgeführt werden können. Diese Erweiterungen haben auch die Möglichkeit, eine einfache Portierung auf ähnliche Technologien wie z. b. UNDA oder zukünftige drahtlose Transporte zu portieren.

Microsoft bietet Unterstützung für Bluetooth unter Windows XP mit Service Pack 1 (SP1) und höher, unter Windows XP Embedded mit Service Pack 2 und auf Windows CE. Bluetooth-Anwendungen, die unter Windows XP ausgeführt werden, sollten in einem Windows XP Embedded-basierten Lauf Zeit Abbild ausgeführt werden können, das die erforderlichen Abhängigkeiten enthält. Weitere Informationen zu Windows XP Embedded finden Sie in der Hilfe Dokumentation zu Windows XP Embedded auf MSDN. Weitere Informationen zur Windows CE Programmierung finden Sie im Windows CE SDK.

Microsoft bietet zwei Ansätze zum Programmieren von Bluetooth unter Windows:

-   Verwenden der Windows Sockets-Schnittstelle
-   Direktes Verwalten von Geräten mithilfe von nicht-Socket-Bluetooth-Schnittstellen

In diesem Abschnitt finden Sie eine Übersicht über diese beiden Ansätze in den folgenden Themen. Weitere Informationen zum Verwenden der Windows Sockets-API-Elemente zum Programmieren von Bluetooth finden Sie unter [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).



| `Section`                                                                                | Inhalt                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Windows Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md)     | Beschreibt die Beziehung zwischen Bluetooth und Windows Sockets. |
| [Verwalten von Bluetooth-Geräten und-Diensten](managing-bluetooth-devices-and-services.md) | Hier wird beschrieben, wie Bluetooth-Geräte und-Dienste verwaltet werden.           |



 

 

 




