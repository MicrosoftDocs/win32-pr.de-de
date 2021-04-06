---
title: Laden eines Zeichens
description: Laden eines Zeichens
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710379"
---
# <a name="loading-a-character"></a><span data-ttu-id="2f0cb-103">Laden eines Zeichens</span><span class="sxs-lookup"><span data-stu-id="2f0cb-103">Loading a Character</span></span>

<span data-ttu-id="2f0cb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2f0cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="2f0cb-105">Zum Animieren eines Zeichens müssen Sie zuerst das Zeichen laden.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-105">To animate a character, you must first load the character.</span></span> <span data-ttu-id="2f0cb-106">Verwenden Sie die [**Load**](load-method.md) -Methode, um die Zeichendaten zu laden.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-106">Use the [**Load**](load-method.md) method to load the character's data.</span></span> <span data-ttu-id="2f0cb-107">Der Microsoft-Agent unterstützt zwei Formate für Zeichen-und Animationsdaten: eine einzelne strukturierte Datei und separate Dateien.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-107">Microsoft Agent supports two formats for character and animation data: a single structured file and separate files.</span></span> <span data-ttu-id="2f0cb-108">Normalerweise verwenden Sie das einzelne Dateiformat (. ACS), wenn die Daten lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-108">Typically, you use the single file format (.ACS) when the data is stored locally.</span></span> <span data-ttu-id="2f0cb-109">Das mehrfache Dateiformat (. ACF,. ACA) funktioniert am besten, wenn Sie Animationen einzeln herunterladen möchten, z. b. beim Zugriff auf Animationen von einem HTTP-Server aus.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-109">The multiple file format (.ACF, .ACA) works best when you want to download animations individually, such as when accessing animations from an HTTP server.</span></span>

<span data-ttu-id="2f0cb-110">Eine Client Anwendung kann nur eine einzelne Instanz desselben Zeichens laden.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-110">A client application can load only a single instance of the same character.</span></span> <span data-ttu-id="2f0cb-111">Bei jedem Versuch, dasselbe Zeichen mehrmals zu laden, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-111">Any attempt to load the same character more than once will fail.</span></span> <span data-ttu-id="2f0cb-112">Allerdings kann eine Anwendung über mehrere Instanzen desselben Zeichens verfügen, die durch die Bereitstellung separater Verbindungen mit dem Microsoft-Agent geladen werden.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-112">However, an application can have multiple instances of the same character loaded by providing separate connections to Microsoft Agent.</span></span> <span data-ttu-id="2f0cb-113">Beispielsweise könnte eine Anwendung dasselbe Zeichen aus zwei Kopien des Microsoft-Agent-Steuer Elements laden.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-113">For example, an application could load the same character from two copies of the Microsoft Agent control.</span></span>

<span data-ttu-id="2f0cb-114">Sie können auch eigene Zeichen für die Verwendung mit dem Microsoft-Agent definieren.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-114">You can also define your own characters for use with Microsoft Agent.</span></span> <span data-ttu-id="2f0cb-115">Sie können ein beliebiges renderingtool verwenden, das Sie bevorzugen, um die Images zu erstellen, vorausgesetzt, Sie verfügen über Windows-bitmapformatdateien.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-115">You may use any rendering tool you prefer to create the images, provided that you end up with Windows bitmap format files.</span></span> <span data-ttu-id="2f0cb-116">Verwenden Sie den Zeichen-Editor von Microsoft-Agent, um die Bilder eines Zeichens für die Verwendung mit dem Microsoft-Agent in Animationen zusammenzustellen und zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-116">To assemble and compile a character's images into animations for use with Microsoft Agent, use the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="2f0cb-117">Mit diesem Tool können Sie die Standardeigenschaften eines Zeichens definieren und Animationen für das Zeichen definieren.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-117">This tool enables you to define a character's default properties as well as define animations for the character.</span></span> <span data-ttu-id="2f0cb-118">Mit dem Zeichen-Editor für Microsoft-Agents können Sie auch das entsprechende Dateiformat auswählen, wenn Sie ein Zeichen erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f0cb-118">The Microsoft Agent Character Editor also enables you to select the appropriate file format when you create a character.</span></span>

 

 




