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
# <a name="interfaces-and-classes"></a>Schnittstellen und Klassen

Die dynamische shaderverknüpfung nutzt die HLSL-Schnittstellen (High-Level Shader Language) und-Klassen, die syntaktisch mit ihren C++-Entsprechungen vergleichbar sind. Dadurch können Shader zur Kompilierzeit auf abstrakte Schnittstellen Instanzen verweisen und die Auflösung dieser Instanzen in konkreten Klassen für die Anwendung zur Laufzeit belassen.

In den folgenden Abschnitten wird erläutert, wie ein Shader für die Verwendung von Schnittstellen und Klassen eingerichtet wird und wie Schnittstellen Instanzen im Anwendungscode initialisiert werden.

-   [Deklarieren von Schnittstellen](#declaring-interfaces)
-   [Deklarieren von Klassen](#declaring-classes)
-   [Deklarationen der Schnittstellen Instanz in einem Shader](#interface-instance-declarations-in-a-shader)
-   [Klasseninstanzdeklarationen in einem Shader](#class-instance-declarations-in-a-shader)
-   [Initialisieren von Schnittstellen Instanzen in einer Anwendung](#initializing-interface-instances-in-an-application)
-   [Zugehörige Themen](#related-topics)

## <a name="declaring-interfaces"></a>Deklarieren von Schnittstellen

Eine Schnittstelle funktioniert auf ähnliche Weise wie eine abstrakte Basisklasse in C++. Eine Schnittstelle wird mit dem-Schlüsselwort der-Schnittstelle in einem Shader deklariert und enthält nur Methoden Deklarationen. Die in einer Schnittstelle deklarierten Methoden sind alle virtuelle Methoden in allen Klassen, die von der-Schnittstelle abgeleitet werden. Abgeleitete Klassen müssen alle in einer Schnittstelle deklarierten Methoden implementieren. Beachten Sie, dass Schnittstellen die einzige Möglichkeit zum Deklarieren von virtuellen Methoden sind. es gibt kein virtuelles Schlüsselwort wie in C++, und Klassen deklarieren keine virtuellen Methoden.

Im folgenden Beispiel-Shader-Code werden zwei Schnittstellen deklariert.


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



## <a name="declaring-classes"></a>Deklarieren von Klassen

Eine-Klasse verhält sich ähnlich wie Klassen in C++. Eine Klasse wird mit dem Schlüsselwort class deklariert und kann Element Variablen und-Methoden enthalten. Eine Klasse kann von 0 (null) oder einer Klasse und NULL oder mehr Schnittstellen erben. Klassen müssen Implementierungen für alle Schnittstellen in der Vererbungs Kette implementieren oder erben, oder die Klasse kann nicht instanziiert werden.

Der folgende Beispiel-Shader-Code veranschaulicht das Ableiten einer Klasse aus einer Schnittstelle und aus einer anderen Klasse.


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



## <a name="interface-instance-declarations-in-a-shader"></a>Deklarationen der Schnittstellen Instanz in einem Shader

Eine Schnittstellen Instanz fungiert als Platzhalter für Klassen Instanzen, die eine Implementierung der Methoden der Schnittstelle bereitstellen. Durch die Verwendung einer Instanz einer Schnittstelle kann Shader-Code eine Methode aufrufen, ohne zu wissen, welche Implementierung dieser Methode aufgerufen wird. Shader-Code deklariert eine oder mehrere-Instanzen für jede Schnittstelle, die Sie definiert. Diese Instanzen werden in Shader-Code auf ähnliche Weise wie C++-Basisklassen Zeiger verwendet.

Der folgende Beispiel-Shader-Code veranschaulicht das Deklarieren mehrerer Schnittstellen Instanzen und deren Verwendung im Shader-Code.


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



## <a name="class-instance-declarations-in-a-shader"></a>Klasseninstanzdeklarationen in einem Shader

Jede Klasse, die anstelle einer Schnittstellen Instanz verwendet wird, muss entweder als Variable in einem konstanten Puffer deklariert oder von der Anwendung zur Laufzeit mithilfe der [**ID3D11ClassLinkage:: forateclassinstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) -Methode erstellt werden. Schnittstellen Instanzen werden auf Klassen Instanzen im Anwendungscode verwiesen. Auf Klassen Instanzen kann im Shader-Code wie jede andere Variable verwiesen werden, aber eine Klasse, die von einer Schnittstelle abgeleitet ist, wird in der Regel nur mit einer Schnittstellen Instanz verwendet, und der Shader-Code wird nicht direkt auf Sie verweisen.

Der folgende Beispiel-Shader-Code veranschaulicht das Deklarieren mehrerer Klassen Instanzen.


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



## <a name="initializing-interface-instances-in-an-application"></a>Initialisieren von Schnittstellen Instanzen in einer Anwendung

Schnittstellen Instanzen werden im Anwendungscode initialisiert, indem ein dynamisches Verknüpfungs Array mit Schnittstellen Zuweisungen an eine der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) setshader-Methoden übergeben wird.

Verwenden Sie die folgenden Schritte, um ein dynamisches Verknüpfungs Array zu erstellen:

1.  Erstellen Sie ein Klassen Verknüpfungs Objekt mithilfe von " [**kreateclassverknüpfung**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage)".
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  Erstellen Sie den Shader, der die dynamische Klassen Verknüpfung verwendet, und übergeben Sie das Klassen Verknüpfungs Objekt als Parameter an die Create-Funktion des Shader.
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  Erstellen Sie ein [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Objekt mit der [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) -Funktion.
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  Verwenden Sie das Shader Reflection-Objekt, um die Anzahl der Schnittstellen Instanzen im Shader mithilfe der [**ID3D11ShaderReflection:: getnuminterfaceslots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) -Methode zu erhalten.
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  Erstellen Sie ein Array, das groß genug ist, um die Anzahl der Schnittstellen Instanzen im Shader aufzunehmen.
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  Bestimmen Sie den Index im Array, der den einzelnen Schnittstellen Instanzen entspricht, mithilfe von [**ID3D11ShaderReflection:: getvariablebyname**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) und [**ID3D11ShaderReflectionVariable:: getinterfakeslot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  Beziehen Sie mithilfe von [**ID3D11ClassLinkage:: getclassinstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance)eine Klasseninstanz für jedes Klassenobjekt, das von einer Schnittstelle im Shader abgeleitet ist.
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  Legen Sie Schnittstellen Instanzen auf Klassen Instanzen fest, indem Sie den entsprechenden Eintrag im Array dynamischer Verknüpfungen festlegen.
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  Übergeben Sie das dynamische Verknüpfungs Array als Parameter an einen setshader-Befehl.
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

[Dynamisches Verknüpfen](overviews-direct3d-11-hlsl-dynamic-linking.md)