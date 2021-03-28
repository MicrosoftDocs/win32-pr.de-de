---
title: So wird es sein, wie ein Geometry-Shader
description: Die Geometry-Shader-Instanziierung ermöglicht das Ausführen mehrerer Ausführungen desselben Geometry-Shader pro primitiver.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992839"
---
# <a name="how-to-instance-a-geometry-shader"></a><span data-ttu-id="6b99e-103">Gewusst wie: instanzgeometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="6b99e-103">How To: Instance a Geometry Shader</span></span>

<span data-ttu-id="6b99e-104">Die Geometry-Shader-Instanziierung ermöglicht das Ausführen mehrerer Ausführungen desselben Geometry-Shader pro primitiver.</span><span class="sxs-lookup"><span data-stu-id="6b99e-104">Geometry shader instancing allows multiple executions of the same geometry shader to be executed per primitive.</span></span> <span data-ttu-id="6b99e-105">Fügen Sie der Main-shaderfunktion ein Instanzattribut hinzu, und identifizieren Sie im Shader-Funktions Text einen instanzindexparameter, um einen Geometry-Shader zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6b99e-105">To instance a geometry shader, add an instance attribute to the main shader function and identify an instance index parameter in the shader function body.</span></span>

<span data-ttu-id="6b99e-106">Zum Instanztyp eines Geometry-Shaders:</span><span class="sxs-lookup"><span data-stu-id="6b99e-106">To Instance a Geometry Shader:</span></span>

1.  <span data-ttu-id="6b99e-107">Fügen Sie der Main-Funktion das [Instanzattribut](sm5-attributes-instance.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="6b99e-107">Add the [instance attribute](sm5-attributes-instance.md) to the main function.</span></span>

    ```
    [instance(24)]
    ```

    

    <span data-ttu-id="6b99e-108">Dadurch wird die Anzahl der Instanzen (maximal 32) definiert, die für die einzelnen primitiven ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b99e-108">This defines the number of instances (a maximum of 32) to be run for each primitive.</span></span>

2.  <span data-ttu-id="6b99e-109">Fügen Sie den System Wert " [SV \_ gsinstanceid](sv-gsinstanceid.md) " an eine Variable in der Liste der Funktionsparameter an, die zum Nachverfolgen der ID der ausgeführten Instanz verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b99e-109">Attach the [SV\_GSInstanceID](sv-gsinstanceid.md) system value to a variable in the function parameter list that can be used to track the ID of the instance being executed.</span></span>
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  <span data-ttu-id="6b99e-110">Kompilieren Sie den Shader, und erstellen Sie ihn genauso wie jeden anderen Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="6b99e-110">Compile and create the shader just as you would any other geometry shader.</span></span>

<span data-ttu-id="6b99e-111">Weitere Details:</span><span class="sxs-lookup"><span data-stu-id="6b99e-111">Other details include:</span></span>

-   <span data-ttu-id="6b99e-112">Die maximale Anzahl von Instanzen beträgt 32.</span><span class="sxs-lookup"><span data-stu-id="6b99e-112">The maximum instance count is 32.</span></span>
-   <span data-ttu-id="6b99e-113">Die maximale Scheitelpunkt Anzahl ist eine maximale Vertex-Anzahl pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="6b99e-113">The maximum vertex count is a per-instance maximum vertex count.</span></span>
-   <span data-ttu-id="6b99e-114">Jeder instanzaufruf (wie jeder Geometry-Shader-Aufruf) erhöht den Aufruf Zähler und generiert einen impliziten restartstrip ().</span><span class="sxs-lookup"><span data-stu-id="6b99e-114">Each instance invocation (like any geometry shader invocation) increases the invocation count and generates an implicit RestartStrip().</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b99e-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b99e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b99e-116">Geometry-Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="6b99e-116">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




