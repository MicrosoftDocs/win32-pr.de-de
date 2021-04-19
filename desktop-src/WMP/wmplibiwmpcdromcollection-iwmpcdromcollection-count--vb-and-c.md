---
title: Iwmpcdromcollection-Anzahl (Eigenschaft)
description: Die Count-Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- Anzahl der Eigenschaften Fenster Media Player
- Count-Eigenschaft, Windows Media Player, iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle, Windows Media Player, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354652"
---
# <a name="iwmpcdromcollectioncount-property"></a>Iwmpcdromcollection:: count (Eigenschaft)

Die **count** -Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl der verfügbaren Laufwerke ist.

## <a name="remarks"></a>Bemerkungen

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

DVD-Laufwerke werden genau wie CD-Laufwerke gezählt. Das Windows Media Player ActiveX-Steuerelement unterstützt jedoch nur DVD-Funktionen für Windows XP oder höher. In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird count verwendet, um die Anzahl der verfügbaren CD-und DVD-Laufwerke in einem Meldungs Feld anzuzeigen. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromcollection-Schnittstelle (VB und c#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





