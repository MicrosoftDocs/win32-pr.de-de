---
title: Konvertieren von Konvertierungs-Plug-ins
description: Konvertieren von Konvertierungs-Plug-ins
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, Konvertierungs-Plug-ins
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, registrieren
- Registrierung, Konvertierungs-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341228"
---
# <a name="registering-conversion-plug-ins"></a><span data-ttu-id="aa851-108">Konvertieren von Konvertierungs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="aa851-108">Registering Conversion Plug-ins</span></span>

<span data-ttu-id="aa851-109">Drittanbieter Formate müssen registriert werden, bevor Windows Media Player das Konvertierungs-Plug-in instanziieren und verwenden können.</span><span class="sxs-lookup"><span data-stu-id="aa851-109">Third-party formats must be registered before Windows Media Player can instantiate and use the conversion plug-in.</span></span> <span data-ttu-id="aa851-110">Um die Datei für die Konvertierung zu registrieren, müssen Sie die Dateinamenerweiterung registrieren, die dem Format zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aa851-110">To register your file for conversion, you must register the file name extension associated with your format.</span></span>

<span data-ttu-id="aa851-111">Die Liste der registrierten Dateinamen Erweiterungen wird als Satz von Registrierungs Schlüsseln verwaltet.</span><span class="sxs-lookup"><span data-stu-id="aa851-111">The list of registered file name extensions is maintained as a set of registry keys.</span></span> <span data-ttu-id="aa851-112">Ausführliche Informationen zum Registrieren von Drittanbieter Formaten finden Sie unter [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="aa851-112">For details about registering third-party formats, see [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="aa851-113">In der folgenden Tabelle werden die Einstellungen der Registrierungs Werte zum Registrieren eines Drittanbieter Formats für die Konvertierung mithilfe eines Konvertierungs-Plug-Ins aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aa851-113">The following table lists the registry value settings to register a third-party format for conversion by using a conversion plug-in.</span></span>



| <span data-ttu-id="aa851-114">Wert</span><span class="sxs-lookup"><span data-stu-id="aa851-114">Value</span></span>                  | <span data-ttu-id="aa851-115">Einstellung</span><span class="sxs-lookup"><span data-stu-id="aa851-115">Setting</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="aa851-116">**Laufzeit**</span><span class="sxs-lookup"><span data-stu-id="aa851-116">**Runtime**</span></span>            | <span data-ttu-id="aa851-117">13</span><span class="sxs-lookup"><span data-stu-id="aa851-117">13</span></span>                                                          |
| <span data-ttu-id="aa851-118">**Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="aa851-118">**Permissions**</span></span>        | <span data-ttu-id="aa851-119">8 (Berechtigungen für die Bibliothek).</span><span class="sxs-lookup"><span data-stu-id="aa851-119">8 (Permission for the library).</span></span>                             |
| <span data-ttu-id="aa851-120">**Convertpluginclsid**</span><span class="sxs-lookup"><span data-stu-id="aa851-120">**ConvertPluginCLSID**</span></span> | <span data-ttu-id="aa851-121">Die Klassen-ID des Konvertierungs-Plug-ins im Registrierungs Format.</span><span class="sxs-lookup"><span data-stu-id="aa851-121">The class ID of the conversion plug-in, in registry format.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aa851-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa851-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa851-123">**Programmier Referenz für Konvertierungs-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="aa851-123">**Conversion Plug-ins Programming Reference**</span></span>](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




