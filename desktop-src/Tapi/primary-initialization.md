---
description: Eine TAPI-Anwendung muss einen Initialisierungs Vorgang aufzurufen, der eine Reihe von Aktionen von TAPI und den Dienstanbietern auffordert, die die Kommunikationsumgebung für die Anwendung einrichten.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Primäre Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350014"
---
# <a name="primary-initialization"></a><span data-ttu-id="e1db1-103">Primäre Initialisierung</span><span class="sxs-lookup"><span data-stu-id="e1db1-103">Primary Initialization</span></span>

<span data-ttu-id="e1db1-104">Eine TAPI-Anwendung muss einen Initialisierungs Vorgang aufzurufen, der eine Reihe von Aktionen von TAPI und den Dienstanbietern auffordert, die die Kommunikationsumgebung für die Anwendung einrichten.</span><span class="sxs-lookup"><span data-stu-id="e1db1-104">A TAPI application must call an initialization operation, which prompts a series of actions from TAPI and the service providers that set up the communication environment for the application.</span></span>

-   <span data-ttu-id="e1db1-105">Die Initialisierung ist synchron und wird erst zurückgegeben, wenn der Vorgang beendet wurde oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e1db1-105">Initialization is synchronous and does not return until the operation is complete or has failed.</span></span>
-   <span data-ttu-id="e1db1-106">Wenn tapisrv nicht bereits ausgeführt wird, wird es von TAPI gestartet.</span><span class="sxs-lookup"><span data-stu-id="e1db1-106">If TAPISRV is not already running, TAPI starts it.</span></span>
-   <span data-ttu-id="e1db1-107">TAPI richtet eine Verbindung mit dem tapisrv-Prozess ein.</span><span class="sxs-lookup"><span data-stu-id="e1db1-107">TAPI sets up a connection to the TAPISRV process.</span></span>
-   <span data-ttu-id="e1db1-108">TAPISVR lädt die in der Registrierung angegebenen Dienstanbieter und fordert Sie auf, die von Ihnen unterstützten Geräte zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e1db1-108">TAPISVR loads the service providers specified in the registry and prompts them to initialize the devices they support.</span></span>

<span data-ttu-id="e1db1-109">**TAPI 2. x:** Anwendungen führen die Initialisierung durch Aufrufen von [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)durch.</span><span class="sxs-lookup"><span data-stu-id="e1db1-109">**TAPI 2.x:** Applications perform initialization by calling [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="e1db1-110">**TAPI 3. x:** Anwendungen nennen [**ittapi:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span><span class="sxs-lookup"><span data-stu-id="e1db1-110">**TAPI 3.x:** Applications call [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span></span>

 

 
