---
title: Iwmpmedia getmarkername-Methode
description: Die getmarkername-Methode gibt den Namen des Markers am angegebenen Index zurück.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- getmarkername-Methode, Windows Media Player
- getmarkername-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, getmarkername-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370312"
---
# <a name="iwmpmediagetmarkername-method"></a>Iwmpmedia:: getmarkername-Methode

Die **getmarkername** -Methode gibt den Namen des Markers am angegebenen Index zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*Markernum* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der MarkerIndex ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. String** -Wert, der der markerName ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt **null** zurück, wenn der angegebene Marker nicht vorhanden ist.

Einige Medienelemente enthalten keine Marker. Verwenden Sie **markercount** , um herauszufinden, wie viele Marker im aktuellen Medien Element sind.

Markerindexnummern beginnen bei 1.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getmarkername** verwendet, um ein mehr zeitiges Textfeld mit den Namen der Marker im aktuellen Medien Element auszufüllen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. markercount (VB und c#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





