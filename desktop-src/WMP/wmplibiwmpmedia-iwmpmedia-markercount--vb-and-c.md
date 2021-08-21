---
title: IWMPMedia markerCount-Eigenschaft
description: Die markerCount-Eigenschaft ruft die Anzahl der Marker im Medienelement ab.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- markerCount-Windows Media Player
- markerCount-Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , markerCount-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8afbc402858452c987bb6f2dcce0e1ad0428b8c67b81d2369de2a8cdbc6a7dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053628"
---
# <a name="iwmpmediamarkercount-property"></a>IWMPMedia::markerCount-Eigenschaft

Die **markerCount-Eigenschaft** ruft die Anzahl der Marker im Medienelement ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das die Markeranzahl ist.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt 0 (null) zurück, wenn eine Datei über keine Marker verfügt oder wenn das Medienelement nicht mit dem in AxWindowsMediaPlayer.currentMedia angegebenen Element identisch ist.

Markernummern beginnen bei 1.

Bevor Sie diese Eigenschaft verwenden können, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **markerCount verwendet,** um die Anzahl der Marker im aktuellen Medienelement abzurufen. Dieser Wert wird dann als obere Grenze für eine Schleifenstruktur verwendet, die die Markerliste durchläuft, um jeden Markernamen abzurufen und in einem mehrzeilenigen Textfeld anzuzeigen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB und C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





