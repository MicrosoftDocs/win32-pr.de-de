---
title: Bluetooth Rückrufe
description: Die Bluetooth Rückruffunktionen in diesem Abschnitt werden in Kombination mit Funktionen verwendet, die es ermöglichen, Bluetooth Und-Dienste zu verwalten.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad822a0c7af4b0bbc5d649919bda638776014dfe7e8195ed1f45bb99032c6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588360"
---
# <a name="bluetooth-callbacks"></a>Bluetooth Rückrufe

Die Bluetooth Rückruffunktionen in diesem Abschnitt werden in Kombination mit Funktionen verwendet, die es ermöglichen, Bluetooth Und-Dienste zu verwalten.

Bluetooth wird auch mithilfe der Windows Sockets-Programmierschnittstelle unterstützt. Weitere Informationen zum Programmieren von Bluetooth mithilfe der Windows Sockets-Schnittstelle finden Sie unter Windows [Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).



| `Section`                                                                                      | Content                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ PFN-AUTHENTIFIZIERUNGSRÜCKRUF**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Wird in Verbindung mit der [**BluetoothRegisterForAuthentication-Funktion**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) verwendet.                                                  |
| [**\_ \_ PFN-AUTHENTIFIZIERUNGSRÜCKRUF \_ EX**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Wird in Verbindung mit der [**BluetoothRegisterForAuthenticationEx-Funktion**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) verwendet.                                              |
| [**RÜCKRUF VON \_ PFN-BLUETOOTH-ENUM-ATTRIBUTEN \_ \_ \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Wird einmal für jedes Attribut im *pSDPStream-Parameter* aufgerufen, das an den [**Funktionsaufruf BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) übergeben wird. |
| [**\_ \_ PFN-GERÄTERÜCKRUF**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Wird in Verbindung mit der Auswahl Bluetooth verwendet.                                                                                                                    |



 

 

 




