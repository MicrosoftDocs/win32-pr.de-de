---
title: Benutzerdefinierte Effekte
description: Zeigt, wie Sie Ihre eigenen benutzerdefinierten Effekte mit dem Standard-HLSL schreiben.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102294"
---
# <a name="custom-effects"></a>Benutzerdefinierte Effekte

[Direct2D](./direct2d-portal.md) wird mit einer Reihe von Effekten ausgeliefert, die eine Reihe von gängigen Bild Vorgängen ausführen. Eine umfassende Liste der Effekte finden Sie im Thema [integrierte Effekte](built-in-effects.md) . Für Funktionen, die mit den integrierten Effekten nicht erreicht werden können, können Sie mit Direct2D ihre eigenen benutzerdefinierten Effekte mithilfe von Standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)schreiben. Sie können diese benutzerdefinierten Effekte neben den integrierten Effekten verwenden, die mit Direct2D ausgeliefert werden.

Beispiele für einen kompletten Pixel-, Vertex-und Compute-Shadereffekt finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

In diesem Thema werden die Schritte und Konzepte erläutert, die Sie zum Entwerfen und Erstellen eines benutzerdefinierten Effekts mit vollem Funktionsumfang benötigen.

## <a name="introduction-what-is-inside-an-effect"></a>Einführung: Was ist innerhalb eines Effekts?

![Diagramm zum Ablegen des Schatten Effekts.](images/custom-effects1.png)

Konzeptionell führt ein [Direct2D](./direct2d-portal.md) Effect eine Abbild Erstellung aus, wie z. b. das Ändern der Helligkeit, das desätalisieren eines Bilds oder, wie oben gezeigt, das Erstellen eines Schlag Schattens. Für die APP sind Sie einfach. Sie können NULL oder mehr Eingabe Bilder akzeptieren, mehrere Eigenschaften verfügbar machen, die ihren Vorgang steuern, und ein einzelnes Ausgabe Bild generieren.

Es gibt vier verschiedene Teile eines benutzerdefinierten Effekts, für den ein Effekt Autor zuständig ist:

1.  Wirkungs Schnittstelle: die Effekt Schnittstelle definiert konzeptionell, wie eine APP mit einem benutzerdefinierten Effekt interagiert (z. b. wie viele Eingaben der Effekt annimmt und welche Eigenschaften verfügbar sind). Die Effect-Schnittstelle verwaltet ein Transformations Diagramm, das die eigentlichen Abbild Erstellungs Vorgänge enthält.
2.  Transformations Diagramm: jeder Effekt erstellt ein internes Transformations Diagramm, das aus einzelnen Transformationen besteht. Jede Transformation stellt einen einzelnen Bild Vorgang dar. Der Effekt ist dafür verantwortlich, diese Transformationen in einem Diagramm zu verknüpfen, um den beabsichtigten Abbild Erstellungs Effekt auszuführen. Ein Effekt kann Transformationen als Reaktion auf Änderungen an den externen Eigenschaften des Effekts hinzufügen, entfernen, ändern und neu anordnen.
3.  Transformation: eine Transformation stellt einen einzelnen Bild Vorgang dar. Der Hauptzweck besteht darin, die Shader zu beherbergen, die für jedes Ausgabe Pixel ausgeführt werden. Zu diesem Zweck ist er für die Berechnung der neuen Größe seines Ausgabe Bilds basierend auf der Logik in seinen Shadern verantwortlich. Außerdem muss berechnet werden, aus welchem Bereich des Eingabe Bilds die Shader lesen müssen, um den angeforderten Ausgabebereich zu rendern.
4.  Shader: ein Shader wird für die Eingabe der Transformation auf der GPU ausgeführt (oder CPU, wenn das Software Rendering beim Erstellen des Direct3D-Geräts angegeben wird). Effekt-Shader werden in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) geschrieben und während der Kompilierung des Effekts in Bytecode kompiliert, der dann von der Auswirkung zur Laufzeit geladen wird. In diesem Referenzdokument wird beschrieben, wie Sie [Direct2D](./direct2d-portal.md)-kompatible HLSL schreiben. Die Direct3D-Dokumentation enthält eine grundlegende HLSL-Übersicht.

## <a name="creating-an-effect-interface"></a>Erstellen einer Wirkungs Schnittstelle

Die Effekt Schnittstelle definiert, wie eine APP mit den benutzerdefinierten Effekten interagiert. Um eine Effekt Schnittstelle zu erstellen, muss eine Klasse ID2D1EffectImpl implementieren, Metadaten definieren, die den Effekt beschreiben (z. b. Name, Eingabe Anzahl und Eigenschaften), und Methoden erstellen, die den benutzerdefinierten Effekt für die Verwendung mit [Direct2D](./direct2d-portal.md)registrieren.

Nachdem alle Komponenten für eine Effekt Schnittstelle implementiert wurden, wird der Header der Klasse wie folgt angezeigt:


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a>Implementieren von ID2D1EffectImpl

Die [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) -Schnittstelle enthält drei Methoden, die Sie implementieren müssen:

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a>Initialize (ID2D1EffectContext \* pcontextinternal, ID2D1TransformGraph \* ptransformgraph)

[Direct2D](./direct2d-portal.md) Ruft die [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) -Methode auf, nachdem die [**ID2D1DeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) -Methode von der app aufgerufen wurde. Sie können diese Methode verwenden, um die interne Initialisierung oder alle anderen Vorgänge auszuführen, die für den Effekt benötigt werden. Außerdem können Sie damit den ursprünglichen Transformations Graphen des Effekts erstellen.

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a>Setgraph (ID2D1TransformGraph \* ptransformgraph)

[Direct2D](./direct2d-portal.md) Ruft die [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) -Methode auf, wenn die Anzahl der Eingaben für den Effekt geändert wird. Obwohl die meisten Effekte eine Konstante Anzahl von Eingaben aufweisen, unterstützen andere wie der zusammen [gesetzte Effekt](composite.md) eine Variable Anzahl von Eingaben. Diese Methode ermöglicht es diesen Effekten, das Transformations Diagramm als Reaktion auf eine veränderliche Eingabe Anzahl zu aktualisieren. Wenn ein Effekt eine Variable Eingabe Anzahl nicht unterstützt, kann diese Methode einfach E \_ notimpl zurückgeben.

### <a name="prepareforrender-d2d1_change_type-changetype"></a>Prepareforrendering (D2D1 \_ \_ Änderungstyp ChangeType)

Die [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) -Methode bietet die Möglichkeit, alle Vorgänge als Reaktion auf externe Änderungen auszuführen. [Direct2D](./direct2d-portal.md) ruft diese Methode direkt vor dem Rendern eines Effekts auf, wenn mindestens einer dieser Aktionen true ist:

-   Der Effekt wurde zuvor initialisiert, aber noch nicht gezeichnet.
-   Eine Effekt Eigenschaft hat sich seit dem letzten zeichnen-Befehl geändert.
-   Der Status des aufrufenden [Direct2D](./direct2d-portal.md) -Kontexts (wie dpi) wurde seit dem letzten zeichnen-Befehl geändert.

### <a name="implement-the-effect-registration-and-callback-methods"></a>Implementieren der Effekt Registrierungs-und Rückruf Methoden

Apps müssen Effekte mit [Direct2D](./direct2d-portal.md) registrieren, bevor Sie instanziiert werden. Diese Registrierung bezieht sich auf eine Instanz einer Direct2D Factory und muss jedes Mal wiederholt werden, wenn die app ausgeführt wird. Zum Aktivieren dieser Registrierung definiert ein benutzerdefinierter Effekt eine eindeutige GUID, eine öffentliche Methode, die den Effekt registriert, und eine private Rückruf Methode, die eine Instanz des Effekts zurückgibt.

### <a name="define-a-guid"></a>Definieren einer GUID

Sie müssen eine GUID definieren, die die Auswirkungen auf die Registrierung bei [Direct2D](./direct2d-portal.md)eindeutig identifiziert. Die APP verwendet dieselbe, um den Effekt zu identifizieren, wenn Sie [**ID2D1DeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)aufruft.

In diesem Code wird veranschaulicht, wie eine GUID für einen Effekt definiert wird. Sie müssen eine eigene eindeutige GUID erstellen, indem Sie ein GUID-Generierungs Tool wie guidgen.exe verwenden.


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a>Definieren einer öffentlichen Registrierungsmethode

Definieren Sie als nächstes eine öffentliche Methode, mit der die APP den Effekt mit [Direct2D](./direct2d-portal.md)registriert. Da die Auswirkung-Registrierung spezifisch für eine Instanz einer Direct2D Factory ist, akzeptiert die Methode eine [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) -Schnittstelle als Parameter. Um den Effekt zu registrieren, ruft die-Methode dann die [**ID2D1Factory1:: registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -API für den **ID2D1Factory1** -Parameter auf.

Diese API akzeptiert eine XML-Zeichenfolge, die die Metadaten, Eingaben und Eigenschaften des Effekts beschreibt. Die Metadaten für einen Effekt dienen nur zu Informationszwecken und können von der APP über die [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) -Schnittstelle abgefragt werden. Die Eingabe-und Eigenschaften Daten werden hingegen von [Direct2D](./direct2d-portal.md) verwendet und repräsentieren die Funktionalität des Effekts.

Eine XML-Zeichenfolge für einen minimalen Beispiel Effekt wird hier dargestellt. Das Hinzufügen von benutzerdefinierten Eigenschaften zum XML-Code wird im Abschnitt Hinzufügen von benutzerdefinierten Eigenschaften zu einem Effekt beschrieben.


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a>Definieren einer Effect Factory-Rückruf Methode

Der Effekt muss außerdem eine private Rückruf Methode bereitstellen, die eine Instanz des Effekts über einen einzelnen IUnknown-Parameter zurückgibt \* \* . Ein Zeiger auf diese Methode wird für [Direct2D](./direct2d-portal.md) bereitgestellt, wenn der Effekt über die [**ID2D1Factory1:: registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -API über den [**PD2D1 \_ Effect \_ Factory**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) -Parameter registriert wird \\ .


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a>Implementieren der IUnknown-Schnittstelle

Schließlich muss der Effekt die IUnknown-Schnittstelle implementieren, um Kompatibilität mit com zu erzielen.

## <a name="creating-the-effects-transform-graph"></a>Erstellen des Transformations Diagramms des Effekts

Ein Effekt kann verschiedene Transformationen (einzelne Bild Vorgänge) verwenden, um den gewünschten Bild Verarbeitungs Effekt zu erstellen. Um die Reihenfolge zu steuern, in der diese Transformationen auf das Eingabebild angewendet werden, ordnet der Effekt Sie in einem Transformations Diagramm an. Ein Transformations Diagramm kann die Effekte und Transformationen verwenden, die in [Direct2D](./direct2d-portal.md) enthalten sind, sowie benutzerdefinierte Transformationen, die vom Effekt Autor erstellt werden.

### <a name="using-transforms-included-with-direct2d"></a>Verwenden von in Direct2D enthaltenen Transformationen

Dies sind die am häufigsten verwendeten Transformationen, die mit [Direct2D](./direct2d-portal.md)bereitgestellt werden.

-   [**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): Diese Transformation kombiniert eine beliebige Anzahl von Eingaben basierend auf einer Blend-Beschreibung. Weitere Beispiele finden Sie im Thema [**D2D1 \_ Blend \_ Description**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) und im [Beispiel Direct2D Composite Effect Modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) . Diese Transformation wird von der [**ID2D1EffectContext:: kreateblendtransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) -Methode zurückgegeben.
-   [**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): mit dieser Transformation wird die Ausgabegröße eines Bilds entsprechend dem angegebenen D2D1-Erweiterungs [**\_ \_ Modus**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) erweitert. Diese Transformation wird von der [**ID2D1EffectContext:: kreatebordertransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) -Methode zurückgegeben.
-   [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): mit dieser Transformation wird die Eingabe durch eine beliebige ganze Anzahl von Pixeln verlagert (übersetzt). Diese Transformation wird von der [**ID2D1EffectContext:: kreateoffsettransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) -Methode zurückgegeben.
-   Alle vorhandenen Effekte können als Transformation für die Transformation des Transformations Diagramms mithilfe der [**ID2D1EffectContext:: deatetransformnodefromeffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) -Methode behandelt werden.

### <a name="creating-a-single-node-transform-graph"></a>Erstellen eines Transformations Diagramms mit einem einzelnen Knoten

Nachdem Sie eine Transformation erstellt haben, muss die Eingabe des Effekts mit der Eingabe der Transformation verbunden werden, und die Ausgabe der Transformation muss mit der Ausgabe des Effekts verbunden werden. Wenn ein Effekt nur eine einzelne Transformation enthält, können Sie dies problemlos mit der [**ID2D1TransformGraph:: setsingletransformnode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) -Methode erreichen.

Sie können eine Transformation in den [**Initialisierungs**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) -oder [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) -Methoden des Effekts mithilfe des bereitgestellten ID2D1TransformGraph-Parameters erstellen oder ändern. Wenn ein Effekt Änderungen am Transformations Diagramm in einer anderen Methode vornehmen muss, bei der dieser Parameter nicht verfügbar ist, kann der Effekt den [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) -Parameter als Member-Variable der Klasse speichern und an anderer Stelle darauf zugreifen, wie z. b. [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) oder eine benutzerdefinierte Eigenschaft Rückruf Methode.

Hier sehen Sie eine Beispiel [**Initialisierungs**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) Methode. Diese Methode erstellt ein Transformations Diagramm mit einem einzelnen Knoten, das das Bild auf jeder Achse um 100 Pixel verlagert.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a>Erstellen eines Transformations Diagramms mit mehreren Knoten

Das Hinzufügen mehrerer Transformationen zum Transformations Diagramm eines Effekts ermöglicht die interne Ausführung mehrerer Bild Vorgänge, die einer App als einzelner einheitlicher Effekt präsentiert werden.

Wie bereits erwähnt, kann das Transformations Diagramm des Effekts in jeder Effekt Methode mithilfe des [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) -Parameters bearbeitet werden, der in der [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) -Methode des Effekts empfangen wird. Die folgenden APIs für diese Schnittstelle können verwendet werden, um das Transformations Diagramm eines Effekts zu erstellen oder zu ändern:

### <a name="addnodeid2d1transformnode-pnode"></a>AddNode (ID2D1TransformNode \* pNode)

Die [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) -Methode registriert die Transformation in der Tat mit dem Effekt und muss aufgerufen werden, bevor die Transformation mit einer der anderen Transformations Diagramm Methoden verwendet werden kann.

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a>Connectumeffectinput (UInt32-Objekt, ID2D1TransformNode \* pNode, UInt32 tonodeinputindex)

Die [**connectdeeffectinput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) -Methode verbindet die Bild Eingabe des Effekts mit der Eingabe einer Transformation. Dieselbe Effekt Eingabe kann mit mehreren Transformationen verbunden werden.

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a>Connectnode (ID2D1TransformNode \* pfromnode, ID2D1TransformNode \* ptonode, UInt32 tonodeinputindex)

Die [**connectnode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) -Methode verbindet die Ausgabe einer Transformation mit der Eingabe einer anderen Transformation. Eine Transformations Ausgabe kann mit mehreren Transformationen verbunden werden.

### <a name="setoutputnodeid2d1transformnode-pnode"></a>Setoutputnode (ID2D1TransformNode \* pNode)

Die [**setoutputnode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) -Methode verbindet die Ausgabe einer Transformation mit der Ausgabe des Effekts. Da ein Effekt nur eine Ausgabe hat, kann nur eine einzelne Transformation als "Ausgabe Knoten" festgelegt werden.

In diesem Code werden zwei separate Transformationen verwendet, um einen einheitlichen Effekt zu erzielen. In diesem Fall ist der Effekt ein übersetzter Schlag Schatten.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a>Hinzufügen von benutzerdefinierten Eigenschaften zu einem Effekt

Effekte können benutzerdefinierte Eigenschaften definieren, die es einer APP ermöglichen, das Verhalten des Effekts während der Laufzeit zu ändern. Es gibt drei Schritte, um eine Eigenschaft für einen benutzerdefinierten Effekt zu definieren:

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a>Hinzufügen der Eigenschafts Metadaten zu den Registrierungsdaten des Effekts

### <a name="add-property-to-registration-xml"></a>Eigenschaft zum Registrierungs-XML hinzufügen

Sie müssen die Eigenschaften eines benutzerdefinierten Effekts während der anfänglichen Registrierung des Effekts bei [Direct2D](./direct2d-portal.md)definieren. Zunächst müssen Sie die Registrierungs-XML-Datei des Effekts in der öffentlichen Registrierungsmethode mit der neuen Eigenschaft aktualisieren:


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



Wenn Sie eine Effect-Eigenschaft in XML definieren, benötigen Sie einen Namen, einen Typ und einen anzeigen Amen. Der Anzeige Name einer Eigenschaft sowie die Werte für Kategorie, Autor und Beschreibung des Gesamt Effekts können lokalisiert werden und sollten lokalisiert werden.

Für jede Eigenschaft können mit einem Effekt optional die Werte Default, min und Max angegeben werden. Diese Werte dienen nur zur Informations Verwendung. Sie werden nicht durch [Direct2D](./direct2d-portal.md)erzwungen. Sie müssen jede angegebene Standard-/min-/Maximum-Logik selbst in der Effekt Klasse implementieren.

Der im XML-Code für die-Eigenschaft aufgelistete Typwert muss mit dem entsprechenden Datentyp übereinstimmen, der von den Methoden Getter und Setter der Eigenschaft verwendet wird. In dieser Tabelle werden die entsprechenden XML-Werte für jeden Datentyp angezeigt:



| Datentyp                                                                                                                              | Entsprechender XML-Wert |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Pwstr                                                                                                                                  | Zeichenfolge                  |
| BOOL                                                                                                                                   | bool                    |
| UINT                                                                                                                                   | uint32                  |
| INT                                                                                                                                    | int32                   |
| GLEITKOMMAZAHL                                                                                                                                  | float                   |
| [**D2D \_ Vector \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | Vector2                 |
| [**D2D \_ Vector \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | Vector3                 |
| [**D2D \_ Vector \_ 4f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | Vector4                 |
| [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool)) | matrix3x2               |
| [**D2D \_ Matrix \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | matrix4x3               |
| [**D2D \_ Matrix 4 \_ x 4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | matrix4x4               |
| [**D2D \_ Matrix \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | matrix5x4               |
| Hobby\[\]                                                                                                                               | Blob                    |
| IUnknown\*                                                                                                                             | IUnknown                |
| [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*                                                                                       | ColorContext            |
| CLSID                                                                                                                                  | clsid                   |
| Enumeration ([**D2D1 \_ Interpolations \_ Modus**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)usw.)                                                | enum                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a>Zuordnen der neuen Eigenschaft zu Getter-und Setter-Methoden

Als nächstes muss der Effekt diese neue Eigenschaft den Getter-und Setter-Methoden zuordnen. Dies erfolgt über das [**D2D1- \_ Eigenschafts \_ Bindungs**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) Array, das an die [**ID2D1Factory1:: registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -Methode übergeben wird.

Das [**\_ \_ Bindungs**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) Array der D2D1-Eigenschaft sieht wie folgt aus:


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



Nachdem Sie das XML-und das Bindungs Array erstellt haben, übergeben Sie Sie an die [**registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -Methode:


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



Das Bindungs Makro des D2D1- \_ \_ Werttyps \_ erfordert, dass die Effect-Klasse vor jeder anderen Schnittstelle von [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) geerbt wird.

Benutzerdefinierte Eigenschaften für einen Effekt werden in der Reihenfolge indiziert, in der Sie in der XML-Datei deklariert sind. nach der Erstellung kann die App mithilfe der [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) -Methode und der [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) -Methode darauf zugreifen. Zur einfacheren Handhabung können Sie eine öffentliche Enumeration erstellen, die jede Eigenschaft in der Header Datei des Effekts auflistet:


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a>Erstellen der Getter-und Setter-Methoden für die Eigenschaft

Der nächste Schritt besteht darin, die Getter-und Setter-Methoden für die neue Eigenschaft zu erstellen. Die Namen der Methoden müssen mit den Namen der Methoden identisch sein, die im [**\_ \_ Bindungs**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) Array der D2D1-Eigenschaft angegeben sind. Außerdem muss der im XML-Code des Effekts angegebene Eigenschaftentyp mit dem Typ des Parameters der Setter-Methode und dem Rückgabewert der Getter-Methode identisch sein.


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a>Aktualisieren von Effekt Transformationen als Reaktion auf Eigenschafts Änderung

Um die Bild Ausgabe eines Effekts als Reaktion auf eine Eigenschafts Änderung tatsächlich zu aktualisieren, muss der Effekt die zugrunde liegenden Transformationen ändern. Dies erfolgt in der Regel in der [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) -Methode des Effekts, die [Direct2D](./direct2d-portal.md) automatisch aufruft, wenn eine der Eigenschaften eines Effekts geändert wurde. Allerdings können Transformationen in den Methoden des Effekts aktualisiert werden, wie z. b. Initialize oder die Eigenschaften Setter-Methoden des Effekts.

Wenn beispielsweise ein Effekt ein [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) enthielt und den Offset Wert in Reaktion auf die geänderte Offset Eigenschaft des Effekts ändern wollte, würde er den folgenden Code in [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)hinzufügen:


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a>Erstellen einer benutzerdefinierten Transformation

Um Bild Vorgänge zu implementieren, die über die in [Direct2D](./direct2d-portal.md)bereitgestellten verfügen, müssen Sie benutzerdefinierte Transformationen implementieren. Benutzerdefinierte Transformationen können ein Eingabebild willkürlich durch die Verwendung benutzerdefinierter HLSL-Shader ändern.

Transformationen implementieren eine von zwei verschiedenen Schnittstellen, je nachdem, welche Typen von Shadern Sie verwenden. Transformationen, die Pixel-und/oder Vertex-Shader verwenden, müssen [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)implementieren, während Transformationen mit COMPUTE-Shadern [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform)implementieren müssen. Diese Schnittstellen erben beide von [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform). In diesem Abschnitt geht es um die Implementierung der Funktionalität, die für beides gilt.

Die [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) -Schnittstelle verfügt über vier Methoden zur Implementierung:

### <a name="getinputcount"></a>GetInputCount

Diese Methode gibt eine ganze Zahl zurück, die die Eingabe Anzahl für die Transformation darstellt.


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a>Mapinputrectstooutputrect

[Direct2D](./direct2d-portal.md) Ruft die [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) -Methode jedes Mal auf, wenn die Transformation gerendert wird. Direct2D übergibt ein Rechteck, das die Begrenzungen der einzelnen Eingaben für die Transformation darstellt. Die Transformation ist dann dafür verantwortlich, die Begrenzungen des Ausgabe Bilds zu berechnen. Die Größe der Rechtecke für alle Methoden in dieser Schnittstelle ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) wird in Pixel, nicht in Dips, definiert.

Diese Methode ist auch für die Berechnung des Bereichs der Ausgabe verantwortlich, der auf der Grundlage der Logik seines Shaders und der nicht transparenten Bereiche der einzelnen Eingaben nicht transparent ist. Ein undurchsichtiger Bereich eines Bilds ist so definiert, dass der Alphakanal für das gesamte Rechteck den Wert "1" hat. Wenn unklar ist, ob die Ausgabe einer Transformation nicht transparent ist, sollte das transparente Ausgabe Rechteck als sicherer Wert auf (0, 0, 0, 0) festgelegt werden. [Direct2D](./direct2d-portal.md) verwendet diese Informationen, um renderoptimierungen mit "garantiertem nicht transparenten" Inhalt auszuführen. Wenn dieser Wert ungenau ist, kann dies zu einem falschen Rendering führen.

Sie können das Renderingverhalten der Transformation (wie in den Abschnitten 6 bis 8 definiert) während dieser Methode ändern. Allerdings können Sie andere Transformationen im Transformations Diagramm oder das Diagramm Layout hier nicht ändern.


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



Wenn Sie ein komplexeres Beispiel wünschen, sollten Sie überprüfen, wie ein einfacher weich Arbeits Vorgang dargestellt wird:

Wenn bei einem weichzeichenvorgang ein 5-Pixel-RADIUS verwendet wird, muss die Größe des Ausgabe Rechtecks um 5 Pixel erweitert werden (siehe unten). Wenn Sie Rechteck Koordinaten ändern, muss eine Transformation sicherstellen, dass Ihre Logik keine over/Underflows in den Rechteck Koordinaten verursacht.


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



Da das Bild verschwommen ist, kann ein nicht transparenter Bereich des Bilds nun teilweise transparent sein. Dies liegt daran, dass der Bereich außerhalb des Bilds standardmäßig transparent schwarz ist und diese Transparenz mit dem Bild um die Ränder kombiniert wird. Die Transformation muss dies in den nicht transparenten Rechteck Berechnungen widerspiegeln:


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



Diese Berechnungen werden hier visualisiert:

![Darstellung der Rechteck Berechnung.](images/custom-effects2.png)

Weitere Informationen zu dieser Methode finden Sie auf der Referenzseite zum [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .

### <a name="mapoutputrecttoinputrects"></a>Mapoutputrecttinputrects

[Direct2D](./direct2d-portal.md) Ruft die [**mapoutputrecttoinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -Methode nach [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)auf. Die Transformation muss den Teil des Bilds berechnen, von dem aus gelesen werden muss, um den angeforderten Ausgabebereich ordnungsgemäß zu rendereln.

Wie bereits zuvor, wenn eine Auswirkung genau Pixel 1-1 zuordnet, kann Sie das Ausgabe Rechteck an das Eingabe Rechteck übergeben:


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



Ebenso, wenn eine Transformation ein Bild verkleinert oder erweitert (wie z. b. das Beispiel "weich"), verwenden Pixel häufig umgebende Pixel, um ihren Wert zu berechnen. Bei einem weichungs Wert wird ein Pixel mit den umgebenden Pixeln durchlaufen, auch wenn Sie sich außerhalb der Begrenzungen des Eingabe Bilds befinden. Dieses Verhalten wird in der Berechnung widergespiegelt. Wie zuvor prüft die Transformation beim Erweitern der Koordinaten eines Rechtecks nach Überläufen.


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



In dieser Abbildung wird die Berechnung visualisiert. [Direct2D](./direct2d-portal.md) prüft automatisch transparente schwarze Pixel, in denen das Eingabebild nicht vorhanden ist, sodass die weich Zeichnung schrittweise mit den vorhandenen Inhalten auf dem Bildschirm kombiniert werden kann.

![Abbildung eines Effekts zum Sampling von transparenten schwarzen Pixeln außerhalb eines Rechtecks.](images/custom-effects3.png)

Wenn die Zuordnung nicht trivial ist, sollte diese Methode das Eingabe Rechteck auf den maximalen Bereich festlegen, um korrekte Ergebnisse sicherzustellen. Legen Sie hierzu den linken und den oberen Rand auf int \_ Min und den rechten und unteren Rand auf int max fest \_ .

Weitere Informationen zu dieser Methode finden Sie im Thema [**mapoutputrecttoinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .

### <a name="mapinvalidrect"></a>Mapinvalidrect

[Direct2D](./direct2d-portal.md) ruft auch die [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) -Methode auf. Anders als bei den [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) -und [**mapoutputrecttoinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -Methoden Direct2D ist es jedoch nicht garantiert, Sie zu einem bestimmten Zeitpunkt aufzurufen. Diese Methode entscheidet konzeptionell, welcher Teil der Ausgabe einer Transformation erneut gerendert werden muss, wenn ein Teil oder alle Eingaben geändert werden. Es gibt drei verschiedene Szenarios, für die das ungültige Rect einer Transformation berechnet werden soll.

### <a name="transforms-with-one-to-one-pixel-mapping"></a>Transformationen mit 1-zu-eins-Pixel Zuordnung

Übergeben Sie für Transformationen, die Pixel 1-1 zuordnen, einfach das ungültige Eingabe Rechteck an das ungültige Ausgabe Rechteck:


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a>Transformationen mit m:n-pixelzuordnung

Wenn die Ausgabe Pixel einer Transformation von Ihrem umgebenden Bereich abhängen, muss das ungültige Eingabe Rechteck entsprechend erweitert werden. Dies soll widerspiegeln, dass die Pixel, die das ungültige Eingabe Rechteck umgeben, ebenfalls beeinträchtigt werden und ungültig werden. Beispielsweise wird mit einem Wert von fünf Pixeln die folgende Berechnung verwendet:


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a>Transformationen mit komplexer Pixel Zuordnung

Bei Transformationen, bei denen Eingabe-und Ausgabe Pixel nicht über eine einfache Zuordnung verfügen, kann die gesamte Ausgabe als ungültig markiert werden. Wenn eine Transformation z. b. einfach die durchschnittliche Farbe der Eingabe ausgibt, ändert sich die gesamte Ausgabe der Transformation, wenn sogar ein kleiner Teil der Eingabe geändert wird. In diesem Fall sollte das ungültige Ausgabe Rechteck auf ein logisch unendliches Rechteck festgelegt werden (siehe unten). [Direct2D](./direct2d-portal.md) bindet dies automatisch an die Begrenzungen der Ausgabe.


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



Weitere Informationen zu dieser Methode finden Sie im Thema [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .

Nachdem Sie diese Methoden implementiert haben, enthält der-Header ihrer Transformation Folgendes:


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a>Hinzufügen eines Pixelshaders zu einer benutzerdefinierten Transformation

Nachdem eine Transformation erstellt wurde, muss Sie einen Shader bereitstellen, der die Bild Pixel bearbeitet. In diesem Abschnitt werden die Schritte zum Verwenden eines Pixelshaders mit einer benutzerdefinierten Transformation behandelt.

### <a name="implementing-id2d1drawtransform"></a>Implementieren von ID2D1DrawTransform

Um einen PixelShader zu verwenden, muss die Transformation die [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) -Schnittstelle implementieren, die von der in Abschnitt 5 beschriebenen [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) -Schnittstelle erbt. Diese Schnittstelle enthält eine neue Methode, die implementiert werden soll:

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a>Setdrawinfo (ID2D1DrawInfo \* pdrawinfo)

[Direct2D](./direct2d-portal.md) Ruft die [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode auf, wenn die Transformation zum ersten Mal dem Transformations Diagramm eines Effekts hinzugefügt wird. Diese Methode stellt einen [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameter bereit, der steuert, wie die Transformation gerendert wird. Informationen zu den hier verfügbaren Methoden finden Sie im Thema **ID2D1DrawInfo** .

Wenn die Transformation diesen Parameter als Klassenmember-Variable speichert, kann auf das *drawinfo* -Objekt zugegriffen werden, und es kann von anderen Methoden wie z. b. Eigenschaften Setter oder [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)geändert werden. Insbesondere kann Sie nicht von den [**mapoutputrectdeinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -oder [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) -Methoden auf [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)aufgerufen werden.

### <a name="creating-a-guid-for-the-pixel-shader"></a>Erstellen einer GUID für den Pixelshader

Als nächstes muss die Transformation eine eindeutige GUID für den Pixelshader selbst definieren. Diese wird verwendet, wenn [Direct2D](./direct2d-portal.md) den Shader in den Arbeitsspeicher lädt, und wenn die Transformation den für die Ausführung zu verwendenden Pixelshader auswählt. Tools wie guidgen.exe, die in Visual Studio enthalten sind, können verwendet werden, um eine zufällige GUID zu generieren.


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a>Der Pixelshader wird mit Direct2D geladen.

Ein Pixelshader muss in den Arbeitsspeicher geladen werden, bevor er von der Transformation verwendet werden kann.

Um den Pixelshader in den Arbeitsspeicher zu laden, sollte die Transformation den kompilierten Shader-Bytecode aus dem Lesen. CSO-Datei, die von Visual Studio generiert wurde (Weitere Informationen finden Sie unter [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Dokumentation) in ein Bytearray. Dieses Verfahren wird im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)ausführlich erläutert.

Nachdem die Shader-Daten in ein Bytearray geladen wurden, können Sie die [**loadpixelshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) -Methode für das [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) -Objekt des Effekts aufrufen. [Direct2D](./direct2d-portal.md) ignoriert Aufrufe von **loadpixelshader** , wenn ein Shader mit der gleichen GUID bereits geladen wurde.

Nachdem ein Pixelshader in den Arbeitsspeicher geladen wurde, muss die Transformation ihn zur Ausführung auswählen, indem er seine GUID an die [**setpixelshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) -Methode des [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameters übergibt, der während der [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode bereitgestellt wird. Der Pixelshader muss bereits in den Arbeitsspeicher geladen werden, bevor er zur Ausführung ausgewählt wird.

### <a name="changing-shader-operation-with-constant-buffers"></a>Ändern des shadervorgangs mit konstantenpuffern

Um zu ändern, wie ein Shader ausgeführt wird, kann eine Transformation einen konstanten Puffer an den Pixelshader übergeben. Zu diesem Zweck definiert eine Transformation eine Struktur, die die gewünschten Variablen im Klassen Header enthält:


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



Die Transformation ruft dann die [**ID2D1DrawInfo:: setpixelshaderconstantbuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) -Methode für den [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameter auf, der in der [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode bereitgestellt wird, um diesen Puffer an den Shader zu übergeben.

Das [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) muss auch eine entsprechende Struktur definieren, die den konstanten Puffer darstellt. Die Variablen, die in der Shader-Struktur enthalten sind, müssen mit denen in der Struktur der Transformation identisch sein.


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



Nachdem der Puffer definiert wurde, können die darin enthaltenen Werte von überall innerhalb des Pixelshader gelesen werden.

### <a name="writing-a-pixel-shader-for-direct2d"></a>Schreiben eines Pixelshaders für Direct2D

[Direct2D](./direct2d-portal.md) -Transformationen verwenden Shader, die mithilfe von Standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)erstellt wurden. Es gibt jedoch einige wichtige Konzepte zum Schreiben eines Pixelshaders, der aus dem Kontext einer Transformation ausgeführt wird. Ein vollständiges Beispiel für einen vollständig funktionalen Pixelshader finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

[Direct2D](./direct2d-portal.md) ordnet die Eingaben einer Transformation automatisch den [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) -und [**samplerstate**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) -Objekten in HLSL zu. Der erste **Texture2D** befindet sich unter Register T0 und der erste **samplerstate** unter Register S0. Jede zusätzliche Eingabe befindet sich unter den nächsten entsprechenden Registern (z. b. T1 und S1). Die Pixel Daten für eine bestimmte Eingabe können durch Aufrufen von Sample für das **Texture2D** -Objekt und durch Übergabe des entsprechenden **samplerstate** -Objekts und der Texel-Koordinaten entnommen werden.

Ein benutzerdefinierter Pixelshader wird einmal für jedes Pixel ausgeführt, das gerendert wird. Jedes Mal, wenn der Shader ausgeführt wird, stellt [Direct2D](./direct2d-portal.md) automatisch drei Parameter bereit, die die aktuelle Ausführungs Position identifizieren:

-   Ausgabe des Szene Raums: dieser Parameter stellt die aktuelle Ausführungs Position in Bezug auf die Gesamt-Ziel Oberfläche dar. Er ist in Pixeln definiert, und die minimalen/maximalen Werte entsprechen den Begrenzungen des Rechtecks, das von [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)zurückgegeben wurde.
-   Ausgabe des Ausschneide Raums: dieser Parameter wird von Direct3D verwendet und darf nicht in einem Pixelshader einer Transformation verwendet werden.
-   Texspace Input: dieser Parameter stellt die aktuelle Ausführungs Position in einer bestimmten Eingabe Textur dar. Ein Shader sollte keinerlei Abhängigkeiten davon annehmen, wie dieser Wert berechnet wird. Es sollte nur verwendet werden, um die Eingabe des Pixels-Shaders zu übertragen, wie im folgenden Code gezeigt:


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a>Hinzufügen eines Vertex-Shaders zu einer benutzerdefinierten Transformation

Mithilfe von Vertex-Shadern können Sie verschiedene Abbild Erstellungs Szenarien ausführen als Pixel-Shader. Vertex-Shader können auf Geometrie basierende Bildeffekte durch Transformieren von Vertices durchführen, die ein Bild bilden. Vertex-Shader können unabhängig von oder in Verbindung mit von der Transformation angegebenen Pixel-Shadern verwendet werden. Wenn kein Scheitelpunkt-Shader angegeben ist, ersetzt [Direct2D](./direct2d-portal.md) in einem standardmäßigen Vertex-Shader für die Verwendung mit dem benutzerdefinierten Pixelshader.

Der Prozess zum Hinzufügen eines Vertex-Shaders zu einer benutzerdefinierten Transformation ähnelt dem eines Pixelshaders – die Transformation implementiert die [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) -Schnittstelle, erstellt eine GUID und (optional) übergibt Konstante Puffer an den Shader. Es gibt jedoch einige wichtige zusätzliche Schritte, die für Vertex-Shader eindeutig sind:

### <a name="creating-a-vertex-buffer"></a>Erstellen eines Scheitelpunkt Puffers

Ein Scheitelpunkt-Shader wird durch Definition an den an ihn weiter gegebenen Scheitel Punkten ausgeführt, nicht an einzelne Pixel. Um die Scheitel Punkte für den Shader anzugeben, die auf ausgeführt werden sollen, erstellt eine Transformation einen Vertex-Puffer, der an den Shader übergeben werden soll. Das Layout der Scheitelpunkt Puffer geht über den Rahmen dieses Dokuments hinaus. Weitere Informationen finden Sie in der [Direct3D-Referenz](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) für eine Beispiel Implementierung.

Nach dem Erstellen eines Scheitelpunkt Puffers im Arbeitsspeicher verwendet die Transformation [**die Methode "**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) Methode" für das [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) -Objekt des enthaltenden Effekts, um diese Daten an die GPU zu übergeben. Weitere Informationen finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) für eine Beispiel Implementierung.

Wenn kein Scheitelpunkt Puffer von der Transformation angegeben wird, übergibt [Direct2D](./direct2d-portal.md) einen standardmäßigen Vertex-Puffer, der den Speicherort des rechteckigen Bilds darstellt.

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a>Ändern von setdrawinfo zum Verwenden eines Scheitelpunkt-Shaders

Wie bei Pixel-Shadern muss die Transformation laden und einen Vertex-Shader für die Ausführung auswählen. Um den Vertexshader zu laden, ruft er die [**loadvertexshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) -Methode für die [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) -Methode auf, die in der Initialize-Methode des Effekts empfangen wird. Um den Vertex-Shader für die Ausführung auszuwählen, ruft er [**setvertexprocessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) für den [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameter auf, der in der [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode der Transformation empfangen wird. Diese Methode akzeptiert eine GUID für einen zuvor geladenen Vertex-Shader sowie (optional) einen zuvor erstellten Vertex-Puffer, auf dem der Shader ausgeführt werden soll.

### <a name="implementing-a-direct2d-vertex-shader"></a>Implementieren eines Direct2D Vertex-Shaders

Eine Draw-Transformation kann sowohl einen Pixel-Shader als auch einen Vertexshader enthalten. Wenn eine Transformation sowohl einen Pixel-Shader als auch einen Vertex-Shader definiert, wird die Ausgabe des Vertex-Shader direkt an den Pixelshader übergeben: die APP kann die Rückgabe Signatur des Vertex-Shaders/der Parameter des Pixel-Shaders anpassen, solange Sie konsistent sind.

Wenn eine Transformation dagegen nur einen Scheitelpunkt-Shader enthält und auf dem standardmäßigen Passthrough-Pixelshader von [Direct2D](./direct2d-portal.md)basiert, muss Sie die folgende Standardausgabe zurückgeben:


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Ein Scheitelpunkt-Shader speichert das Ergebnis seiner Scheitelpunkt Transformationen in der Szenen Raum-Ausgabevariable des Shader. Um die Ausgabevariablen für den Ausschneide Bereich und die texspace-Eingabevariablen zu berechnen, stellt [Direct2D](./direct2d-portal.md) automatisch Konvertierungs Matrizen in einem konstanten Puffer bereit:


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



Ein Beispiel für einen Vertex-Shader-Code finden Sie unten, der die Konvertierungs Matrizen verwendet, um die richtigen Clip-und textzspaces zu berechnen, die von [Direct2D](./direct2d-portal.md)


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



Der obige Code kann als Ausgangspunkt für einen Vertex-Shader verwendet werden. Sie durchläuft lediglich das Eingabebild, ohne Transformationen auszuführen. Weitere Informationen finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) für eine vollständig implementierte Vertex-Shader-basierte Transformation.

Wenn kein Scheitelpunkt Puffer von der Transformation angegeben wird, ersetzt [Direct2D](./direct2d-portal.md) in einem standardmäßigen Vertex-Puffer, der den Speicherort des rechteckigen Bilds darstellt. Die Parameter für den Vertex-Shader werden in die Werte der Standard-Shader-Ausgabe geändert:


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Der Vertex-Shader kann seine Parameter *scenespaceoutput* und *clipspaceoutput* nicht ändern. Diese müssen unverändert zurückgegeben werden. Der *texelspaceinput* -Parameter kann jedoch für jedes Eingabebild geändert werden. Wenn die Transformation auch einen benutzerdefinierten Pixelshader enthält, kann der Vertex-Shader weiterhin zusätzliche benutzerdefinierte Parameter direkt an den Pixelshader übergeben. Außerdem wird der benutzerdefinierte Puffer der *scenespace* -Konvertierungs Matrizen (B0) nicht mehr bereitgestellt.

## <a name="adding-a-compute-shader-to-a-custom-transform"></a>Hinzufügen eines Compute-Shaders zu einer benutzerdefinierten Transformation

Zum Schluss können benutzerdefinierte Transformationen Compute-Shader für bestimmte gezielte Szenarien nutzen. Compute-Shader können zum Implementieren komplexer Bildeffekte verwendet werden, die willkürlichen Zugriff auf Eingabe-und Ausgabe Bild Puffer erfordern. Beispielsweise kann ein grundlegender histogrammalgorithmus nicht mit einem Pixelshader implementiert werden, da Einschränkungen für den Speicherzugriff bestehen.

Da Compute-Shader höhere Anforderungen an die Hardware Funktionsebene als Pixel-Shader aufweisen, sollten nach Möglichkeit Pixel-Shader verwendet werden, um einen bestimmten Effekt zu implementieren. Insbesondere können Compute-Shader nur auf den meisten DirectX 10-Karten der Ebene und höher ausgeführt werden. Wenn eine Transformation einen Compute-Shader verwendet, muss Sie zusätzlich zur Implementierung der [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) -Schnittstelle die entsprechende Hardwareunterstützung während der Instanziierung überprüfen.

### <a name="checking-for-compute-shader-support"></a>Überprüfen der Unterstützung von Compute-Shader

Wenn ein Effekt einen Compute-Shader verwendet, muss er während seiner Erstellung mithilfe der [**ID2D1EffectContext:: checkfeaturesupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) -Methode auf die Unterstützung von Compute-Shader überprüfen. Wenn die GPU keine Compute-Shader unterstützt, muss der Effekt [**D2DERR \_ unzureichende \_ Geräte \_ Funktionen**](direct2d-error-codes.md)zurückgeben.

Es gibt zwei verschiedene Arten von Compute-Shadern, die von einer Transformation verwendet werden können: Shader Model 4 (DirectX 10) und Shader Model 5 (DirectX 11). Es gibt bestimmte Einschränkungen für Shader Model 4-Shader. Weitere Informationen finden Sie in der [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Dokumentation. Transformationen können beide Typen von Shadern enthalten und können bei Bedarf auf Shader Model 4 zurückgreifen: im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) finden Sie eine Implementierung dieses.

### <a name="implement-id2d1computetransform"></a>Implementieren von ID2D1ComputeTransform

Diese Schnittstelle enthält zwei neue Methoden, die implementiert werden müssen, zusätzlich zu den in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a>Setcomputeingefo (ID2D1ComputeInfo \* pcomputeingefo)

Wie bei Pixel-und Vertex-Shadern ruft [Direct2D](./direct2d-portal.md) die [**setcomputeinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) -Methode auf, wenn die Transformation zum ersten Mal dem Transformations Diagramm eines Effekts hinzugefügt wird. Diese Methode stellt einen [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) -Parameter bereit, der steuert, wie die Transformation gerendert wird. Dazu gehört auch die Auswahl des Compute-Shaders, der durch die [**ID2D1ComputeInfo:: setcomputeshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) -Methode ausgeführt werden soll. Wenn die Transformation diesen Parameter als Klassenmember-Variable speichert, kann auf Sie über eine beliebige Transformations-oder Effekt Methode zugegriffen und diese geändert werden, mit Ausnahme der [**mapoutputrectdeinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -und [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) -Methoden. Weitere hier verfügbare Methoden finden Sie im Thema **ID2D1ComputeInfo** .

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a>Calculatethrecgroups (ID2D1ComputeInfo \* poutputrect, UInt32 \* pdimensionx, UInt32 \* pdimensiony, UInt32 \* pdimensionz)

Während Pixel-Shader pro Pixel ausgeführt werden und Vertex-Shader pro Scheitelpunkt ausgeführt werden, werden Compute-Shader auf der Basis von Thread Group ausgeführt. Eine Thread Gruppe stellt eine Anzahl von Threads dar, die gleichzeitig auf der GPU ausgeführt werden. Der COMPUTE-Shader-HLSL-Code bestimmt, wie viele Threads pro Thread Group ausgeführt werden sollen. Der Effekt skaliert die Anzahl der Thread Gruppen so, dass der Shader die gewünschte Anzahl von Uhrzeiten ausführt, abhängig von der Logik des Shaders.

Die [**calculatethread Groups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) -Methode ermöglicht der Transformation, zu informieren [Direct2D](./direct2d-portal.md) wie viele Thread Gruppen erforderlich sind, basierend auf der Größe des Bilds und den eigenen Kenntnissen des Shader der Transformation.

Die Häufigkeit, mit der der COMPUTE-Shader ausgeführt wird, ist ein Produkt der Thread Group-Anzahl, die hier angegeben ist, und der numThreads-Anmerkung im COMPUTE-Shader- [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl). Wenn die Transformation z. b. die Thread Group-Dimensionen auf (2, 2, 1) festlegt, gibt der Shader (3, 3, 1) Threads pro Thread Gruppe an, dann werden 4 Thread Gruppen ausgeführt, von denen jeder über 9 Threads verfügt, sodass insgesamt 36 Thread Instanzen verwendet werden.

Ein häufiges Szenario ist die Verarbeitung eines Ausgabe Pixels für jede Instanz des Compute-Shaders. Um die Anzahl der Thread Gruppen für dieses Szenario zu berechnen, dividiert die Transformation die Breite und Höhe des Bilds durch die entsprechenden x-und y-Dimensionen der "numThreads"-Anmerkung im COMPUTE-Shader- [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).

Wichtig: Wenn diese Division durchgeführt wird, muss die Anzahl der angeforderten Thread Gruppen immer auf die nächste ganze Zahl aufgerundet werden, andernfalls werden die "restpixel" nicht auf ausgeführt. Wenn ein Shader (z. b.) ein einzelnes Pixel mit jedem Thread berechnet, würde der Code der Methode wie folgt aussehen.


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



Der [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) verwendet den folgenden Code, um die Anzahl der Threads in den einzelnen Thread Gruppen anzugeben:


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



Während der Ausführung werden der aktuelle Thread Group und der aktuelle Thread Index als Parameter an die Shader-Methode übermittelt:


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a>Lesen von Bilddaten

Compute-Shader greifen als einzelne zweidimensionale Textur auf das Eingabebild der Transformation zu:


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



Wie bei Pixel-Shadern ist es jedoch nicht garantiert, dass die Daten des Bilds in der Textur mit (0,0) beginnen. Stattdessen stellt [Direct2D](./direct2d-portal.md) System Konstanten bereit, mit denen Shader eine beliebige Abweichung ausgleichen können:


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



Nachdem der obige Konstante Puffer und die angegebene Hilfsmethode definiert wurden, kann der Shader Bild Daten mithilfe folgender Beispiele abgleichen:


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a>Schreiben von Bilddaten

[Direct2D](./direct2d-portal.md) erwartet, dass ein Shader einen Ausgabepuffer für das resultierende Bild definiert. In Shader Model 4 (DirectX 10) muss es sich um einen eindimensionalen Puffer aufgrund von Funktionseinschränkungen handeln:


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



Die Ausgabe Textur wird zuerst als indizierte Zeile angezeigt, damit das gesamte Bild gespeichert werden kann.


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



Andererseits können Shader Model 5-Shader (DirectX 11) zweidimensionale Ausgabe Texturen verwenden:


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



Mit Shader Model 5-Shadern bietet [Direct2D](./direct2d-portal.md) einen zusätzlichen Parameter "outpuesffset" im Konstanten Puffer. Die Ausgabe des Shaders sollte durch diesen Betrag ausgelagert werden:


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



Unten wird ein vollständiges Pass-Through-Shader-Modell 5-Compute-Shader angezeigt. Darin werden die einzelnen Compute-Shader-Threads ein einzelnes Pixel des Eingabe Bilds lesen und schreiben.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



Der folgende Code zeigt die äquivalente Shader Model 4-Version des Shaders. Beachten Sie, dass der Shader jetzt in einen eindimensionalen Ausgabepuffer gerendert wird.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 