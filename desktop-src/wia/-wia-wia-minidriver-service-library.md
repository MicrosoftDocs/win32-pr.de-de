---
description: Um die Treiber Implementierung so weit wie möglich zu vereinfachen, stellt die Windows-Abbild Erfassung (WIA) eine Minidriver-Dienst Bibliothek bereit, die viele der administrativen Aufgaben durchführt, die für die WIA-Architektur erforderlich sind
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: WIA-Mini Treiber-Dienst Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357346"
---
# <a name="wia-minidriver-service-library"></a><span data-ttu-id="2a859-103">WIA-Mini Treiber-Dienst Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a859-103">WIA Minidriver Service Library</span></span>

<span data-ttu-id="2a859-104">Um die Treiber Implementierung so weit wie möglich zu vereinfachen, stellt die Windows-Abbild Erfassung (WIA) eine Minidriver-Dienst Bibliothek bereit, die viele der administrativen Aufgaben durchführt, die für die WIA-Architektur erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="2a859-104">To simplify driver implementation as much as possible, Windows Image Acquisition (WIA) provides a Minidriver Service Library that performs many of the administrative tasks required by the WIA architecture.</span></span> <span data-ttu-id="2a859-105">Die Dienst Bibliothek stellt Hilfsfunktionen bereit, um die Struktur von [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekten des Geräts zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2a859-105">The service library provides helper functions to maintain the device's tree of [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) objects.</span></span>

<span data-ttu-id="2a859-106">Die grundlegenden Dienst Bibliotheksfunktionen führen Hilfsfunktionen aus, die von den meisten Gerätetreibern anderweitig implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2a859-106">The basic service library functions perform helper functions that most device drivers would otherwise need to implement.</span></span> <span data-ttu-id="2a859-107">Diese Funktionen lesen und Schreiben Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a859-107">These functions read and write properties.</span></span> <span data-ttu-id="2a859-108">Außerdem erstellen Sie Treiber Element Objekte und kopieren Geräte Informations Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a859-108">They also create driver item objects and copy device information properties.</span></span>

 

 



