---
title: Schnittstellen und Klassen
description: Die dynamische shaderverknüpfung nutzt die HLSL-Schnittstellen (High-Level Shader Language) und-Klassen, die syntaktisch mit ihren C++-Entsprechungen vergleichbar sind.
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390752"
---
# <a name="interfaces-and-classes"></a><span data-ttu-id="c9b0b-103">Schnittstellen und Klassen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-103">Interfaces and classes</span></span>

<span data-ttu-id="c9b0b-104">Die dynamische shaderverknüpfung nutzt die HLSL-Schnittstellen (High-Level Shader Language) und-Klassen, die syntaktisch mit ihren C++-Entsprechungen vergleichbar sind.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-104">Dynamic shader linkage makes use of high-level shader language (HLSL) interfaces and classes that are syntactically similar to their C++ counterparts.</span></span> <span data-ttu-id="c9b0b-105">Dadurch können Shader zur Kompilierzeit auf abstrakte Schnittstellen Instanzen verweisen und die Auflösung dieser Instanzen in konkreten Klassen für die Anwendung zur Laufzeit belassen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-105">This allows shaders to reference abstract interface instances at compile time and leave resolution of those instances to concrete classes for the application at runtime.</span></span>

<span data-ttu-id="c9b0b-106">In den folgenden Abschnitten wird erläutert, wie ein Shader für die Verwendung von Schnittstellen und Klassen eingerichtet wird und wie Schnittstellen Instanzen im Anwendungscode initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-106">The following sections detail how to setup a shader to use interfaces and classes and how to initialize interface instances in application code.</span></span>

-   [<span data-ttu-id="c9b0b-107">Deklarieren von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-107">Declaring Interfaces</span></span>](#declaring-interfaces)
-   [<span data-ttu-id="c9b0b-108">Deklarieren von Klassen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-108">Declaring Classes</span></span>](#declaring-classes)
-   [<span data-ttu-id="c9b0b-109">Deklarationen der Schnittstellen Instanz in einem Shader</span><span class="sxs-lookup"><span data-stu-id="c9b0b-109">Interface Instance Declarations in a Shader</span></span>](#interface-instance-declarations-in-a-shader)
-   [<span data-ttu-id="c9b0b-110">Klasseninstanzdeklarationen in einem Shader</span><span class="sxs-lookup"><span data-stu-id="c9b0b-110">Class Instance Declarations in a Shader</span></span>](#class-instance-declarations-in-a-shader)
-   [<span data-ttu-id="c9b0b-111">Initialisieren von Schnittstellen Instanzen in einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="c9b0b-111">Initializing Interface Instances in an Application</span></span>](#initializing-interface-instances-in-an-application)
-   [<span data-ttu-id="c9b0b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-112">Related topics</span></span>](#related-topics)

## <a name="declaring-interfaces"></a><span data-ttu-id="c9b0b-113">Deklarieren von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-113">Declaring interfaces</span></span>

<span data-ttu-id="c9b0b-114">Eine Schnittstelle funktioniert auf ähnliche Weise wie eine abstrakte Basisklasse in C++.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-114">An interface functions in a similar manner to an abstract base class in C++.</span></span> <span data-ttu-id="c9b0b-115">Eine Schnittstelle wird mit dem-Schlüsselwort der-Schnittstelle in einem Shader deklariert und enthält nur Methoden Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-115">An interface is declared in a shader using the interface keyword and only contains method declarations.</span></span> <span data-ttu-id="c9b0b-116">Die in einer Schnittstelle deklarierten Methoden sind alle virtuelle Methoden in allen Klassen, die von der-Schnittstelle abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-116">The methods declared in an interface will all be virtual methods in any classes derived from the interface.</span></span> <span data-ttu-id="c9b0b-117">Abgeleitete Klassen müssen alle in einer Schnittstelle deklarierten Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-117">Derived classes must implement all methods declared in an interface.</span></span> <span data-ttu-id="c9b0b-118">Beachten Sie, dass Schnittstellen die einzige Möglichkeit zum Deklarieren von virtuellen Methoden sind. es gibt kein virtuelles Schlüsselwort wie in C++, und Klassen deklarieren keine virtuellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-118">Note that interfaces are the only way to declare virtual methods, there is no virtual keyword as in C++, and classes connot declare virtual methods.</span></span>

<span data-ttu-id="c9b0b-119">Im folgenden Beispiel-Shader-Code werden zwei Schnittstellen deklariert.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-119">The following example shader code declares two interfaces.</span></span>


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a><span data-ttu-id="c9b0b-120">Deklarieren von Klassen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-120">Declaring Classes</span></span>

<span data-ttu-id="c9b0b-121">Eine-Klasse verhält sich ähnlich wie Klassen in C++.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-121">A class behaves in a similar manner to classes in C++.</span></span> <span data-ttu-id="c9b0b-122">Eine Klasse wird mit dem Schlüsselwort class deklariert und kann Element Variablen und-Methoden enthalten.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-122">A class is declared with the class keyword and can contain member variables and methods.</span></span> <span data-ttu-id="c9b0b-123">Eine Klasse kann von 0 (null) oder einer Klasse und NULL oder mehr Schnittstellen erben.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-123">A class can inherit from zero or one class and zero or more interfaces.</span></span> <span data-ttu-id="c9b0b-124">Klassen müssen Implementierungen für alle Schnittstellen in der Vererbungs Kette implementieren oder erben, oder die Klasse kann nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-124">Classes must implement or inherit implementations for all interfaces in its inheritance chain or the class cannot be instantiated.</span></span>

<span data-ttu-id="c9b0b-125">Der folgende Beispiel-Shader-Code veranschaulicht das Ableiten einer Klasse aus einer Schnittstelle und aus einer anderen Klasse.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-125">The following example shader code illustrates deriving a class from an interface and from another class.</span></span>


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a><span data-ttu-id="c9b0b-126">Deklarationen der Schnittstellen Instanz in einem Shader</span><span class="sxs-lookup"><span data-stu-id="c9b0b-126">Interface Instance Declarations in a Shader</span></span>

<span data-ttu-id="c9b0b-127">Eine Schnittstellen Instanz fungiert als Platzhalter für Klassen Instanzen, die eine Implementierung der Methoden der Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-127">An interface instance acts as a place holder for class instances that provide an implementation of the interface's methods.</span></span> <span data-ttu-id="c9b0b-128">Durch die Verwendung einer Instanz einer Schnittstelle kann Shader-Code eine Methode aufrufen, ohne zu wissen, welche Implementierung dieser Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-128">Using an instance of an interface allows shader code to call a method without knowing which implementation of that method will be invoked.</span></span> <span data-ttu-id="c9b0b-129">Shader-Code deklariert eine oder mehrere-Instanzen für jede Schnittstelle, die Sie definiert.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-129">Shader code declares one or more instances for each interface it defines.</span></span> <span data-ttu-id="c9b0b-130">Diese Instanzen werden in Shader-Code auf ähnliche Weise wie C++-Basisklassen Zeiger verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-130">These instances are used in shader code in a similar manner to C++ base class pointers.</span></span>

<span data-ttu-id="c9b0b-131">Der folgende Beispiel-Shader-Code veranschaulicht das Deklarieren mehrerer Schnittstellen Instanzen und deren Verwendung im Shader-Code.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-131">The following example shader code illustrates declaring several interface instances and using them in shader code.</span></span>


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a><span data-ttu-id="c9b0b-132">Klasseninstanzdeklarationen in einem Shader</span><span class="sxs-lookup"><span data-stu-id="c9b0b-132">Class Instance Declarations in a Shader</span></span>

<span data-ttu-id="c9b0b-133">Jede Klasse, die anstelle einer Schnittstellen Instanz verwendet wird, muss entweder als Variable in einem konstanten Puffer deklariert oder von der Anwendung zur Laufzeit mithilfe der [**ID3D11ClassLinkage:: forateclassinstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) -Methode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-133">Each class that will be used in place of an interface instance must either be declared as a variable in a constant buffer or created by the application at runtime using the [**ID3D11ClassLinkage::CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) method.</span></span> <span data-ttu-id="c9b0b-134">Schnittstellen Instanzen werden auf Klassen Instanzen im Anwendungscode verwiesen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-134">Interface instances will be pointed at class instances in the application code.</span></span> <span data-ttu-id="c9b0b-135">Auf Klassen Instanzen kann im Shader-Code wie jede andere Variable verwiesen werden, aber eine Klasse, die von einer Schnittstelle abgeleitet ist, wird in der Regel nur mit einer Schnittstellen Instanz verwendet, und der Shader-Code wird nicht direkt auf Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-135">Class instances can be referenced in shader code like any other variable, but a class that is derived from an interface will typically only be used with an interface instance and will not be referenced by shader code directly.</span></span>

<span data-ttu-id="c9b0b-136">Der folgende Beispiel-Shader-Code veranschaulicht das Deklarieren mehrerer Klassen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-136">The following example shader code illustrates declaring several class instances.</span></span>


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a><span data-ttu-id="c9b0b-137">Initialisieren von Schnittstellen Instanzen in einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="c9b0b-137">Initializing Interface Instances in an Application</span></span>

<span data-ttu-id="c9b0b-138">Schnittstellen Instanzen werden im Anwendungscode initialisiert, indem ein dynamisches Verknüpfungs Array mit Schnittstellen Zuweisungen an eine der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) setshader-Methoden übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-138">Interface instances are initialized in application code by passing a dynamic linkage array containing interface assignments to one of the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader methods.</span></span>

<span data-ttu-id="c9b0b-139">Verwenden Sie die folgenden Schritte, um ein dynamisches Verknüpfungs Array zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="c9b0b-139">To create a dynamic linkage array use the following steps</span></span>

1.  <span data-ttu-id="c9b0b-140">Erstellen Sie ein Klassen Verknüpfungs Objekt mithilfe von " [**kreateclassverknüpfung**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage)".</span><span class="sxs-lookup"><span data-stu-id="c9b0b-140">Create a class linkage object using [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span></span>
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  <span data-ttu-id="c9b0b-141">Erstellen Sie den Shader, der die dynamische Klassen Verknüpfung verwendet, und übergeben Sie das Klassen Verknüpfungs Objekt als Parameter an die Create-Funktion des Shader.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-141">Create the shader that will be using dynamic class linking, passing the class linkage object as a parameter to the shader's create function.</span></span>
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  <span data-ttu-id="c9b0b-142">Erstellen Sie ein [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Objekt mit der [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-142">Create a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) object using the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) function.</span></span>
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  <span data-ttu-id="c9b0b-143">Verwenden Sie das Shader Reflection-Objekt, um die Anzahl der Schnittstellen Instanzen im Shader mithilfe der [**ID3D11ShaderReflection:: getnuminterfaceslots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) -Methode zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-143">Use the shader reflection object to get the number of interface instances in the shader using the [**ID3D11ShaderReflection::GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) method.</span></span>
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  <span data-ttu-id="c9b0b-144">Erstellen Sie ein Array, das groß genug ist, um die Anzahl der Schnittstellen Instanzen im Shader aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-144">Create an array large enough to hold the number of interface instances in the shader.</span></span>
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  <span data-ttu-id="c9b0b-145">Bestimmen Sie den Index im Array, der den einzelnen Schnittstellen Instanzen entspricht, mithilfe von [**ID3D11ShaderReflection:: getvariablebyname**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) und [**ID3D11ShaderReflectionVariable:: getinterfakeslot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span><span class="sxs-lookup"><span data-stu-id="c9b0b-145">Determine the index in the array that corresponds to each interface instance using [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) and [**ID3D11ShaderReflectionVariable::GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span></span>
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  <span data-ttu-id="c9b0b-146">Beziehen Sie mithilfe von [**ID3D11ClassLinkage:: getclassinstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance)eine Klasseninstanz für jedes Klassenobjekt, das von einer Schnittstelle im Shader abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-146">Get a class instance for each class object derived from an interface in the shader using [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span></span>
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  <span data-ttu-id="c9b0b-147">Legen Sie Schnittstellen Instanzen auf Klassen Instanzen fest, indem Sie den entsprechenden Eintrag im Array dynamischer Verknüpfungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-147">Set interface instances to class instances by setting the corresponding entry in the dynamic linkage array.</span></span>
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  <span data-ttu-id="c9b0b-148">Übergeben Sie das dynamische Verknüpfungs Array als Parameter an einen setshader-Befehl.</span><span class="sxs-lookup"><span data-stu-id="c9b0b-148">Pass the dynamic linkage array as a parameter to a SetShader call.</span></span>
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c9b0b-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-149">Related topics</span></span>

[<span data-ttu-id="c9b0b-150">Dynamisches Verknüpfen</span><span class="sxs-lookup"><span data-stu-id="c9b0b-150">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)