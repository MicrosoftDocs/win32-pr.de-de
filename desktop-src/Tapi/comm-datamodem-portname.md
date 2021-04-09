---
description: Die Geräteklasse "comm/DataModem/Portname" besteht aus den Gerätenamen, an die Modems angefügt werden.
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: comm/DataModem/Portname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866920"
---
# <a name="commdatamodemportname"></a><span data-ttu-id="68f9a-103">comm/DataModem/Portname</span><span class="sxs-lookup"><span data-stu-id="68f9a-103">comm/datamodem/portname</span></span>

<span data-ttu-id="68f9a-104">Die Geräteklasse "comm/DataModem/Portname" besteht aus den Gerätenamen, an die Modems angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="68f9a-104">The comm/datamodem/portname device class consists of the device names to which modems are attached.</span></span> <span data-ttu-id="68f9a-105">Wenn dieser Gerätename in einem Aufrufen der [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion angegeben wird, füllt die Funktion die [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur mit einer null-terminierten ANSI-Zeichenfolge (nicht Unicode) aus, die den Namen des Ports angibt, an den das angegebene Modem angefügt ist, z. b. "COM1 \\ 0".</span><span class="sxs-lookup"><span data-stu-id="68f9a-105">When this device name is specified in a call to the [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function, the function fills the [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure with a null-terminated ANSI (not Unicode) string specifying the name of the port to which the specified modem is attached, such as "COM1\\0".</span></span> <span data-ttu-id="68f9a-106">Dies dient primär zur Identifizierung in der Benutzeroberfläche, kann aber unter bestimmten Umständen verwendet werden, um das Gerät direkt zu öffnen, wobei der Dienstanbieter umgangen wird (wenn der Dienstanbieter das Gerät nicht bereits geöffnet hat).</span><span class="sxs-lookup"><span data-stu-id="68f9a-106">This is intended primarily for identification purposes in the user interface, but could be used under some circumstances to open the device directly, bypassing the service provider (if the service provider does not already have the device open itself).</span></span> <span data-ttu-id="68f9a-107">Wenn dem Gerät kein Port zugeordnet ist, wird eine NULL-Zeichenfolge (" \\ 0") in der **varstring** -Struktur (mit einer Zeichen folgen Länge von 1) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68f9a-107">If there is no port associated with the device, a null string ("\\0") is returned in the **VARSTRING** structure (with a string length of 1).</span></span>

 

 



