---
title: Verwenden Bluetooth
description: In diesem Abschnitt werden Aufgaben beschrieben, die sich auf das Schreiben Windows-basierten Anwendungen für Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80d57d12b2594ab5bbaeb5ad5d026552ab180ae409ba81446288ac396c746a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701830"
---
# <a name="using-bluetooth"></a>Verwenden Bluetooth

In diesem Abschnitt werden Aufgaben beschrieben, die sich auf das Schreiben Windows-basierten Anwendungen für Bluetooth.

Bluetooth bietet Programmierdefinitionen in den Dateien Ws2bth.h und BluetoothAPIs.h. Die Datei Bthsdpdef.h muss vor BluetoothAPIs.h enthalten sein. Die Datei "Ws2bth.h" muss nach "Winsock2.h" enthalten sein, um Bluetooth verwenden zu können. Verknüpfen Sie nur mit Bthprops.lib, und vermeiden Sie die Verknüpfung mit Irprops.lib. Irprops.lib wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Bthprops.lib ist im Windows Vista SDK verfügbar. Sie können das Windows Vista SDK verwenden, um Anwendungen für Windows XP mit Service Pack 2 (SP2) zu entwickeln. Das Windows Vista SDK ist im [Download Center verfügbar.](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe)

Alle synchronen und überlappenden Standardmechanismen zum Lesen und Schreiben von Daten, die derzeit mit anderen Adressfamilien unterstützt werden, funktionieren auch ordnungsgemäß mit der \_ AF-BTH-Adressfamilie.

Im SDK ist ein Beispielcode enthalten, der eine einfache Bluetooth mit winsock 2.2 und dem RFCOMM-Protokoll zeigt. Den Quellcode für das Beispiel finden Sie im SDK-Installationsspeicherort unter C: Programme \\ \\ Microsoft SDKs Windows Samples \\ \\ <version number> \\ \\ NetDs \\ winsock \\ Bluetooth.

In diesem Abschnitt werden die folgenden Themen beschrieben.



| `Section`                                                                                      | Inhalt                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Bluetooth Programmieren mit Windows Sockets](bluetooth-programming-with-windows-sockets.md) | Erläutert die Verwendung Windows Sockets-Schnittstellen zum Implementieren eines Bluetooth Netzwerks. |



 

 

 




