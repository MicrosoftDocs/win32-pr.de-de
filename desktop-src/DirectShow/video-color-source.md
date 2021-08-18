---
description: Videofarbquelle
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Videofarbquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331640a9240ef0ea16ff565180503066f22ce5ae2550fa1e1ec524dcf05c8fa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071934"
---
# <a name="video-color-source"></a>Videofarbquelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die Videofarbquelle erstellt ein fortlaufendes Videobild einer Volltonfarbe.

Klassen-ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**

CLSID-Variablenname: **CLSID \_ ColorSource**

Eigenschaften



| Eigenschaft | type      | Standard | Beschreibung                                   |
|----------|-----------|---------|-----------------------------------------------|
| "Farbe"  | **DWORD** | 0       | Gibt die zu generierende Farbe an. Siehe Hinweise. |



 

## <a name="remarks"></a>Hinweise

Die Videofarbquelle wird mit Quellobjekten verwendet. Erstellen Sie zunächst ein neues Quellobjekt. Legen Sie dann die UNTEROBJEKT-GUID des Quellobjekts auf CLSID ColorSource fest, indem Sie die \_ [**IAMTimelineObj::SetSubObjectGUID-Methode**](iamtimelineobj-setsubobjectguid.md) aufrufen.

Erstellen Sie zum Festlegen der Farbe ein [Property Setter-Objekt,](property-setter.md) und wenden Sie die Eigenschaft "Color" zum Zeitpunkt 0 (null) an. Der Wert dieser Eigenschaft ist eine Hexadezimalzahl im Format *0xAARRGGBB,* wobei *AA* der Alphawert, *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist. Alphawerte reichen von 0x00 (transparent) bis 0xFF (nicht transparent). Die -Eigenschaft ist statisch und muss zum Zeitpunkt 0 (null) angewendet werden.

Wenn Sie den Alphawert nicht angeben, wird standardmäßig 0 (transparent) verwendet. In einem 32-Bit-Farbvideoprojekt verursacht dies Übergänge oder Effekte, die Alpha verwenden, um die Videofarbquelle als vollständig transparent zu rendern. Um sicher zu sein, geben Sie immer das Alpha an. Beispielsweise ist opakes Schwarz **0xFF000000.**

Im folgenden Codebeispiel wird die Verwendung dieses -Objekts veranschaulicht. Weitere Informationen zur Verwendung von [**IPropertySetter finden**](ipropertysetter.md)Sie unter [Festlegen von Eigenschaften für Effekte und Übergänge:](setting-properties-on-effects-and-transitions.md)


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



Das folgende Beispiel zeigt die XML-Darstellung des -Objekts, das im vorherigen Beispiel erstellt wurde. In diesem Fall unterstützt [**das param-Element**](param-element.md) keine [**at-**](at-element.md) oder [**linearen**](linear-element.md) Elemente, da das -Objekt keine dynamischen Eigenschaften unterstützt:


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



