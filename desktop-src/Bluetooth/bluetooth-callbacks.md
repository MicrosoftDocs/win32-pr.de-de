---
title: Bluetooth-Rückrufe
description: Die Bluetooth-Rückruf Funktionen in diesem Abschnitt werden in Kombination mit Funktionen verwendet, die das Verwalten von Bluetooth-Geräten und-Diensten ermöglichen.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708112"
---
# <a name="bluetooth-callbacks"></a>Bluetooth-Rückrufe

Die Bluetooth-Rückruf Funktionen in diesem Abschnitt werden in Kombination mit Funktionen verwendet, die das Verwalten von Bluetooth-Geräten und-Diensten ermöglichen.

Bluetooth wird auch durch die Verwendung der Windows Sockets-Programmierschnittstelle unterstützt. Weitere Informationen zum Programmieren von Bluetooth mithilfe der Windows Sockets-Schnittstelle finden Sie [unter Windows Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).



| `Section`                                                                                      | Inhalt                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFN- \_ Authentifizierungs \_ Rückruf**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Wird in Verbindung mit der [**bluetoothregisterforauthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) -Funktion verwendet.                                                  |
| [**PFN- \_ Authentifizierungs \_ Rückruf ( \_ Ex)**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Wird in Verbindung mit der [**bluetoothregisterforauthenticationex**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) -Funktion verwendet.                                              |
| [**Rückruf der PFN-Bluetooth-Aufzählungs \_ \_ \_ Attribute \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Wird einmal für jedes Attribut aufgerufen, das im *psdpstream* -Parameter enthalten ist, der an den [**bluetoothsdpumattribute**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) -Funktionsaufruf übergeben wird. |
| [**PFN- \_ Geräte \_ Rückruf**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Wird in Verbindung mit der Auswahl von Bluetooth-Geräten verwendet.                                                                                                                    |



 

 

 




