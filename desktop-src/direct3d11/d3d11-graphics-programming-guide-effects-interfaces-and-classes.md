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
# <a name="interfaces-and-classes-in-effects"></a>Schnittstellen und Klassen in Effekten

Es gibt viele Möglichkeiten, Klassen und Schnittstellen in den Effekten 11 zu verwenden. Informationen zur Schnittstelle und Klassen Syntax finden Sie unter [Schnittstellen und Klassen](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

In den folgenden Abschnitten wird erläutert, wie Klassen Instanzen für einen Shader angegeben werden, der Schnittstellen verwendet. In den Beispielen werden die folgenden Schnittstellen und Klassen verwendet:


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



Beachten Sie, dass Schnittstellen Instanzen mit Klassen Instanzen initialisiert werden können. Arrays von Klassen-und Schnittstellen Instanzen werden ebenfalls unterstützt und können wie im folgenden Beispiel initialisiert werden:


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a>Einheitliche Schnittstellenparameter

Ebenso wie andere einheitliche Datentypen müssen einheitliche Schnittstellenparameter im compileshader-Befehl angegeben werden. Schnittstellenparameter können globalen Schnittstellen Instanzen oder globalen Klassen Instanzen zugewiesen werden. Wenn Sie einer globalen Schnittstellen Instanz zugewiesen ist, hat der Shader eine Abhängigkeit von der Schnittstellen Instanz, was bedeutet, dass er auf eine Klasseninstanz festgelegt werden muss. Wenn Sie globalen Klassen Instanzen zugewiesen ist, spezialisiert der Compiler den Shader (wie bei anderen einheitlichen Datentypen), um diese Klasse zu verwenden. Dies ist für zwei Szenarien wichtig:

1.  Shader mit einem 4 \_ x-Ziel können Schnittstellenparameter verwenden, wenn diese Parameter einheitlich sind und globalen Klassen Instanzen zugewiesen sind (sodass keine dynamische Verknüpfung verwendet wird).
2.  Benutzer können sich entscheiden, viele kompilierte, spezialisierte Shader ohne dynamische Verknüpfung oder wenige kompilierte Shader mit dynamischer Verknüpfung zu haben.


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



Wenn pIColor2 über die API unverändert bleibt, sind die beiden vorherigen Durchläufen funktional äquivalent, aber der erste verwendet einen \_ statischen PS 4 \_ 0-Shader, während der zweite einen PS \_ 5 0- \_ Shader mit dynamischer Verknüpfung verwendet. Wenn pIColor2 über die Effects-API geändert wird (siehe Festlegen von Klassen Instanzen unten), kann sich das Verhalten des Pixelshader im zweiten Durchlauf ändern.

## <a name="non-uniform-interface-parameters"></a>Nicht einheitliche Schnittstellenparameter

Nicht einheitliche Schnittstellenparameter erstellen Schnittstellen Abhängigkeiten für die Shader. Beim Anwenden eines Shaders mit Schnittstellenparametern müssen diese Parameter mit dem bindinterfaces-Befehl zugewiesen werden. Globale Schnittstellen Instanzen und globale Klassen Instanzen können im bindinterfaces-aufrufen angegeben werden.


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



Wenn pIColor2 über die API unverändert bleibt, sind die beiden vorherigen Durchläufen funktional äquivalent, und beide verwenden dynamische Verknüpfungen. Wenn pIColor2 über die Effects-API geändert wird (siehe Festlegen von Klassen Instanzen unten), kann sich das Verhalten des Pixelshader im zweiten Durchlauf ändern.

## <a name="setting-class-instances"></a>Festlegen von Klassen Instanzen

Wenn Sie einen Shader mit dynamischer shaderverknüpfung zum Direct3D 11-Gerät festlegen, müssen auch Klassen Instanzen angegeben werden. Es ist ein Fehler, einen solchen Shader mit einer **null** -Klasseninstanz festzulegen. Daher müssen alle Schnittstellen Instanzen, auf die ein Shader verweist, über eine zugeordnete Klasseninstanz verfügen.

Im folgenden Beispiel wird gezeigt, wie Sie eine Klasseninstanzvariable aus einem Effekt erhalten und auf eine Schnittstellen Variable festlegen:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 