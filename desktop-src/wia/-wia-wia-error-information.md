---
description: Die APIs für die Windows-Abbild Beschaffung (WIA) geben ihren Abschluss Status in einem HRESULT-Rückgabewert zurück.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: WIA-Fehlerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348414"
---
# <a name="wia-error-information"></a><span data-ttu-id="7baa3-103">WIA-Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="7baa3-103">WIA Error Information</span></span>

<span data-ttu-id="7baa3-104">Die APIs für die Windows-Abbild Beschaffung (WIA) geben ihren Abschluss Status in einem HRESULT-Rückgabewert zurück.</span><span class="sxs-lookup"><span data-stu-id="7baa3-104">The Windows Image Acquisition (WIA)APIs return their completion status in an HRESULT return value.</span></span> <span data-ttu-id="7baa3-105">Anwendungen überprüfen diese Rückgabewerte anhand der Funktion " \_ WIA", um zu bestimmen, ob für den Fehler ein Benutzereingriff erforderlich ist, z. b. ein Papierstau-Papierpfad, und Berichte an den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7baa3-105">Applications check these return values against the FACILITY\_WIA constant to determine whether the error requires user intervention to clear, such as a jammed paper path, and report them to the user.</span></span> <span data-ttu-id="7baa3-106">Außerdem werden alle Fehler auf Treiber Ebene im Ereignisprotokoll unter Verwendung von Fehler Zeichenfolgen, die vom Geräte-Mini Treiber bereitgestellt werden, ausführlich protokolliert.</span><span class="sxs-lookup"><span data-stu-id="7baa3-106">In addition, all driver-level errors are logged in detail to the event log, using error strings provided by the device minidriver.</span></span> <span data-ttu-id="7baa3-107">Eine Auflistung der WIA-spezifischen Fehlercodes finden Sie unter [Fehlercodes](-wia-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7baa3-107">For a listing of WIA-specific error codes, see [Error Codes](-wia-error-codes.md).</span></span>

 

 



