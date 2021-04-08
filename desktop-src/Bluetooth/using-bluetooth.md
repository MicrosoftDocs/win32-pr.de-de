---
title: Verwenden von Bluetooth
description: In diesem Abschnitt werden Aufgaben beschrieben, die sich auf das Schreiben von Windows-basierten Anwendungen für Bluetooth beziehen.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734529"
---
# <a name="using-bluetooth"></a>Verwenden von Bluetooth

In diesem Abschnitt werden Aufgaben beschrieben, die sich auf das Schreiben von Windows-basierten Anwendungen für Bluetooth beziehen.

Bluetooth stellt Programmier Definitionen in den Dateien Ws2bth. h und bluetoothapis. h bereit. Die Datei bthsdpdef. h muss vor bluetoothapis. h enthalten sein. Die Datei Ws2bth. h muss nach Winsock2. h eingeschlossen werden, damit Bluetooth-Sockets verwendet werden können. Verknüpfen Sie nur mit bthrequi. lib, und vermeiden Sie das Verknüpfen mit "unrequi. lib". "Uncompatibility. lib" wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Bthrequi. lib ist im Windows Vista SDK verfügbar. Sie können das Windows Vista SDK zum Entwickeln von Anwendungen für Windows XP mit Service Pack 2 (SP2) verwenden. Das Windows Vista SDK ist im [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe)verfügbar.

Alle standardmäßigen synchronen und überlappenden Mechanismen zum Lesen und Schreiben von Daten, die derzeit mit anderen Adressfamilien unterstützt werden, funktionieren ebenfalls ordnungsgemäß mit der AF- \_ BTH-Adressfamilie.

Im SDK ist ein Beispielcode enthalten, der eine einfache Bluetooth-Anwendung mit dem Winsock 2,2-und RFCOMM-Protokoll anzeigt. Den Quellcode für das Beispiel finden Sie im SDK-Installationsverzeichnis unter C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ <version number> \\ Samples \\ netds \\ Winsock \\ Bluetooth.

In diesem Abschnitt werden die folgenden Themen beschrieben.



| `Section`                                                                                      | Inhalt                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Bluetooth-Programmierung mit Windows Sockets](bluetooth-programming-with-windows-sockets.md) | Erläutert die Verwendung von Windows Sockets-Schnittstellen zum Implementieren eines Bluetooth-Netzwerks. |



 

 

 




