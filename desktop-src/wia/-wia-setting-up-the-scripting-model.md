---
description: Um das WIA-Skript Modell (Windows Image Acquisition) verwenden zu können, müssen Sie die Datei Wiascr.dll auf dem Computer installiert und registriert haben.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Einrichten der Entwicklungsumgebung für das Skript Modell
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214647"
---
# <a name="setting-up-the-scripting-model-development-environment"></a><span data-ttu-id="2e846-103">Einrichten der Entwicklungsumgebung für das Skript Modell</span><span class="sxs-lookup"><span data-stu-id="2e846-103">Setting up the Scripting Model Development Environment</span></span>

<span data-ttu-id="2e846-104">Um das WIA-Skript Modell (Windows Image Acquisition) verwenden zu können, müssen Sie die Datei Wiascr.dll auf dem Computer installiert und registriert haben.</span><span class="sxs-lookup"><span data-stu-id="2e846-104">To use the Windows Image Acquisition (WIA) scripting model, you must have the file Wiascr.dll installed and registered on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="2e846-105">Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2e846-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="2e846-106">Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)</span><span class="sxs-lookup"><span data-stu-id="2e846-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="2e846-107">Kopieren Sie diese Datei aus dem WIA-SDK in das Verzeichnis *% windir%*/System32 (z. b. c: \\ Windows \\ system32).</span><span class="sxs-lookup"><span data-stu-id="2e846-107">Copy this file from the WIA SDK into the *%windir%*/System32 (for example, c:\\windows\\System32) directory.</span></span> <span data-ttu-id="2e846-108">Navigieren Sie in der Befehlszeile zu diesem Verzeichnis, und geben Sie **regsvr32 Wiascr.dll** ein.</span><span class="sxs-lookup"><span data-stu-id="2e846-108">At the command line, navigate to this directory, and type **regsvr32 Wiascr.dll**.</span></span>

<span data-ttu-id="2e846-109">Dies gibt die erforderlichen Informationen in der Systemregistrierung ein.</span><span class="sxs-lookup"><span data-stu-id="2e846-109">This enters the necessary information in the system registry.</span></span>

<span data-ttu-id="2e846-110">Sie können jetzt das WIA-Skript Modell verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e846-110">You are now ready to use the WIA scripting model.</span></span>

 

 
