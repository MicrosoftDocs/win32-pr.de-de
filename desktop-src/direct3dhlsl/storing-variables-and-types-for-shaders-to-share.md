---
title: Speichern von Variablen und Typen für die Freigabe von Shadern
description: Das Klassen Verknüpfungs Objekt ist ein Namespace für Variablen und Typen, die von mehreren Shadern gemeinsam genutzt werden können.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976824"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a><span data-ttu-id="3d03b-103">Speichern von Variablen und Typen für die Freigabe von Shadern</span><span class="sxs-lookup"><span data-stu-id="3d03b-103">Storing Variables and Types for Shaders to Share</span></span>

<span data-ttu-id="3d03b-104">Das Klassen Verknüpfungs Objekt ist ein Namespace für Variablen und Typen, die von mehreren Shadern gemeinsam genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="3d03b-104">The class linkage object is a namespace for variables and types that multiple shaders can share.</span></span> <span data-ttu-id="3d03b-105">Wenn Sie ein Klassen Verknüpfungs Objekt an einen-Befehl übergeben, um einen Shader zu erstellen, sammelt die Laufzeit eine Liste der Variablen und Typen, die jede Schnittstelle im Shader implementieren können, und speichert die Namen dieser Variablen und Typen im Klassen Verknüpfungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="3d03b-105">When you pass a class linkage object in a call to create a shader, the runtime gathers a list of variables and types that can implement each interface in the shader and stores the names of those variables and types in the class linkage object.</span></span>

<span data-ttu-id="3d03b-106">Wenn Sie daher die [**ID3D11ClassLinkage:: getclassinstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) -Methode aufrufen, um Klassen Instanzen aus dem Klassen Verknüpfungs Objekt zu generieren, kann die Common Language Runtime die Variable oder den Typ abrufen, die dem Namen entspricht, der in den einzelnen Shader bereitgestellt wird (wenn der Name für einen bestimmten Shader gültig ist) und der mit dem angegebenen Klassen Verknüpfungs Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3d03b-106">Therefore, when you call the [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) method to generate class instances from the class linkage object, the runtime can retrieve the variable or type that corresponds to the name that is provided in each shader (if that name is valid for a given shader) and that is created with the given class linkage object.</span></span>

<span data-ttu-id="3d03b-107">Angenommen, Sie verfügen über eine einfache **Klasse, die eine** **Farb** Schnittstelle implementiert, und Sie verwenden diese Klasse in Ihrem Scheitelpunkt-Shader und PixelShader.</span><span class="sxs-lookup"><span data-stu-id="3d03b-107">For example, suppose you have a **Light** class that implements a **Color** interface, and you use this class in your vertex shader and pixel shader.</span></span> <span data-ttu-id="3d03b-108">Wenn Sie einen Shader erstellen (z. b. durch Aufrufen von [**ID3D11Device:: createpixelshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), stellt die Laufzeit fest, dass der **Light** -Klassentyp in Scheitelpunkt-und Pixel-Shadern verfügbar ist, und fügt dem Klassen Verknüpfungs Objekt den **Light** -Klassentyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="3d03b-108">When you create a shader (for example, by calling [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), the runtime determines that the **Light** class type is available in both vertex and pixel shaders and adds the **Light** class type to the class linkage object.</span></span> <span data-ttu-id="3d03b-109">Anschließend können Sie an einem gewünschten Speicherort eine **Light** -Instanz erstellen, die Ressourcen für beide Shader binden und diese Instanz im Klassen Instanzen Array übergeben, wenn Sie den Shader auf das Gerät festlegen (z. b. durch Aufrufen von [**Verknüpfung id3d11devicecontext aus::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span><span class="sxs-lookup"><span data-stu-id="3d03b-109">You can then create a **Light** instance at a location that you want, bind the resources for both shaders, and pass this instance in the class instances array when you set the shader to the device (for example, by calling [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span></span> <span data-ttu-id="3d03b-110">Die Laufzeit führt dann die folgende Sequenz aus:</span><span class="sxs-lookup"><span data-stu-id="3d03b-110">The runtime then performs the following sequence:</span></span>

1.  <span data-ttu-id="3d03b-111">Überprüft, ob die Instanz mit dem gleichen Klassen Verknüpfungs Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3d03b-111">Verifies that the instance was created with the same class linkage object.</span></span>
2.  <span data-ttu-id="3d03b-112">Überprüft, ob der **Light** -Klassentyp in Scheitelpunkt-und Pixel-Shadern verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3d03b-112">Verifies that the **Light** class type is availabe in both vertex and pixel shaders.</span></span>
3.  <span data-ttu-id="3d03b-113">Wählt die richtigen Funktionstabellen aus, die für den Scheitelpunkt und die Pixel-Shader unterschiedlich sein können.</span><span class="sxs-lookup"><span data-stu-id="3d03b-113">Selects the correct function tables, which can be different for the vertex and pixel shaders.</span></span>
4.  <span data-ttu-id="3d03b-114">Sendet die Offsets, die von der-Instanz bereitstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3d03b-114">Sends down the offsets that the instance provides.</span></span>

<span data-ttu-id="3d03b-115">Das Klassen Verknüpfungs Objekt ist letztendlich ein Repository vom Typ und Variablennamen.</span><span class="sxs-lookup"><span data-stu-id="3d03b-115">The class linkage object is ultimately a repository of type and variable names.</span></span> <span data-ttu-id="3d03b-116">Die maximale Anzahl von Namen, die für jedes Element (Typ und Variable) verfügbar sind, beträgt 64K.</span><span class="sxs-lookup"><span data-stu-id="3d03b-116">The maximum number of names available for each item (type and variable) is 64K.</span></span> <span data-ttu-id="3d03b-117">Je länger der Typ und die Variablennamen sind, desto höher ist der Speicherbedarf für die Schnittstellen Metadaten, die pro Shader gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3d03b-117">The longer the type and variable names are, the higher the storage requirement is for the interface metadata that is stored per shader.</span></span> <span data-ttu-id="3d03b-118">Dies liegt daran, dass die Laufzeit für jeden Shader eine Zuordnung für diese Namen speichern muss.</span><span class="sxs-lookup"><span data-stu-id="3d03b-118">This is because the runtime must store a mapping for these names for each shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d03b-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3d03b-119">Related Topics</span></span>

[<span data-ttu-id="3d03b-120">Dynamisches Verknüpfen</span><span class="sxs-lookup"><span data-stu-id="3d03b-120">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a><span data-ttu-id="3d03b-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d03b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d03b-122">Dynamisches Verknüpfen</span><span class="sxs-lookup"><span data-stu-id="3d03b-122">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 