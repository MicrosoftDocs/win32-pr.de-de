---
title: Schnittstellen und Klassen in Effekten
description: Es gibt viele Möglichkeiten, Klassen und Schnittstellen in den Effekten 11 zu verwenden.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390521"
---
# <a name="interfaces-and-classes-in-effects"></a><span data-ttu-id="3cd40-103">Schnittstellen und Klassen in Effekten</span><span class="sxs-lookup"><span data-stu-id="3cd40-103">Interfaces and Classes in Effects</span></span>

<span data-ttu-id="3cd40-104">Es gibt viele Möglichkeiten, Klassen und Schnittstellen in den Effekten 11 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3cd40-104">There are many ways to use classes and interfaces in Effects 11.</span></span> <span data-ttu-id="3cd40-105">Informationen zur Schnittstelle und Klassen Syntax finden Sie unter [Schnittstellen und Klassen](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="3cd40-105">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="3cd40-106">In den folgenden Abschnitten wird erläutert, wie Klassen Instanzen für einen Shader angegeben werden, der Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cd40-106">The following sections detail how to specify class instances to a shader which uses interfaces.</span></span> <span data-ttu-id="3cd40-107">In den Beispielen werden die folgenden Schnittstellen und Klassen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3cd40-107">We will use the following interface and classes in the examples:</span></span>


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



<span data-ttu-id="3cd40-108">Beachten Sie, dass Schnittstellen Instanzen mit Klassen Instanzen initialisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="3cd40-108">Note that interface instances can be initialized to class instances.</span></span> <span data-ttu-id="3cd40-109">Arrays von Klassen-und Schnittstellen Instanzen werden ebenfalls unterstützt und können wie im folgenden Beispiel initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="3cd40-109">Arrays of class and interface instances are also supported and they can be initialized as in the following example:</span></span>


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a><span data-ttu-id="3cd40-110">Einheitliche Schnittstellenparameter</span><span class="sxs-lookup"><span data-stu-id="3cd40-110">Uniform Interface Parameters</span></span>

<span data-ttu-id="3cd40-111">Ebenso wie andere einheitliche Datentypen müssen einheitliche Schnittstellenparameter im compileshader-Befehl angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3cd40-111">Just like other uniform data types, uniform interface parameters must be specified in the CompileShader call.</span></span> <span data-ttu-id="3cd40-112">Schnittstellenparameter können globalen Schnittstellen Instanzen oder globalen Klassen Instanzen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3cd40-112">Interface parameters can be assigned to global interface instances or global class instances.</span></span> <span data-ttu-id="3cd40-113">Wenn Sie einer globalen Schnittstellen Instanz zugewiesen ist, hat der Shader eine Abhängigkeit von der Schnittstellen Instanz, was bedeutet, dass er auf eine Klasseninstanz festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3cd40-113">When assigned to a global interface instance, the shader will have a dependency on the interface instance, which means that it must be set to a class instance.</span></span> <span data-ttu-id="3cd40-114">Wenn Sie globalen Klassen Instanzen zugewiesen ist, spezialisiert der Compiler den Shader (wie bei anderen einheitlichen Datentypen), um diese Klasse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3cd40-114">When assigned to global class instances, the compiler specializes the shader (as with other uniform data types) to use that class.</span></span> <span data-ttu-id="3cd40-115">Dies ist für zwei Szenarien wichtig:</span><span class="sxs-lookup"><span data-stu-id="3cd40-115">This is important for two scenarios:</span></span>

1.  <span data-ttu-id="3cd40-116">Shader mit einem 4 \_ x-Ziel können Schnittstellenparameter verwenden, wenn diese Parameter einheitlich sind und globalen Klassen Instanzen zugewiesen sind (sodass keine dynamische Verknüpfung verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="3cd40-116">Shaders with a 4\_x target can use interface parameters if these parameters are uniform and assigned to global class instances (so no dynamic linkage is used).</span></span>
2.  <span data-ttu-id="3cd40-117">Benutzer können sich entscheiden, viele kompilierte, spezialisierte Shader ohne dynamische Verknüpfung oder wenige kompilierte Shader mit dynamischer Verknüpfung zu haben.</span><span class="sxs-lookup"><span data-stu-id="3cd40-117">Users can decide to have many compiled, specialized shaders with no dynamic linkage or few compiled shaders with dynamic linkage.</span></span>


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



<span data-ttu-id="3cd40-118">Wenn pIColor2 über die API unverändert bleibt, sind die beiden vorherigen Durchläufen funktional äquivalent, aber der erste verwendet einen \_ statischen PS 4 \_ 0-Shader, während der zweite einen PS \_ 5 0- \_ Shader mit dynamischer Verknüpfung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cd40-118">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent, but the first uses a ps\_4\_0 static shader while the second uses a ps\_5\_0 shader with dynamic linkage.</span></span> <span data-ttu-id="3cd40-119">Wenn pIColor2 über die Effects-API geändert wird (siehe Festlegen von Klassen Instanzen unten), kann sich das Verhalten des Pixelshader im zweiten Durchlauf ändern.</span><span class="sxs-lookup"><span data-stu-id="3cd40-119">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="non-uniform-interface-parameters"></a><span data-ttu-id="3cd40-120">Nicht einheitliche Schnittstellenparameter</span><span class="sxs-lookup"><span data-stu-id="3cd40-120">Non-Uniform Interface Parameters</span></span>

<span data-ttu-id="3cd40-121">Nicht einheitliche Schnittstellenparameter erstellen Schnittstellen Abhängigkeiten für die Shader.</span><span class="sxs-lookup"><span data-stu-id="3cd40-121">Non-uniform interface parameters create interface dependencies for the shaders.</span></span> <span data-ttu-id="3cd40-122">Beim Anwenden eines Shaders mit Schnittstellenparametern müssen diese Parameter mit dem bindinterfaces-Befehl zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3cd40-122">When applying a shader with interface parameters, these parameters must be assigned in with the BindInterfaces call.</span></span> <span data-ttu-id="3cd40-123">Globale Schnittstellen Instanzen und globale Klassen Instanzen können im bindinterfaces-aufrufen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3cd40-123">Global interface instances and global class instances can be specified in the BindInterfaces call.</span></span>


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



<span data-ttu-id="3cd40-124">Wenn pIColor2 über die API unverändert bleibt, sind die beiden vorherigen Durchläufen funktional äquivalent, und beide verwenden dynamische Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="3cd40-124">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent and both use dynamic linkage.</span></span> <span data-ttu-id="3cd40-125">Wenn pIColor2 über die Effects-API geändert wird (siehe Festlegen von Klassen Instanzen unten), kann sich das Verhalten des Pixelshader im zweiten Durchlauf ändern.</span><span class="sxs-lookup"><span data-stu-id="3cd40-125">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="setting-class-instances"></a><span data-ttu-id="3cd40-126">Festlegen von Klassen Instanzen</span><span class="sxs-lookup"><span data-stu-id="3cd40-126">Setting Class Instances</span></span>

<span data-ttu-id="3cd40-127">Wenn Sie einen Shader mit dynamischer shaderverknüpfung zum Direct3D 11-Gerät festlegen, müssen auch Klassen Instanzen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3cd40-127">When setting a shader with dynamic shader linkage to the Direct3D 11 device, class instances must also be specified.</span></span> <span data-ttu-id="3cd40-128">Es ist ein Fehler, einen solchen Shader mit einer **null** -Klasseninstanz festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3cd40-128">It is an error to set such a shader with a **NULL** class instance.</span></span> <span data-ttu-id="3cd40-129">Daher müssen alle Schnittstellen Instanzen, auf die ein Shader verweist, über eine zugeordnete Klasseninstanz verfügen.</span><span class="sxs-lookup"><span data-stu-id="3cd40-129">Therefore, all interface instances which a shader references must have an associated class instance.</span></span>

<span data-ttu-id="3cd40-130">Im folgenden Beispiel wird gezeigt, wie Sie eine Klasseninstanzvariable aus einem Effekt erhalten und auf eine Schnittstellen Variable festlegen:</span><span class="sxs-lookup"><span data-stu-id="3cd40-130">The following example shows how to get a class instance variable from an effect and set it to an interface variable:</span></span>


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a><span data-ttu-id="3cd40-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cd40-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cd40-132">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="3cd40-132">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 