---
title: Puffer Längen der Netzwerk Verwaltungsfunktion
description: In diesem Thema werden die Anforderungen für Funktions Puffer Längen bei der Verwendung mit den Netzwerkverwaltungs-APIs erörtert.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856232"
---
# <a name="network-management-function-buffer-lengths"></a><span data-ttu-id="57248-103">Puffer Längen der Netzwerk Verwaltungsfunktion</span><span class="sxs-lookup"><span data-stu-id="57248-103">Network Management Function Buffer Lengths</span></span>

<span data-ttu-id="57248-104">In diesem Thema werden die Anforderungen für Funktions Puffer Längen bei der Verwendung mit den Netzwerkverwaltungs-APIs erörtert.</span><span class="sxs-lookup"><span data-stu-id="57248-104">This topic discusses the requirements for function buffer lengths when used with the network management APIs.</span></span>

<span data-ttu-id="57248-105">Anwendungen, die beim Aufrufen der Enumerationsfunktionen für die Netzwerkverwaltung (und verschiedene Datenabruf Funktionen) Puffergrößen angeben, müssen Puffer angeben, die groß genug sind, um die zurückgegebene Informationsstruktur (oder Strukturen) sowie die Zeichen folgen, auf die ihre Elemente zeigen, aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="57248-105">Applications that specify buffer sizes when calling network management enumeration functions (and various data retrieval functions) must specify buffers large enough to hold the returned information structure (or structures) plus the strings to which their members point.</span></span> <span data-ttu-id="57248-106">Wenn Sie keinen ausreichend großen Puffer angeben, um alle verfügbaren Einträge zu empfangen, gibt die Funktion Fehler \_ Weitere \_ Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="57248-106">If you do not specify a large enough buffer to receive all the available entries, the function returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="57248-107">Enumerationsaufrufe geben keine partiellen Einträge zurück.</span><span class="sxs-lookup"><span data-stu-id="57248-107">Enumeration calls do not return partial entries.</span></span>

<span data-ttu-id="57248-108">Einige Netzwerk Verwaltungsfunktionen verwenden einen richtlinienrichtlinienparameter mit der maximalen Daten Länge " *präfemaxlen*".</span><span class="sxs-lookup"><span data-stu-id="57248-108">Some network management functions take an advisory maximum data-length parameter, *prefmaxlen*.</span></span> <span data-ttu-id="57248-109">Dieser Parameter ermöglicht es einer Anwendung, die Anzahl der Bytes vorzuschlagen, die der Server von einem Funktions Aufrufwert zurückgeben soll.</span><span class="sxs-lookup"><span data-stu-id="57248-109">This parameter allows an application to suggest the number of bytes the server should return from a function call.</span></span>

<span data-ttu-id="57248-110">Wenn Sie im Parameter "präfemaxlen" den Wert "Max \_ Preferred length" angeben \_ , weisen die Netzwerk Verwaltungsfunktionen die Menge an Arbeitsspeicher zu, der für die Daten erforderlich ist. </span><span class="sxs-lookup"><span data-stu-id="57248-110">If you specify the value MAX\_PREFERRED\_LENGTH in the *prefmaxlen* parameter, the network management functions allocate the amount of memory required for the data.</span></span>

<span data-ttu-id="57248-111">Weitere Informationen finden Sie unter [Netzwerk Verwaltungs Funktions Puffer](network-management-function-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="57248-111">For more information, see [Network Management Function Buffers](network-management-function-buffers.md).</span></span>

 

 




