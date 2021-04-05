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
# <a name="bluetooth-callbacks"></a><span data-ttu-id="a19e9-103">Bluetooth-Rückrufe</span><span class="sxs-lookup"><span data-stu-id="a19e9-103">Bluetooth Callbacks</span></span>

<span data-ttu-id="a19e9-104">Die Bluetooth-Rückruf Funktionen in diesem Abschnitt werden in Kombination mit Funktionen verwendet, die das Verwalten von Bluetooth-Geräten und-Diensten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a19e9-104">The Bluetooth callback functions in this section are used in combination with functions that make it possible to manage Bluetooth devices and services.</span></span>

<span data-ttu-id="a19e9-105">Bluetooth wird auch durch die Verwendung der Windows Sockets-Programmierschnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a19e9-105">Bluetooth is also supported by using the Windows Sockets programming interface.</span></span> <span data-ttu-id="a19e9-106">Weitere Informationen zum Programmieren von Bluetooth mithilfe der Windows Sockets-Schnittstelle finden Sie [unter Windows Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="a19e9-106">For more information about programming Bluetooth by using the Windows Sockets interface, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>



| <span data-ttu-id="a19e9-107">`Section`</span><span class="sxs-lookup"><span data-stu-id="a19e9-107">Section</span></span>                                                                                      | <span data-ttu-id="a19e9-108">Inhalt</span><span class="sxs-lookup"><span data-stu-id="a19e9-108">Content</span></span>                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a19e9-109">**PFN- \_ Authentifizierungs \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="a19e9-109">**PFN\_AUTHENTICATION\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | <span data-ttu-id="a19e9-110">Wird in Verbindung mit der [**bluetoothregisterforauthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="a19e9-110">Used in conjunction with the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function.</span></span>                                                  |
| [<span data-ttu-id="a19e9-111">**PFN- \_ Authentifizierungs \_ Rückruf ( \_ Ex)**</span><span class="sxs-lookup"><span data-stu-id="a19e9-111">**PFN\_AUTHENTICATION\_CALLBACK\_EX**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | <span data-ttu-id="a19e9-112">Wird in Verbindung mit der [**bluetoothregisterforauthenticationex**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="a19e9-112">Used in conjunction with the [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) function.</span></span>                                              |
| [<span data-ttu-id="a19e9-113">**Rückruf der PFN-Bluetooth-Aufzählungs \_ \_ \_ Attribute \_**</span><span class="sxs-lookup"><span data-stu-id="a19e9-113">**PFN\_BLUETOOTH\_ENUM\_ATTRIBUTES\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | <span data-ttu-id="a19e9-114">Wird einmal für jedes Attribut aufgerufen, das im *psdpstream* -Parameter enthalten ist, der an den [**bluetoothsdpumattribute**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) -Funktionsaufruf übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a19e9-114">Called once for each attribute found in the *pSDPStream* parameter that is passed to the [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) function call.</span></span> |
| [<span data-ttu-id="a19e9-115">**PFN- \_ Geräte \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="a19e9-115">**PFN\_DEVICE\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | <span data-ttu-id="a19e9-116">Wird in Verbindung mit der Auswahl von Bluetooth-Geräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="a19e9-116">Used in association with selecting Bluetooth devices.</span></span>                                                                                                                    |



 

 

 




