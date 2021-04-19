---
description: Die seriellen Geräte auf einem virtuellen Computer bestehen aus seriellen Controllern und seriellen Anschlüssen. Jeder virtuelle Computer verfügt über genau einen seriellen Controller, und jeder serielle Controller verfügt über genau zwei serielle Anschlüsse.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Serielle Geräteklassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360629"
---
# <a name="serial-devices-classes"></a><span data-ttu-id="92c4e-104">Serielle Geräteklassen</span><span class="sxs-lookup"><span data-stu-id="92c4e-104">Serial devices classes</span></span>

<span data-ttu-id="92c4e-105">Die seriellen Geräte auf einem virtuellen Computer bestehen aus seriellen Controllern und seriellen Anschlüssen.</span><span class="sxs-lookup"><span data-stu-id="92c4e-105">The serial devices in a virtual machine consist of serial controllers and serial ports.</span></span> <span data-ttu-id="92c4e-106">Jeder virtuelle Computer verfügt über genau einen seriellen Controller, und jeder serielle Controller verfügt über genau zwei serielle Anschlüsse.</span><span class="sxs-lookup"><span data-stu-id="92c4e-106">Each virtual machine has exactly one serial controller, and each serial controller has exactly two serial ports.</span></span>

<span data-ttu-id="92c4e-107">Die Einstellungen für den seriellen Controller sind nicht konfigurierbar. Daher ist keine Einstellungsdaten Instanz zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="92c4e-107">The settings for the serial controller are not configurable; therefore, there is no setting data instance associated with it.</span></span> <span data-ttu-id="92c4e-108">Außerdem ist es nicht möglich, serielle Controller oder serielle Anschlüsse von einem virtuellen Computer hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="92c4e-108">Also, you cannot add or remove serial controllers or serial ports from a virtual machine.</span></span> <span data-ttu-id="92c4e-109">Daher sind keine Ressourcenpool Instanzen für serielle Geräte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="92c4e-109">Therefore, there are no resource pool instances for serial devices.</span></span>

<span data-ttu-id="92c4e-110">Im folgenden finden Sie virtualisierungswmi-Klassen, die mit seriellen Geräten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="92c4e-110">The following are virtualization WMI classes related to serial devices.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="92c4e-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="92c4e-111">In this section</span></span>



| <span data-ttu-id="92c4e-112">Thema</span><span class="sxs-lookup"><span data-stu-id="92c4e-112">Topic</span></span>                                                                                      | <span data-ttu-id="92c4e-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92c4e-113">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="92c4e-114">**MSVM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="92c4e-114">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)<br/>                         | <span data-ttu-id="92c4e-115">Stellt die Funktionen und die Verwaltung des seriellen Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="92c4e-115">Represents the capabilities and management of the serial controller.</span></span><br/> |
| [<span data-ttu-id="92c4e-116">**MSVM- \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="92c4e-116">**Msvm\_SerialPort**</span></span>](msvm-serialport.md)<br/>                                     | <span data-ttu-id="92c4e-117">Stellt einen seriellen Anschluss dar, der dem seriellen Controller zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92c4e-117">Represents a serial port associated with the serial controller.</span></span><br/>      |
| [<span data-ttu-id="92c4e-118">**MSVM \_ serialportonserialcontroller**</span><span class="sxs-lookup"><span data-stu-id="92c4e-118">**Msvm\_SerialPortOnSerialController**</span></span>](msvm-serialportonserialcontroller.md)<br/> | <span data-ttu-id="92c4e-119">Ordnet einen seriellen Anschluss einem seriellen Controller zu.</span><span class="sxs-lookup"><span data-stu-id="92c4e-119">Associates a serial port with a serial controller.</span></span><br/>                   |



 

 

 




