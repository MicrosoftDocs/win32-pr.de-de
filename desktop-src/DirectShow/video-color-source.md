---
description: Video Farbquelle
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Video Farbquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216777"
---
# <a name="video-color-source"></a>Video Farbquelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die Video Farbquelle erstellt ein kontinuierliches Video Bild mit einer voll Tonfarbe.

Klassen-ID (CLSID): **{0cfdd070-581a-11d2-9ee6-006008039e37}**

CLSID-Variablen Name: **CLSID \_ ColorSource**

Eigenschaften



| Eigenschaft | type      | Standard | BESCHREIBUNG                                   |
|----------|-----------|---------|-----------------------------------------------|
| Codes  | **DWORD** | 0       | Gibt die zu Generier gende Farbe an. Siehe Hinweise. |



 

## <a name="remarks"></a>Bemerkungen

Die Video Farb Quelle wird mit Quell Objekten verwendet. Erstellen Sie zunächst ein neues Quell Objekt. Legen Sie dann die untergeordnete GUID des Quell Objekts auf CLSID \_ ColorSource fest, indem Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode aufrufen.

Um die Farbe festzulegen, erstellen Sie ein [Eigenschaften Setter](property-setter.md) -Objekt, und wenden Sie die Color-Eigenschaft zur Zeit 0 (null) an. Der Wert dieser Eigenschaft ist eine hexadezimale Zahl im Format *0xaarrggbb*, wobei *AA* der Alpha Wert, *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist. Alpha Werte reichen von 0x00 (transparent) bis 0xFF (undurchsichtig). Die-Eigenschaft ist statisch und muss zum Zeitpunkt 0 (null) angewendet werden.

Wenn Sie den Alpha Wert nicht angeben, wird der Wert standardmäßig auf 0 (null) (transparent) festgelegt. In einem 32-Bit-Color-Videoprojekt bewirkt dies, dass Übergänge oder Effekte, bei denen Alpha verwendet wird, um die Video Farb Quelle als vollständig transparent darzustellen. Um sicher zu sein, geben Sie immer das Alpha an. Beispielsweise ist " **0xFF000000**" ein undurchsichtiges Schwarzes.

Im folgenden Codebeispiel wird gezeigt, wie dieses-Objekt verwendet wird. Weitere Informationen zur Verwendung von [**ipropertysetter**](ipropertysetter.md)finden Sie unter [Festlegen von Eigenschaften für Effekte und Übergänge](setting-properties-on-effects-and-transitions.md):


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



Das folgende Beispiel zeigt die XML-Darstellung des-Objekts, das im vorherigen Beispiel erstellt wurde. In diesem Fall unterstützt das [**param**](param-element.md) -Element keine oder [**lineare**](linear-element.md) Elemente, da das Objekt dynamische Eigenschaften nicht [**unterstützt:**](at-element.md)


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



