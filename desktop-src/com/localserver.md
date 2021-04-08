---
title: LocalServer
description: Gibt den vollständigen Pfad zu einer 16-Bit-Anwendung für den lokalen Server an.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- Registrierungsschlüssel für LocalServer com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037306"
---
# <a name="localserver"></a><span data-ttu-id="209a9-104">LocalServer</span><span class="sxs-lookup"><span data-stu-id="209a9-104">LocalServer</span></span>

<span data-ttu-id="209a9-105">Gibt den vollständigen Pfad zu einer 16-Bit-Anwendung für den lokalen Server an.</span><span class="sxs-lookup"><span data-stu-id="209a9-105">Specifies the full path to a 16-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="209a9-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="209a9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a><span data-ttu-id="209a9-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="209a9-107">Remarks</span></span>

<span data-ttu-id="209a9-108">Dies ist ein **reg \_ SZ** -Wert, der den vollständigen Pfad angibt und beliebige Befehlszeilenargumente enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="209a9-108">This is a **REG\_SZ** value that specifies the full path and can include any command-line arguments.</span></span>

<span data-ttu-id="209a9-109">COM fügt das Flag "-Einbettungs" an die Zeichenfolge an, sodass die Anwendung, die Flags verwendet, die gesamte Zeichenfolge analysieren und nach dem-Einbettungs Flag suchen muss.</span><span class="sxs-lookup"><span data-stu-id="209a9-109">COM appends the "-Embedding" flag to the string, so the application that uses flags must parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="209a9-110">Um einen COM-Objekt Server in einem separaten Speicherbereich auszuführen, ändern Sie den Wert von **LocalServer** wie folgt:</span><span class="sxs-lookup"><span data-stu-id="209a9-110">To run a COM object server in a separate memory space, change the value of **LocalServer** as follows:</span></span>

<span data-ttu-id="209a9-111">**cmd/c Start/separate** *Path \* \* *. exe**</span><span class="sxs-lookup"><span data-stu-id="209a9-111">**cmd /c start /separate** *path\*\*\*.exe*\*</span></span>

## <a name="related-topics"></a><span data-ttu-id="209a9-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="209a9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="209a9-113">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="209a9-113">**LocalServer32**</span></span>](localserver32.md)
</dt> </dl>

 

 




